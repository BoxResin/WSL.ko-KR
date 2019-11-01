---
title: WSL 2 설치
description: WSL 2의 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: e3593aaf0e1c176cbeec2d3ba7d8eca1ede6b1ec
ms.sourcegitcommit: d74fab7469f4e589ab0bf4418be575381a3f72a0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2019
ms.locfileid: "73240367"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="c2a1d-104">WSL 2의 설치 지침</span><span class="sxs-lookup"><span data-stu-id="c2a1d-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="c2a1d-105">WSL 2를 사용하여 설치하고 시작하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="c2a1d-106">WSL 2는 Windows 10 빌드 18917 이상 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="c2a1d-107">WSL이 설치 되어 있는지 확인 하 고 ( [여기](./install-win10.md)에서 작업을 수행 하기 위한 지침을 찾을 수 있음) Windows 10 **빌드 18917** 이상을 실행 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="c2a1d-108">빌드 18917 이상을 사용 하 고 있는지 확인 하려면 [Windows 참가자 프로그램에](https://insider.windows.com/en-us/) 참여 하 고 ' Fast ' 링을 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="c2a1d-109">명령 프롬프트를 열고 `ver` 명령을 실행 하 여 Windows 버전을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="c2a1d-110">'가상 머신 플랫폼' 옵션 구성 요소 사용</span><span class="sxs-lookup"><span data-stu-id="c2a1d-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="c2a1d-111">명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정</span><span class="sxs-lookup"><span data-stu-id="c2a1d-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="c2a1d-112">Distro가 사용 중인 WSL 버전 확인</span><span class="sxs-lookup"><span data-stu-id="c2a1d-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="c2a1d-113">' 가상 컴퓨터 플랫폼 ' 옵션 구성 요소를 사용 하도록 설정 하 고 WSL이 사용 하도록 설정 되어 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="c2a1d-114">관리자 권한으로 PowerShell을 열어 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-114">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

<span data-ttu-id="c2a1d-115">그러면 Linux 선택적 구성 요소에 대 한 가상 컴퓨터 플랫폼과 Windows 하위 시스템이 모두 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-115">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="c2a1d-116">이러한 명령을 실행 한 후 컴퓨터를 다시 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-116">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="c2a1d-117">명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정</span><span class="sxs-lookup"><span data-stu-id="c2a1d-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="c2a1d-118">PowerShell에서 실행하고</span><span class="sxs-lookup"><span data-stu-id="c2a1d-118">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="c2a1d-119">`<Distro>`를 Distro의 실제 이름으로 대체해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-119">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="c2a1d-120">(`wsl -l` 명령을 사용하여 이를 찾을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="c2a1d-120">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="c2a1d-121">위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-121">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="c2a1d-122">또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-122">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="c2a1d-123">이렇게 하면 설치한 새로운 Distro가 WSL 2 Distro로 초기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-123">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="c2a1d-124">Distro가 사용 중인 WSL의 버전을 확인하는 작업으로 마무리합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-124">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="c2a1d-125">각 배포판가 사용 하는 WSL의 버전을 확인 하려면 다음 명령을 사용 합니다 (Windows 빌드 18917 이상 에서만 사용 가능).</span><span class="sxs-lookup"><span data-stu-id="c2a1d-125">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="c2a1d-126">`wsl --list --verbose` 또는 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="c2a1d-126">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="c2a1d-127">위에서 선택한 Distro는 이제 'version' 열 아래에 '2'를 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-127">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="c2a1d-128">이제 WSL 2 Distro를 자유롭게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-128">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="c2a1d-129">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="c2a1d-129">Troubleshooting:</span></span> 

<span data-ttu-id="c2a1d-130">다음은 WSL 2를 설치할 때 발생하는 관련 오류 및 권장되는 수정 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-130">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="c2a1d-131">기타 일반적인 WSL 오류 및 해결 방법은 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-131">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="c2a1d-132">**0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-132">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="c2a1d-133">컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-133">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="c2a1d-134">이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-134">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="c2a1d-135">**업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-135">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="c2a1d-136">Linux용 Windows 하위 시스템을 사용하도록 설정하고 Windows Build 버전 18917 이상을 사용하고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-136">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="c2a1d-137">WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 Powershell 프롬프트에서 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-137">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="c2a1d-138">전체 WSL 설치 지침은 [여기](./install-win10.md)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-138">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="c2a1d-139">**가상 디스크 시스템 제한으로 인해 요청한 작업을 완료할 수 없습니다. 가상 하드 디스크 파일은 압축 되지 않고 암호화 되지 않아야 하며 스파스 일 수 없습니다.**</span><span class="sxs-lookup"><span data-stu-id="c2a1d-139">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="c2a1d-140">업데이트 된 정보에 대 한이 문제가 추적 되는 [Wsl Github 스레드 #4103](https://github.com/microsoft/WSL/issues/4103) 를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2a1d-140">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>