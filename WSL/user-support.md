---
title: Linux 사용자 계정 및 권한
description: Linux용 Windows 하위 시스템의 사용자 계정 및 권한 관리에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, 사용자 계정
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d8434283e459ae25637fac0c0b1877ca07d9a255
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269707"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="3e0e7-104">Linux용 Windows 하위 시스템에 대한 사용자 계정 및 권한</span><span class="sxs-lookup"><span data-stu-id="3e0e7-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="3e0e7-105">WSL에서 새 Linux 배포를 설정하는 첫 번째 단계는 Linux 사용자를 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="3e0e7-106">처음 만든 사용자 계정은 다음과 같은 몇 가지 특수 특성을 사용하여 자동으로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="3e0e7-107">기본 사용자이며, 시작할 때 자동으로 로그인됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="3e0e7-108">기본적으로 Linux 관리자(sudo 그룹의 멤버)입니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="3e0e7-109">Linux용 Windows 하위 시스템에서 실행되는 각 Linux 배포에는 고유한 Linux 사용자 계정과 암호가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="3e0e7-110">배포를 추가하거나, 다시 설치하거나, 다시 설정할 때마다 Linux 사용자 계정을 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="3e0e7-111">Linux 사용자 계정은 배포마다 독립적일 뿐만 아니라 Windows 사용자 계정과도 독립적입니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="3e0e7-112">Linux 암호 재설정</span><span class="sxs-lookup"><span data-stu-id="3e0e7-112">Resetting your Linux password</span></span>

<span data-ttu-id="3e0e7-113">Linux 사용자 계정에 대한 액세스 권한이 있고 현재 암호를 알고 있는 경우 해당 배포의 Linux 암호 재설정 도구(대부분 `passwd`)를 사용하여 암호를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="3e0e7-114">이 도구가 옵션이 아닌 경우 배포에 따라 기본 사용자를 다시 설정하여 암호를 다시 설정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="3e0e7-115">WSL에서는 WSL을 시작할 때 자동으로 로그인되는 사용자 계정을 식별하는 기본 사용자 태그를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="3e0e7-116">대부분의 배포에는 기본 사용자를 루트로 설정하고 암호가 설정되지 않은 루트 사용자도 설정하는 명령이 포함되어 있으므로 기본 사용자를 루트로 변경하는 것은 암호 재설정과 같은 작업에 유용한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="3e0e7-117">크리에이터스 업데이트 및 이전 버전의 경우</span><span class="sxs-lookup"><span data-stu-id="3e0e7-117">For Creators Update and earlier</span></span>
<span data-ttu-id="3e0e7-118">Windows 10 크리에이터스 업데이트를 실행하는 경우 다음 명령을 실행하여 기본 Bash 사용자를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="3e0e7-119">기본 사용자를 `root`로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="3e0e7-120">지금 `bash.exe`를 실행하여 `root`로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="3e0e7-121">배포의 암호 명령을 사용하여 암호를 다시 설정하고 Linux 콘솔을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="3e0e7-122">Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="3e0e7-123">Fall Creators Update 및 이후 버전의 경우</span><span class="sxs-lookup"><span data-stu-id="3e0e7-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="3e0e7-124">특정 배포에 사용할 수 있는 명령을 확인하려면 `[distro.exe] /?`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="3e0e7-125">예를 들어 Ubuntu가 설치된 경우 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="3e0e7-126">Ubuntu를 사용한 단계별 지침은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="3e0e7-127">CMD를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-127">Open CMD</span></span>
1. <span data-ttu-id="3e0e7-128">기본 Linux 사용자를 `root`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="3e0e7-129">Linux 배포(`ubuntu`)를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="3e0e7-130">자동으로 `root`로 로그인됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="3e0e7-131">`passwd` 명령을 사용하여 암호를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="3e0e7-132">Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="3e0e7-133">권한</span><span class="sxs-lookup"><span data-stu-id="3e0e7-133">Permissions</span></span>

<span data-ttu-id="3e0e7-134">WSL의 권한과 관련하여 다음 두 가지 중요한 개념을 명심해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="3e0e7-135">Windows 권한 모델은 Windows 리소스에 대한 프로세스의 권한을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="3e0e7-136">Linux 권한 모델은 Linux 리소스에 대한 프로세스의 권한을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="3e0e7-137">WSL에서 Linux를 실행하는 경우 Linux는 이를 시작하는 프로세스와 동일한 Windows 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="3e0e7-138">Linux는 다음 두 가지 권한 수준 중 하나로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="3e0e7-139">보통(관리자 권한 없음): Linux가 로그인한 사용자의 권한으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="3e0e7-140">관리자 권한/관리자: Linux가 관리자 권한/관리자 Windows 권한으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="3e0e7-141">관리자 권한으로 실행되는 프로세스는 시스템 수준 설정 및 시스템 수준의 보호된 데이터에 액세스하여 수정할 수 있으므로(이에 따라 손상시킬 수 있음) Windows 또는 Linux 애플리케이션/도구/셸인지 여부와 관계없이 반드시 필요한 경우가 아니면 관리자 권한으로 실행되는 프로세스를 **시작하지 마세요**!</span><span class="sxs-lookup"><span data-stu-id="3e0e7-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="3e0e7-142">위의 Windows 권한은 Linux 인스턴스 내의 권한과는 독립적입니다. Linux "루트 권한"은 Linux 환경 및 파일 시스템 내의 사용자의 권한에만 영향을 주며, 부여된 Windows 권한에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="3e0e7-143">따라서 Linux 프로세스를 루트로(예: `sudo`를 통해) 실행하면 Linux 환경 내에서 해당 프로세스 관리자 권한만 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="3e0e7-144">**예제:**   </span><span class="sxs-lookup"><span data-stu-id="3e0e7-144">**Example:**  </span></span>  
<span data-ttu-id="3e0e7-145">Windows 관리자 권한이 있는 Bash 세션은 `cd /mnt/c/Users/Administrator`에 액세스할 수 있지만, 관리자 권한이 없는 Bash 세션은 "권한 거부" 오류를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="3e0e7-146">Windows 내의 권한은 Windows에서 관리하므로 Linux에서 `sudo cd /mnt/c/Users/Administrator`를 입력하더라도 관리자의 디렉터리에 대한 액세스 권한이 부여되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="3e0e7-147">Linux 권한 모델은 사용자에게 현재 Linux 사용자 기반의 권한이 있는 Linux 환경 내에서 중요합니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="3e0e7-148">**예제:**</span><span class="sxs-lookup"><span data-stu-id="3e0e7-148">**Example:**</span></span>  
<span data-ttu-id="3e0e7-149">sudo 그룹의 사용자가 `sudo apt update`를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e0e7-149">A user in the sudo group may run `sudo apt update`.</span></span>
