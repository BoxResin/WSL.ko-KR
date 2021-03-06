---
title: WSL 2 설치
description: WSL 2의 설치 지침
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux용 windows 하위 시스템, windowssubsystem, ubuntu, debian, suse, windows 10, 설치
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520552"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2의 설치 지침

아래 비디오를 시청 하거나이 문서의 내용을 읽어 WSL2을 설치 하는 방법을 배울 수 있습니다. 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

WSL 2를 사용하여 설치하고 시작하려면 다음 단계를 완료합니다.

> WSL 2는 Windows 10 빌드 18917 이상 에서만 사용할 수 있습니다.

- WSL이 설치 되어 있는지 확인 하 고 ( [여기](./install-win10.md)에서 작업을 수행 하기 위한 지침을 찾을 수 있음) Windows 10 **빌드 18917** 이상을 실행 하 고 있는지 확인 합니다.
   - 빌드 18917 이상을 사용 하 고 있는지 확인 하려면 [Windows 참가자 프로그램에](https://insider.windows.com/en-us/) 참여 하 고 ' Fast ' 링 또는 ' 느림 ' 링을 선택 하세요. 
   - 명령 프롬프트를 열고 `ver` 명령을 실행 하 여 Windows 버전을 확인할 수 있습니다.
- '가상 머신 플랫폼' 옵션 구성 요소 사용
- 명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정
- Distro가 사용 중인 WSL 버전 확인

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>' 가상 컴퓨터 플랫폼 ' 옵션 구성 요소를 사용 하도록 설정 하 고 WSL이 사용 하도록 설정 되어 있는지 확인 합니다.

Linux 용 Windows 하위 시스템 및 가상 컴퓨터 플랫폼 선택적 구성 요소가 설치 되어 있는지 확인 해야 합니다. PowerShell에서 다음 명령을 실행 하 여이 작업을 수행할 수 있습니다. 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

두 구성 요소 설치를 완료 하려면 컴퓨터를 다시 시작 하세요.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>명령줄을 사용하여 WSL 2에 의해 지원되도록 Distro 설정

Linux 배포판이 설치 되어 있지 않은 경우 설치 하는 방법에 대 한 지침은 [Windows 10 문서에 설치](./install-win10.md#install-your-linux-distribution-of-choice) 페이지를 참조 하세요. 

배포판를 설정 하려면 다음을 실행 하세요. 

```
wsl --set-version <Distro> 2
```

`<Distro>`를 Distro의 실제 이름으로 대체해야 합니다. (`wsl -l` 명령을 사용하여 이를 찾을 수 있습니다.) 위와 동일한 명령을 실행하되 '2'를 '1'로 바꾸면 언제든지 WSL 1로 다시 변경할 수 있습니다.

또한 WSL 2를 기본 아키텍처로 설정하려는 경우 이 명령을 사용하여 수행할 수 있습니다.

```
wsl --set-default-version 2
```

이렇게 하면 설치한 새로운 Distro가 WSL 2 Distro로 초기화됩니다.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Distro가 사용 중인 WSL의 버전을 확인하는 작업으로 마무리합니다.

각 배포판가 사용 하는 WSL의 버전을 확인 하려면 다음 명령을 사용 합니다 (Windows 빌드 18917 이상 에서만 사용 가능).

`wsl --list --verbose` 또는 `wsl -l -v`

위에서 선택한 Distro는 이제 'version' 열 아래에 '2'를 표시해야 합니다. 이제 WSL 2 Distro를 자유롭게 사용할 수 있습니다. 

## <a name="troubleshooting"></a>문제 해결: 

다음은 WSL 2를 설치할 때 발생하는 관련 오류 및 권장되는 수정 사항입니다. 기타 일반적인 WSL 오류 및 해결 방법은 [WSL 문제 해결 페이지](troubleshooting.md)를 참조하세요.

* **0x80070003 오류 또는 0x80370102 오류로 인해 설치하지 못했습니다.**
    * 컴퓨터 BIOS 내에서 가상화를 사용하도록 설정했는지 확인합니다. 이 방법에 대한 지침은 컴퓨터마다 다르며, CPU 관련 옵션에 있을 가능성이 높습니다.
   
* **업그레이드 시도 중 오류: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Linux용 Windows 하위 시스템을 사용하도록 설정하고 Windows Build 버전 18917 이상을 사용하고 있는지 확인합니다. WSL을 실행하도록 하려면 관리자 권한(`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`)으로 Powershell 프롬프트에서 이 명령을 실행합니다. 전체 WSL 설치 지침은 [여기](./install-win10.md)에서 찾을 수 있습니다.

* **가상 디스크 시스템 제한으로 인해 요청한 작업을 완료할 수 없습니다. 가상 하드 디스크 파일은 압축 되지 않고 암호화 되지 않아야 하며 스파스 일 수 없습니다.**
    * 업데이트 된 정보에 대 한이 문제가 추적 되는 [Wsl Github 스레드 #4103](https://github.com/microsoft/WSL/issues/4103) 를 확인 하세요.

* **용어 ' wsl '은 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램의 이름으로 인식 되지 않습니다.** 
    * [Linux 용 Windows 하위 시스템 옵션 구성 요소가 설치](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled)되어 있는지 확인 합니다.<br> 또한 Arm64 장치를 사용 하 고 PowerShell에서이 명령을 실행 하는 경우이 오류가 표시 됩니다. 대신 [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)또는 명령 프롬프트에서 `wsl.exe`를 실행 합니다. 
