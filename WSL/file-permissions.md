---
title: 파일 사용 권한
description: WSL에서 Windows의 파일 사용 권한을 확인 하는 방법 이해
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10, 파일, 사용 권한에 대 한 windows 하위 시스템
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520862"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="85123-104">WSL에 대 한 파일 권한</span><span class="sxs-lookup"><span data-stu-id="85123-104">File Permissions for WSL</span></span>

<span data-ttu-id="85123-105">이 페이지에서는 linux 용 Windows 하위 시스템에서 Linux 파일 사용 권한을 해석 하는 방법에 대해 자세히 설명 합니다. 특히 NT 파일 시스템의 Windows 내부 리소스에 액세스 하는 경우에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="85123-106">이 설명서에서는 [Linux 파일 시스템 권한 구조](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) 를 기본적으로 이해 하 고 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="85123-107">[umask 명령](https://en.wikipedia.org/wiki/Umask)입니다.</span><span class="sxs-lookup"><span data-stu-id="85123-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="85123-108">WSL에서 Windows 파일에 액세스할 때 파일 권한은 Windows 사용 권한에서 계산 되거나 WSL에서 파일에 추가 된 메타 데이터에서 읽혀집니다.</span><span class="sxs-lookup"><span data-stu-id="85123-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="85123-109">이 메타 데이터는 기본적으로 사용 하도록 설정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="85123-110">Windows 파일의 WSL 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="85123-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="85123-111">WSL의 탑재 옵션으로 메타 데이터를 사용 하는 경우 Windows NT 파일의 확장 된 특성을 추가 하 고 해석 하 여 Linux 파일 시스템 권한을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="85123-112">WSL은 다음과 같은 네 가지 NTFS 확장 특성을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="85123-113">특성 이름</span><span class="sxs-lookup"><span data-stu-id="85123-113">Attribute Name</span></span> | <span data-ttu-id="85123-114">설명</span><span class="sxs-lookup"><span data-stu-id="85123-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="85123-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="85123-115">$LXUID</span></span> | <span data-ttu-id="85123-116">사용자 소유자 ID</span><span class="sxs-lookup"><span data-stu-id="85123-116">User Owner ID</span></span> |
| <span data-ttu-id="85123-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="85123-117">$LXGID</span></span> | <span data-ttu-id="85123-118">그룹 소유자 ID</span><span class="sxs-lookup"><span data-stu-id="85123-118">Group Owner ID</span></span> |
| <span data-ttu-id="85123-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="85123-119">$LXMOD</span></span> | <span data-ttu-id="85123-120">파일 모드 (파일 시스템 권한 octals 및 형식, 예: 0777)</span><span class="sxs-lookup"><span data-stu-id="85123-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="85123-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="85123-121">$LXDEV</span></span> | <span data-ttu-id="85123-122">장치 (장치 파일 인 경우)</span><span class="sxs-lookup"><span data-stu-id="85123-122">Device, if it is a device file</span></span> |

<span data-ttu-id="85123-123">또한 일반 파일 또는 디렉터리가 아닌 파일 (예: symlink, FIFOs, 블록 장치, unix 소켓 및 문자 장치)에도 NTFS [재분석 지점이](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="85123-124">이렇게 하면 확장 된 특성을 쿼리하지 않고도 지정 된 디렉터리의 파일 종류를 훨씬 빠르게 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="85123-125">파일 액세스 시나리오</span><span class="sxs-lookup"><span data-stu-id="85123-125">File Access Scenarios</span></span>

<span data-ttu-id="85123-126">다음은 Linux 용 Windows 하위 시스템을 사용 하 여 다양 한 방법으로 파일에 액세스할 때 사용 권한이 결정 되는 방법에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="85123-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="85123-127">Linux에서 DrvFS (Windows 드라이브 파일 시스템)의 파일 액세스</span><span class="sxs-lookup"><span data-stu-id="85123-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="85123-128">이러한 시나리오는 `/mnt/c`를 통해 WSL에서 Windows 파일에 액세스할 때 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="85123-129">기존 Windows 파일에서 파일 사용 권한 읽기</span><span class="sxs-lookup"><span data-stu-id="85123-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="85123-130">이 결과는 파일에 기존 메타 데이터가 이미 있는지 여부에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="85123-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="85123-131">**파일에 메타 데이터가 없습니다 (기본값).**</span><span class="sxs-lookup"><span data-stu-id="85123-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="85123-132">파일에 연결 된 메타 데이터가 없으면 Windows 사용자의 유효 사용 권한을 읽기/쓰기/실행 비트로 변환 하 고이를 사용자, 그룹 및 기타에 대 한 동일한 값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="85123-133">예를 들어 Windows 사용자 계정에 읽기 및 실행 권한이 있지만 파일에 대 한 쓰기 권한이 없는 경우 사용자, 그룹 및 기타에 대 한 `r-x`으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="85123-134">Windows에서 파일에 ' 읽기 전용 ' 특성이 설정 되어 있으면 Linux에서 쓰기 권한을 부여 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="85123-135">파일에 메타 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-135">The file has metadata</span></span>

<span data-ttu-id="85123-136">파일에 메타 데이터가 있는 경우 Windows 사용자의 유효 사용 권한을 변환 하는 대신 해당 메타 데이터 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="85123-137">Chmod를 사용 하 여 기존 Windows 파일에 대 한 파일 사용 권한 변경</span><span class="sxs-lookup"><span data-stu-id="85123-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="85123-138">이 결과는 파일에 기존 메타 데이터가 이미 있는지 여부에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="85123-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="85123-139">**파일에 메타 데이터가 없습니다 (기본값).**</span><span class="sxs-lookup"><span data-stu-id="85123-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="85123-140">Chmod에는 하나의 효과만 있습니다. 파일의 모든 쓰기 특성을 제거 하면 Windows 파일의 ' 읽기 전용 ' 특성이 설정 됩니다 .이는 CIFS (Common Internet File System)와 Linux의 SMB (서버 메시지 블록) 클라이언트의 동작 이기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="85123-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="85123-141">파일에 메타 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-141">The file has metadata</span></span>

<span data-ttu-id="85123-142">Chmod는 파일의 기존 메타 데이터에 따라 메타 데이터를 변경 하거나 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="85123-143">메타 데이터에 해당 하는 경우에도 Windows에서 사용 하는 것 보다 더 많은 액세스 권한을 부여할 수 없다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="85123-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="85123-144">예를 들어 `chmod 777`를 사용 하 여 파일에 대 한 쓰기 권한이 있지만 해당 파일에 대 한 액세스를 시도한 경우에는 해당 파일에 쓸 수 없도록 메타 데이터를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="85123-145">Windows 파일에 대 한 읽기 또는 쓰기 명령이 Windows 사용자 권한을 통해 라우팅되도록 interopability.</span><span class="sxs-lookup"><span data-stu-id="85123-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="85123-146">드라이브에서 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="85123-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="85123-147">메타 데이터를 사용할 수 있는지 여부에 따라 결과가 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="85123-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="85123-148">메타 데이터를 사용할 수 없습니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="85123-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="85123-149">새로 만든 파일의 Windows 권한은 특정 보안 설명자 없이 Windows에서 파일을 만든 경우와 동일 합니다 .이는 부모의 권한을 상속 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="85123-150">메타 데이터를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-150">Metadata is enabled</span></span>

<span data-ttu-id="85123-151">파일의 사용 권한 비트는 Linux umask을 따르도록 설정 되며 파일은 메타 데이터와 함께 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="85123-152">어떤 Linux 사용자 및 Linux 그룹이 파일을 소유 하나요?</span><span class="sxs-lookup"><span data-stu-id="85123-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="85123-153">이 결과는 파일에 기존 메타 데이터가 이미 있는지 여부에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="85123-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="85123-154">**파일에 메타 데이터가 없습니다 (기본값).**</span><span class="sxs-lookup"><span data-stu-id="85123-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="85123-155">기본 시나리오에서 Windows 드라이브를 automounting 때 모든 파일에 대 한 UID (사용자 ID)가 WSL 사용자의 사용자 ID로 설정 되 고 GID (그룹 ID)가 WSL 사용자의 주 그룹 ID로 설정 되도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="85123-156">파일에 메타 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-156">The file has metadata</span></span>

<span data-ttu-id="85123-157">메타 데이터에 지정 된 UID 및 GID는 파일의 사용자 소유자 및 그룹 소유자로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="85123-158">`\\wsl$`를 사용 하 여 Windows에서 Linux 파일 액세스</span><span class="sxs-lookup"><span data-stu-id="85123-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="85123-159">`\\wsl$`를 통해 Linux 파일에 액세스 하면 WSL 배포판의 기본 사용자가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="85123-160">따라서 Linux 파일에 액세스 하는 모든 Windows 앱은 기본 사용자와 동일한 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="85123-161">새 파일 만들기</span><span class="sxs-lookup"><span data-stu-id="85123-161">Creating a new file</span></span>

<span data-ttu-id="85123-162">Windows에서 WSL 배포판 내에 새 파일을 만들 때 기본 umask 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="85123-163">기본 umask은 `022`, 즉 그룹 및 기타에 대 한 쓰기 권한을 제외한 모든 사용 권한을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="85123-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="85123-164">Linux에서 Linux 루트 파일 시스템의 파일에 액세스</span><span class="sxs-lookup"><span data-stu-id="85123-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="85123-165">Linux 루트 파일 시스템에서 생성, 수정 또는 액세스 되는 모든 파일은 umask를 새로 만든 파일에 적용 하는 것과 같은 표준 Linux 규칙을 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="85123-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="85123-166">파일 사용 권한 구성</span><span class="sxs-lookup"><span data-stu-id="85123-166">Configuring file permissions</span></span>

<span data-ttu-id="85123-167">Wsl의 탑재 옵션을 사용 하 여 Windows 드라이브 내에서 파일 사용 권한을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="85123-168">탑재 옵션을 사용 하 여 `umask`, `dmask` 및 `fmask` 사용 권한 마스크를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85123-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="85123-169">`umask` 모든 파일에 적용 되며 `dmask` 디렉터리에만 적용 되 고 `fmask` 파일에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="85123-170">이러한 권한 마스크는 파일에 적용 될 때 논리적 OR 작업을 통해 배치 됩니다. 예를 들어 `umask` 값이 `023`이 고 `fmask` 값이 `022` 이면 파일에 대 한 결과 권한 마스크는 `023`됩니다.</span><span class="sxs-lookup"><span data-stu-id="85123-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="85123-171">이 작업을 수행 하는 방법에 대 한 지침은 [' Linux 배포판 관리 '](./wsl-config.md) 문서 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85123-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

