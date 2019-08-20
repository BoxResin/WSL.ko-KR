---
title: Linux 용 Windows 하위 시스템 명령 참조
description: Linux 용 Windows 하위 시스템을 관리 하는 명령 목록
keywords: BashOnWindows, bash, wsl, windows, linux 용 windows 하위 시스템, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 018b02b43e859476f7ee38f54df8efa0ca0e652b
ms.sourcegitcommit: 62c49d435a91f2e390c3c495f3e09e62b5ada13c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69578844"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="9f154-104">Linux 용 Windows 하위 시스템에 대 한 명령 참조</span><span class="sxs-lookup"><span data-stu-id="9f154-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="9f154-105">Linux 용 Windows 하위 시스템을 조작 하는 가장 좋은 방법은 `wsl.exe` 명령을 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="9f154-106">다음은 Windows 버전 1903를 사용 하 `wsl.exe` 는 경우 모든 옵션을 포함 하는 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="9f154-107">사용 하 여`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="9f154-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="9f154-108">Linux 이진 파일을 실행 하기 위한 인수</span><span class="sxs-lookup"><span data-stu-id="9f154-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="9f154-109">**인수 없는**</span><span class="sxs-lookup"><span data-stu-id="9f154-109">**Without arguments**</span></span>

  <span data-ttu-id="9f154-110">명령줄이 제공 되지 않은 경우 wsl .exe는 기본 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="9f154-111">**--exec,-e \<명령줄 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="9f154-112">기본 Linux 셸을 사용 하지 않고 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="9f154-113">나머지 명령줄을 있는 그대로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="9f154-114">위의 명령도 다음 옵션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="9f154-115">**--분포,-d \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="9f154-116">지정 된 분포를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-116">Run the specified distribution.</span></span>

* <span data-ttu-id="9f154-117">**--사용자,-u \<사용자 이름 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="9f154-118">지정 된 사용자로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="9f154-119">Linux 용 Windows 하위 시스템을 관리 하기 위한 인수</span><span class="sxs-lookup"><span data-stu-id="9f154-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="9f154-120">**--배포판 \<> \<파일 이름 >를 내보냅니다.**</span><span class="sxs-lookup"><span data-stu-id="9f154-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="9f154-121">배포를 tar 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="9f154-122">표준 출력의 경우 파일 이름으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="9f154-123">**--import \<배포판 > \<InstallLocation > \<FileName >**</span><span class="sxs-lookup"><span data-stu-id="9f154-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="9f154-124">지정 된 tar 파일을 새 배포로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="9f154-125">표준 입력의 경우 파일 이름으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="9f154-126">**--list,-l [Options]**</span><span class="sxs-lookup"><span data-stu-id="9f154-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="9f154-127">분포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-127">Lists distributions.</span></span>

  <span data-ttu-id="9f154-128">옵션:</span><span class="sxs-lookup"><span data-stu-id="9f154-128">Options:</span></span>
  * <span data-ttu-id="9f154-129">**--모두**</span><span class="sxs-lookup"><span data-stu-id="9f154-129">**--all**</span></span>
      
    <span data-ttu-id="9f154-130">현재 설치 또는 제거 되는 배포를 포함 하 여 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="9f154-131">**--실행 중**</span><span class="sxs-lookup"><span data-stu-id="9f154-131">**--running**</span></span>
      
    <span data-ttu-id="9f154-132">현재 실행 중인 배포만 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="9f154-133">**--set-기본값,-s \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-134">분포를 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="9f154-135">**--terminate,-t \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-136">지정 된 분포를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="9f154-137">**--배포판 \<> 등록 취소**</span><span class="sxs-lookup"><span data-stu-id="9f154-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-138">배포를 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="9f154-139">**--도움말** 사용 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="9f154-140">추가 명령</span><span class="sxs-lookup"><span data-stu-id="9f154-140">Additional Commands</span></span>

<span data-ttu-id="9f154-141">또한 Linux 용 Windows 하위 시스템을 조작 하는 기록 명령도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="9f154-142">해당 기능은에 포함 `wsl.exe`되어 있지만 여전히 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="9f154-143">이 명령을 사용 하 여 WSL 배포를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="9f154-144">다음은 해당 옵션의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-144">Below is a list of its options.</span></span>

<span data-ttu-id="9f154-145">사용 하 여`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="9f154-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="9f154-146">인수</span><span class="sxs-lookup"><span data-stu-id="9f154-146">Arguments</span></span>
* <span data-ttu-id="9f154-147">**/l,/list [Options]**</span><span class="sxs-lookup"><span data-stu-id="9f154-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="9f154-148">등록 된 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="9f154-149">옵션:</span><span class="sxs-lookup"><span data-stu-id="9f154-149">Options:</span></span>
    * <span data-ttu-id="9f154-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="9f154-150">**/all**</span></span>
    
      <span data-ttu-id="9f154-151">필요에 따라 현재 설치 또는 제거 되는 배포를 포함 하 여 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="9f154-152">**/실행 중**</span><span class="sxs-lookup"><span data-stu-id="9f154-152">**/running**</span></span>
      
      <span data-ttu-id="9f154-153">현재 실행 중인 배포만 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="9f154-154">**/s,/setdefault \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-155">분포를 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="9f154-156">**/t,/종료 \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-157">분포를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-157">Terminates the distribution.</span></span>

