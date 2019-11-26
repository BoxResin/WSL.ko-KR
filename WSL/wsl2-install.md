---
title: WSL 2 설치
description: WSL 2의 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a53e6a986813809d0c355b80b3fe3028adb21375
ms.sourcegitcommit: 73f4cc6ac9482ea9727f3cda0ec5c3572e164256
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2019
ms.locfileid: "74309054"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="e12de-104">WSL 2의 설치 지침</span><span class="sxs-lookup"><span data-stu-id="e12de-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="e12de-105">WSL 2를 사용하여 설치하고 시작하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="e12de-106">WSL 2는 Windows 10 빌드 18917 이상 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="e12de-107">WSL이 설치 되어 있는지 확인 하 고 ( [여기](./install-win10.md)에서 작업을 수행 하기 위한 지침을 찾을 수 있음) Windows 10 **빌드 18917** 이상을 실행 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="e12de-108">빌드 18917 이상을 사용 하 고 있는지 확인 하려면 [Windows 참가자 프로그램에](https://insider.windows.com/en-us/) 참여 하 고 ' Fast ' 링을 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="e12de-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="e12de-109">명령 프롬프트를 열고 `ver` 명령을 실행 하 여 Windows 버전을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="e12de-110">'가상 머신 플랫폼' 옵션 구성 요소 사용</span><span class="sxs-lookup"><span data-stu-id="e12de-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="e12de-111">명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정</span><span class="sxs-lookup"><span data-stu-id="e12de-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="e12de-112">Distro가 사용 중인 WSL 버전 확인</span><span class="sxs-lookup"><span data-stu-id="e12de-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="e12de-113">' 가상 컴퓨터 플랫폼 ' 옵션 구성 요소를 사용 하도록 설정 하 고 WSL이 사용 하도록 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="e12de-114">Linux 용 Windows 하위 시스템 및 가상 컴퓨터 플랫폼 선택적 구성 요소가 설치 되어 있는지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="e12de-115">PowerShell에서 다음 명령을 실행 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-115">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="e12de-116">두 구성 요소 설치를 완료 하려면 컴퓨터를 다시 시작 하세요.</span><span class="sxs-lookup"><span data-stu-id="e12de-116">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="e12de-117">명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정</span><span class="sxs-lookup"><span data-stu-id="e12de-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="e12de-118">Linux 배포판이 설치 되어 있지 않은 경우 설치 하는 방법에 대 한 지침은 [Windows 10 문서에 설치](./install-win10.md#install-your-linux-distribution-of-choice) 페이지를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e12de-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="e12de-119">배포판를 설정 하려면 다음을 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e12de-119">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="e12de-120">`<Distro>`를 Distro의 실제 이름으로 대체해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-120">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="e12de-121">(`wsl -l` 명령을 사용하여 이를 찾을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="e12de-121">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="e12de-122">위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-122">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="e12de-123">또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-123">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="e12de-124">이렇게 하면 설치한 새로운 Distro가 WSL 2 Distro로 초기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-124">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="e12de-125">Distro가 사용 중인 WSL의 버전을 확인하는 작업으로 마무리합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-125">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="e12de-126">각 배포판가 사용 하는 WSL의 버전을 확인 하려면 다음 명령을 사용 합니다 (Windows 빌드 18917 이상 에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="e12de-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="e12de-127">`wsl --list --verbose` 또는 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="e12de-127">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="e12de-128">위에서 선택한 Distro는 이제 'version' 열 아래에 '2'를 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-128">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="e12de-129">이제 WSL 2 Distro를 자유롭게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-129">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="e12de-130">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="e12de-130">Troubleshooting:</span></span> 

<span data-ttu-id="e12de-131">다음은 WSL 2를 설치할 때 발생하는 관련 오류 및 권장되는 수정 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-131">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="e12de-132">기타 일반적인 WSL 오류 및 해결 방법은 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e12de-132">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="e12de-133">**0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**</span><span class="sxs-lookup"><span data-stu-id="e12de-133">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="e12de-134">컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-134">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="e12de-135">이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-135">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="e12de-136">**업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="e12de-136">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="e12de-137">Linux용 Windows 하위 시스템을 사용하도록 설정하고 Windows Build 버전 18917 이상을 사용하고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-137">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="e12de-138">WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 Powershell 프롬프트에서 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-138">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="e12de-139">전체 WSL 설치 지침은 [여기](./install-win10.md)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-139">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="e12de-140">**가상 디스크 시스템 제한으로 인해 요청한 작업을 완료할 수 없습니다. 가상 하드 디스크 파일은 압축 되지 않고 암호화 되지 않아야 하며 스파스 일 수 없습니다.**</span><span class="sxs-lookup"><span data-stu-id="e12de-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="e12de-141">업데이트 된 정보에 대 한이 문제가 추적 되는 [Wsl Github 스레드 #4103](https://github.com/microsoft/WSL/issues/4103) 를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="e12de-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="e12de-142">**용어 ' wsl '은 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램의 이름으로 인식 되지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="e12de-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="e12de-143">[Linux 용 Windows 하위 시스템 옵션 구성 요소가 설치](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled)되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="e12de-144">또한 Arm64 장치를 사용 하 고 PowerShell에서이 명령을 실행 하는 경우이 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="e12de-145">대신 [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)또는 명령 프롬프트에서 `wsl.exe`를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e12de-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
