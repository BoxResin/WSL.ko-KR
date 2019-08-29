---
title: WSL 2 설치
description: WSL 2의 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 6b7ed18480ea88200d00b67a3a6dc859947397db
ms.sourcegitcommit: 6f10b40f6199538c8eedf6301f02b7d70ead3fe7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70117830"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="902a8-104">WSL 2의 설치 지침</span><span class="sxs-lookup"><span data-stu-id="902a8-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="902a8-105">WSL 2를 사용하여 설치하고 시작하려면 다음 단계를 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="902a8-106">WSL이 설치 되어 있는지 확인 하 고 ( [여기](./install-win10.md)에서 작업을 수행 하기 위한 지침을 찾을 수 있음) Windows 10 빌드 18917 이상을 실행 하 고 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
   - <span data-ttu-id="902a8-107">빌드 18917 이상을 사용 하 고 있는지 확인 하려면 [Windows 참가자 프로그램에](https://insider.windows.com/en-us/) 참여 하 고 ' Fast ' 링을 선택 하세요.</span><span class="sxs-lookup"><span data-stu-id="902a8-107">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="902a8-108">명령 프롬프트를 열고 `ver` 명령을 실행 하 여 Windows 버전을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-108">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="902a8-109">'가상 머신 플랫폼' 옵션 구성 요소 사용</span><span class="sxs-lookup"><span data-stu-id="902a8-109">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="902a8-110">명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정</span><span class="sxs-lookup"><span data-stu-id="902a8-110">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="902a8-111">Distro가 사용 중인 WSL 버전 확인</span><span class="sxs-lookup"><span data-stu-id="902a8-111">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="902a8-112">'가상 머신 플랫폼' 옵션 구성 요소 사용</span><span class="sxs-lookup"><span data-stu-id="902a8-112">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="902a8-113">관리자 권한으로 PowerShell을 열어 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-113">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="902a8-114">이러한 변경 내용을 사용한 후에는 컴퓨터를 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-114">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="902a8-115">명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정</span><span class="sxs-lookup"><span data-stu-id="902a8-115">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="902a8-116">PowerShell에서 실행하고</span><span class="sxs-lookup"><span data-stu-id="902a8-116">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="902a8-117">`<Distro>`를 Distro의 실제 이름으로 대체해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-117">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="902a8-118">(`wsl -l` 명령을 사용하여 이를 찾을 수 있습니다.)</span><span class="sxs-lookup"><span data-stu-id="902a8-118">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="902a8-119">위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-119">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="902a8-120">또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-120">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="902a8-121">이렇게 하면 설치한 새로운 Distro가 WSL 2 Distro로 초기화됩니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-121">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="902a8-122">Distro가 사용 중인 WSL의 버전을 확인하는 작업으로 마무리합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-122">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="902a8-123">Distro가 사용 중인 WSL의 버전을 확인하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-123">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="902a8-124">`wsl --list --verbose` 또는 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="902a8-124">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="902a8-125">위에서 선택한 Distro는 이제 'version' 열 아래에 '2'를 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-125">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="902a8-126">이제 WSL 2 Distro를 자유롭게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-126">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="902a8-127">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="902a8-127">Troubleshooting:</span></span> 

<span data-ttu-id="902a8-128">다음은 WSL 2를 설치할 때 발생하는 관련 오류 및 권장되는 수정 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-128">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="902a8-129">기타 일반적인 WSL 오류 및 해결 방법은 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="902a8-129">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="902a8-130">**0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**</span><span class="sxs-lookup"><span data-stu-id="902a8-130">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="902a8-131">컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-131">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="902a8-132">이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-132">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="902a8-133">**업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="902a8-133">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="902a8-134">Linux용 Windows 하위 시스템을 사용하도록 설정하고 Windows Build 버전 18917 이상을 사용하고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-134">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="902a8-135">WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 Powershell 프롬프트에서 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-135">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="902a8-136">전체 WSL 설치 지침은 [여기](./install-win10.md)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="902a8-136">You can find the full WSL install instructions [here](./install-win10.md).</span></span>