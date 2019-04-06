---
title: Windows 10에서 Linux (WSL) 용 Windows 하위 시스템을 설치
description: Windows 10에서 Linux 용 Windows 하위 시스템에 대 한 설치 지침입니다.
keywords: BashOnWindows, bash, wsl, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템에 설치
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063291"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10 용 Linux 설치 가이드 용 Windows 하위 시스템

## <a name="install-the-windows-subsystem-for-linux"></a>Linux 용 Windows 하위 시스템을 설치 합니다.

WSL에 대 한 모든 Linux 배포판을 설치 하기 전에 "Windows 하위 시스템에 대 한 Linux" 선택적 기능을 사용 해야 합니다.

1. 관리자 권한으로 PowerShell을 열고 실행 합니다.
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 메시지가 표시 되 면 컴퓨터를 다시 시작 합니다.

## <a name="install-your-linux-distribution-of-choice"></a>선택한 Linux 배포를 설치 합니다.
를 다운로드 하 여 기본 distro(s)를 설치 하는 세 가지 옵션이 있습니다.
1. (아래 참조) Windows 스토어에서 다운로드 및 설치
1. Command 명령줄/스크립트에서 다운로드 및 설치 ([수동 설치 지침을 읽고](install-manual.md))
1. 다운로드 하 고 수동으로 풀고 설치 (Windows Server-에 대 한 [지침이](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 이상: Microsoft Store 설치

> 이 섹션에서는 Windows 빌드 16215 이상입니다.  다음이 단계를 수행 [빌드를 확인할](troubleshooting.md#check-your-build-number)합니다. 

1. Microsoft Store 열고 원하는 Linux 배포판을 선택 합니다.

    ![Windows 스토어에서 Linux 배포판의 보기](media/store.png)

    다음 링크는 각 배포에 대 한 Windows 스토어 페이지를 엽니다.

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. 배포판의 페이지에서 "Get"을 선택

    ![Windows 스토어에서 Linux 배포판의 보기](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>배포의 초기화를 완료
이제 Linux 배포를 설치 해야 [새 배포판 인스턴스를 초기화](initialize-distro.md) 번 사용할 수 있습니다.

## <a name="troubleshooting"></a>문제 해결: 

다음은 관련된 오류 및 제안 된 수정 합니다. 참조 된 [WSL 문제 해결 페이지](troubleshooting.md) 다른 일반적인 오류 및 해결 방법에 대 한 합니다.

* **설치 0x80070003 오류로 실패 합니다.**
    * Linux 용 Windows 하위 시스템은 시스템 드라이브에만 실행 됩니다 (이 일반적으로 프로그램 `C:` 드라이브). 배포판은 시스템 드라이브에 저장 되도록 해야 합니다.  
    * 오픈 **설정을** -> **Storage** -> **더 많은 저장소 설정: 새 콘텐츠 저장 위치 변경**
    ![c: 드라이브에 앱을 설치 시스템 설정의 그림](media/AppStorage.png)
