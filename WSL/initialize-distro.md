---
title: 새 WSL Linux 배포판 초기화
description: WSL용 Linux 배포판이 설치되면 여기에 나와 있는 간단한 단계에 따라 초기화를 완료합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122711"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="dcb55-104">새로 설치된 배포판 초기화</span><span class="sxs-lookup"><span data-stu-id="dcb55-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="dcb55-105">배포판을 다운로드하여 설치한 후에는 새 배포판의 초기화를 완료해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="dcb55-106">배포판 시작</span><span class="sxs-lookup"><span data-stu-id="dcb55-106">Launch a distro</span></span>
<span data-ttu-id="dcb55-107">새로 설치한 배포판의 초기화를 완료하려면 새 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="dcb55-108">이 작업은 Microsoft Store 앱에서 "시작" 단추를 클릭하거나 시작 메뉴에서 배포판을 시작하여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="dcb55-109">팁: 가장 자주 사용하는 배포판을 시작 메뉴 및/또는 작업 표시줄에 고정하는 것이 좋습니다!</span><span class="sxs-lookup"><span data-stu-id="dcb55-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![시작 메뉴에서 배포판 시작](media/start-menu.png)

> <span data-ttu-id="dcb55-111">Windows 서버의 경우 배포판의 설치 폴더에서 배포판의 시작 관리자 실행 파일인 `<distro>.exe`를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="dcb55-112">새로 설치한 배포판이 처음 실행되면 콘솔 창이 열리고, 설치가 완료될 때까지 1~2분 정도 기다리라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="dcb55-113">이 설치의 마지막 단계에서 배포판의 파일이 압축 해제되고 PC에 저장되어 사용할 준비가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="dcb55-114">이 경우 PC의 스토리지 디바이스 성능에 따라 약 1분 이상이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="dcb55-115">이 초기 설치 단계는 배포판을 새로 설치하는 경우에만 필요하며, 이후의 모든 시작에는 1초 미만이 걸립니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="dcb55-116">새 Linux 사용자 계정 설정</span><span class="sxs-lookup"><span data-stu-id="dcb55-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="dcb55-117">설치가 완료되면 새 사용자 계정(및 해당 암호)을 만들라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows 콘솔에서 Ubuntu 압축 풀기](media/UbuntuInstall.png)

<span data-ttu-id="dcb55-119">이 사용자 계정은 배포판을 시작할 때 기본적으로 로그인되는 관리자가 아닌 일반 사용자를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="dcb55-120">원하는 사용자 이름과 암호를 선택할 수 있으며, Windows 사용자 이름과는 관련이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="dcb55-121">새 배포판 인스턴스를 열면 암호를 입력하라는 메시지가 표시되지 않지만, **`sudo`를 사용하여 프로세스를 관리자 권한으로 실행하는 경우** 암호를 입력해야 하므로 쉽게 기억할 수 있는 암호를 선택해야 합니다!</span><span class="sxs-lookup"><span data-stu-id="dcb55-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="dcb55-122">자세한 내용은 [사용자 지원](user-support.md) 페이지를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcb55-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="dcb55-123">배포판 패키지 업데이트 및 업그레이드</span><span class="sxs-lookup"><span data-stu-id="dcb55-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="dcb55-124">대부분의 배포판에는 비어 있거나 최소한의 패키지 카탈로그가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="dcb55-125">배포판의 기본 설정 패키지 관리자를 사용하여 정기적으로 패키지 카탈로그를 업데이트하고 설치된 패키지를 업그레이드하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="dcb55-126">Debian/Ubuntu에서는 apt를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="dcb55-127">Windows에서는 Linux 배포판을 자동으로 업데이트하거나 업그레이드하지 않습니다. 이는 Linux 사용자가 직접 제어하는 것을 선호하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="dcb55-128">작업을 완료했습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-128">You're done!</span></span> <span data-ttu-id="dcb55-129">WSL에서 새 Linux 배포판을 사용해 보세요!</span><span class="sxs-lookup"><span data-stu-id="dcb55-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="dcb55-130">WSL에 대해 자세히 알아보려면 다른 [WSL 문서](https://aka.ms/wsldocs) 또는 [WSL 학습 리소스 페이지](https://aka.ms/learnwsl)를 검토하세요.</span><span class="sxs-lookup"><span data-stu-id="dcb55-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![WSL에서 Linux 사용](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="dcb55-132">문제 해결</span><span class="sxs-lookup"><span data-stu-id="dcb55-132">Troubleshooting</span></span>

<span data-ttu-id="dcb55-133">관련 오류 및 제안된 수정 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="dcb55-134">다른 일반적인 오류 및 해결 방법에 대해서는 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcb55-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="dcb55-135">**0x8007007e 오류로 인한 설치 실패** 이 오류는 시스템에서 스토어의 Linux를 지원하지 않을 때 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="dcb55-136">다음 사항을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="dcb55-136">Make sure that:</span></span>
> * <span data-ttu-id="dcb55-137">Windows 빌드 16215 이상을 실행하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="dcb55-138">[빌드를 확인](troubleshooting.md#check-your-build-number)하세요.</span><span class="sxs-lookup"><span data-stu-id="dcb55-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="dcb55-139">Linux용 Windows 하위 시스템의 선택적 구성 요소가 사용하도록 설정되어 있고 컴퓨터가 다시 시작되었습니다.</span><span class="sxs-lookup"><span data-stu-id="dcb55-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="dcb55-140">[WSL이 사용하도록 설정되어 있는지 확인](troubleshooting.md#confirm-wsl-is-enabled)하세요.</span><span class="sxs-lookup"><span data-stu-id="dcb55-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
