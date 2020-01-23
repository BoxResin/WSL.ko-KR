---
title: WSL 이전 Windows 버전에서 사용자 계정 업데이트
description: Linux 용 Windows 하위 시스템을 사용 하 여 Linux 사용자 계정을 업데이트 하기 위한 이전 Windows 버전에 대 한 참조입니다.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 406158d769c4b465b6168d7cca45b48ff1f201fe
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520842"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a><span data-ttu-id="86fc9-103">WSL 이전 Windows 버전에서 사용자 계정 업데이트</span><span class="sxs-lookup"><span data-stu-id="86fc9-103">WSL User Account updates on Previous Windows Versions</span></span>

<span data-ttu-id="86fc9-104">이 콘텐츠는 Linux 용 하위 시스템을 지 원하는 이전 버전의 Windows 운영 체제 사용자를 위해 보관 되며 Linux 사용자 계정 업데이트에 대 한 지원이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-104">This content is archived for users of earlier versions of Windows operating system that support the subsystem for Linux and need support with updating Linux user accounts.</span></span>

<span data-ttu-id="86fc9-105">최신 설명서는 Linux 용 [Windows 하위 시스템에 대 한 사용자 계정](../user-support.md)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86fc9-105">For current documentation, see [User Accounts for Windows Subsystem for Linux](../user-support.md).</span></span>

### <a name="for-creators-update-version-of-windows-and-earlier"></a><span data-ttu-id="86fc9-106">Windows 및 이전 버전의 작성자 업데이트</span><span class="sxs-lookup"><span data-stu-id="86fc9-106">For Creators Update version of Windows and earlier</span></span>

<span data-ttu-id="86fc9-107">Windows 10 크리에이터스 업데이트를 실행하는 경우 다음 명령을 실행하여 기본 Bash 사용자를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-107">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="86fc9-108">기본 사용자를 `root`로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-108">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="86fc9-109">지금 `bash.exe`를 실행하여 `root`로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-109">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="86fc9-110">배포의 암호 명령을 사용하여 암호를 다시 설정하고 Linux 콘솔을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-110">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="86fc9-111">Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-111">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="86fc9-112">Fall Creators Update 및 이후 버전의 경우</span><span class="sxs-lookup"><span data-stu-id="86fc9-112">For Fall Creators Update and later</span></span>

<span data-ttu-id="86fc9-113">특정 배포에 사용할 수 있는 명령을 확인하려면 `[distro.exe] /?`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-113">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="86fc9-114">예를 들어 Ubuntu가 설치된 경우 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-114">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="86fc9-115">Ubuntu를 사용한 단계별 지침은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-115">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="86fc9-116">CMD를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-116">Open CMD</span></span>
1. <span data-ttu-id="86fc9-117">기본 Linux 사용자를 `root`로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-117">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="86fc9-118">Linux 배포(`ubuntu`)를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-118">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="86fc9-119">자동으로 `root`로 로그인됩니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-119">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="86fc9-120">`passwd` 명령을 사용하여 암호를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-120">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="86fc9-121">Windows CMD에서 기본 사용자를 일반 Linux 사용자 계정으로 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86fc9-121">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```