* <span data-ttu-id="9f154-158">**/u,/unregister \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-159">배포를 등록 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="9f154-160">**/upgrade \<배포판 >**</span><span class="sxs-lookup"><span data-stu-id="9f154-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="9f154-161">배포를 WslFs 파일 시스템 형식으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="9f154-162">이 명령은 bash 셸을 시작 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="9f154-163">다음은이 명령에서 사용할 수 있는 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="9f154-164">사용 하 여`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="9f154-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="9f154-165">**지정 된 옵션이 없습니다.**</span><span class="sxs-lookup"><span data-stu-id="9f154-165">**No Option given**</span></span>
  
  <span data-ttu-id="9f154-166">현재 디렉터리에서 Bash 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="9f154-167">Bash 셸이 설치 되어 있지 않으면 자동으로 실행 됩니다.`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="9f154-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="9f154-168">`bash ~`사용자의 홈 디렉터리에 bash 셸을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="9f154-169">실행과 `cd ~`비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="9f154-170">**-c "\<명령 >"**</span><span class="sxs-lookup"><span data-stu-id="9f154-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="9f154-171">명령을 실행 하 고 출력을 출력 한 다음 Windows 명령 프롬프트로 다시 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="9f154-172">예: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="9f154-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="9f154-173">사용 되지 않는 명령</span><span class="sxs-lookup"><span data-stu-id="9f154-173">Deprecated Commands</span></span>

<span data-ttu-id="9f154-174">는 `lxrun.exe` Linux 용 Windows 하위 시스템을 설치 하 고 관리 하는 데 사용 되는 첫 번째 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="9f154-175">Windows 10 1803 이상에서 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="9f154-176">명령을 `lxrun.exe` 사용 하 여 [Linux 용 Windows 하위 시스템 (wsl)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) 을 직접 조작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="9f154-177">이러한 명령은 `\Windows\System32` 디렉터리에 설치 되며, Windows 명령 프롬프트 또는 PowerShell 내에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="9f154-178">명령</span><span class="sxs-lookup"><span data-stu-id="9f154-178">Command</span></span>                     | <span data-ttu-id="9f154-179">설명</span><span class="sxs-lookup"><span data-stu-id="9f154-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="9f154-180">Lxrun 명령은 WSL 인스턴스를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="9f154-181">다운로드 및 설치 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="9f154-182">모든 프롬프트를 무시 하도록 **/y** 를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="9f154-183">확인 메시지가 자동으로 수락 되 고 기본 사용자가 root로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="9f154-184">Ubuntu 이미지를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="9f154-185">기본적으로 사용자의 Ubuntu 홈 디렉터리는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="9f154-186">자동으로 확인 메시지를 수락 하도록 **/y** 를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="9f154-187">**/full** 사용자의 Ubuntu 홈 디렉터리를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="9f154-188">Ubuntu 사용자에 대 한 기본 Bash를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="9f154-189">지정 된 사용자가 없는 경우 암호를 입력 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="9f154-190">자세한 내용은을 참조 https://aka.ms/wslusers 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f154-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="9f154-191">**/y** 암호에 대 한 promping를 무시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="9f154-192">사용자가 암호 없이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="9f154-193">하위 시스템의 패키지 인덱스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f154-193">Updates the subsystem's package index</span></span>          |
