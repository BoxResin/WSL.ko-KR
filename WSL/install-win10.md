---
title: Windows 10에 WSL(Linux용 Windows 하위 시스템) 설치
description: Linux용 Windows 하위 시스템을 Windows 10에 설치하는 방법에 대한 지침입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, Debian, Suse, Windows 10, 설치
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122772"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="21efe-104">Windows 10에 Linux용 Windows 하위 시스템 설치 가이드</span><span class="sxs-lookup"><span data-stu-id="21efe-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="21efe-105">Linux용 Windows 하위 시스템 설치</span><span class="sxs-lookup"><span data-stu-id="21efe-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="21efe-106">WSL용 Linux 배포판을 설치하려면 먼저 선택적인 "Linux용 Windows 하위 시스템" 기능을 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="21efe-107">PowerShell을 관리자 권한으로 열어 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="21efe-108">메시지가 표시되면 컴퓨터를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="21efe-109">선택한 Linux 배포 설치</span><span class="sxs-lookup"><span data-stu-id="21efe-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="21efe-110">기본 설정 배포판을 다운로드하여 설치하려면 다음 세 가지 옵션 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="21efe-111">Microsoft Store에서 다운로드 및 설치(아래 참조)</span><span class="sxs-lookup"><span data-stu-id="21efe-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="21efe-112">명령줄/스크립트에서 다운로드 및 설치([수동 설치 지침 참조](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="21efe-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="21efe-113">다운로드 및 수동으로 압축을 푼 후 설치(Windows Server의 경우 - [지침](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="21efe-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="21efe-114">Windows 10 Fall Creators Update 이상: Microsoft Store에서 설치</span><span class="sxs-lookup"><span data-stu-id="21efe-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="21efe-115">이 섹션은 Windows 빌드 16215 이상에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="21efe-116">다음 단계에 따라 [빌드를 확인](troubleshooting.md#check-your-build-number)하세요.</span><span class="sxs-lookup"><span data-stu-id="21efe-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="21efe-117">Microsoft Store를 열고 즐겨찾는 Linux 배포를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store에서 Linux 배포판 보기](media/store.png)

    <span data-ttu-id="21efe-119">각 배포에 대한 Microsoft Store 페이지를 여는 링크는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="21efe-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="21efe-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="21efe-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="21efe-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="21efe-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="21efe-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="21efe-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="21efe-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="21efe-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="21efe-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="21efe-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="21efe-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="21efe-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="21efe-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="21efe-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="21efe-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="21efe-128">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="21efe-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="21efe-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="21efe-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="21efe-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="21efe-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="21efe-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="21efe-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="21efe-132">배포판의 페이지에서 "가져오기"를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-132">From the distro's page, select "Get"</span></span>

    ![Microsoft Store에서 Linux 배포판 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="21efe-134">배포판의 초기화 완료</span><span class="sxs-lookup"><span data-stu-id="21efe-134">Complete initialization of your distro</span></span>
<span data-ttu-id="21efe-135">이제 Linux 배포판이 설치되었으므로 새 배포판 인스턴스를 사용하려면 먼저 [초기화](initialize-distro.md)해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="21efe-136">문제 해결:</span><span class="sxs-lookup"><span data-stu-id="21efe-136">Troubleshooting:</span></span> 

<span data-ttu-id="21efe-137">관련 오류 및 제안된 수정 사항은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="21efe-138">다른 일반적인 오류 및 해결 방법에 대해서는 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21efe-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="21efe-139">**0x80070003 오류로 인한 설치 실패**</span><span class="sxs-lookup"><span data-stu-id="21efe-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="21efe-140">Linux용 Windows 하위 시스템은 시스템 드라이브(일반적으로 `C:` 드라이브)에서만 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="21efe-141">배포판이 시스템 드라이브에 저장되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="21efe-142">**설정** -> **스토리지** -> **더 많은 스토리지 설정을 차례로 엽니다. 새 콘텐츠가 저장된 위치를 변경합니다.** 
    ![C: 드라이브에 앱을 설치하기 위한 시스템 설정에 대한 그림](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="21efe-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="21efe-143">**0x8007019e 오류로 인한 WslRegisterDistribution 실패**</span><span class="sxs-lookup"><span data-stu-id="21efe-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="21efe-144">선택적인 Linux용 Windows 하위 시스템 구성 요소가 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="21efe-145">제어판 프로그램 및 기능 Windows 기능 사용/사용 안 함 을 차례로 열어 Linux용 Windows 하위 시스템 을 선택하거나 이 문서의 시작 부분에서 설명한 PowerShell cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="21efe-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
