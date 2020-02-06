---
title: Linux용 Windows 하위 시스템의 릴리스 정보
description: Linux용 Windows 하위 시스템의 릴리스 정보입니다.  매주 업데이트됩니다.
keywords: BashOnWindows, bash, wsl, windows, linux용 windows 하위 시스템, windows 하위 시스템, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 31bf975afb202a6cfd9a2879cff29a77b2969fce
ms.sourcegitcommit: 7069b8d452308c32cc7fa31d1158fcb130d42e06
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/01/2020
ms.locfileid: "76911707"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="5e6fb-105">Linux용 Windows 하위 시스템의 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="5e6fb-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19555"></a><span data-ttu-id="5e6fb-106">빌드 19555</span><span class="sxs-lookup"><span data-stu-id="5e6fb-106">Build 19555</span></span>
<span data-ttu-id="5e6fb-107">빌드 19555에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-107">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="5e6fb-108">[WSL2] 메모리 cgroup을 사용하여 설치 및 변환 작업에 사용되는 메모리 양 제한 [GH 4669]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-108">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="5e6fb-109">기능 검색 기능을 향상시키기 위해 Linux용 Windows 하위 시스템 선택적 구성 요소를 사용할 수 없는 경우 wsl.exe가 표시되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-109">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="5e6fb-110">WSL 선택적 구성 요소가 설치되지 않은 경우 도움말 텍스트를 인쇄하도록 wsl.exe 변경</span><span class="sxs-lookup"><span data-stu-id="5e6fb-110">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="5e6fb-111">인스턴스를 만들 때 경합 상태 수정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-111">Fix race condition when creating instances</span></span>
* <span data-ttu-id="5e6fb-112">모든 명령줄 기능이 포함된 wslclient.dll 생성</span><span class="sxs-lookup"><span data-stu-id="5e6fb-112">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="5e6fb-113">LxssManagerUser 서비스 중지 중 충돌 방지</span><span class="sxs-lookup"><span data-stu-id="5e6fb-113">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="5e6fb-114">distroName 매개 변수가 NULL인 경우 wslapi.dll 빠른 실패 수정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-114">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="5e6fb-115">빌드 19041</span><span class="sxs-lookup"><span data-stu-id="5e6fb-115">Build 19041</span></span>
<span data-ttu-id="5e6fb-116">빌드 19041에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-116">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="5e6fb-117">[WSL2] 프로세스를 시작하기 전에 신호 마스크 지우기</span><span class="sxs-lookup"><span data-stu-id="5e6fb-117">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="5e6fb-118">[WSL2] Linux 커널을 4.19.84로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5e6fb-118">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="5e6fb-119">symlink가 비 상대적일 때 /etc/resolv.conf symlink 생성 처리</span><span class="sxs-lookup"><span data-stu-id="5e6fb-119">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="5e6fb-120">빌드 19028</span><span class="sxs-lookup"><span data-stu-id="5e6fb-120">Build 19028</span></span>
<span data-ttu-id="5e6fb-121">빌드 19028에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-121">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="5e6fb-122">[WSL2] Linux 커널을 4.19.81로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5e6fb-122">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="5e6fb-123">[WSL2] /dev/net/tun의 기본 권한을 0666으로 변경 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-123">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="5e6fb-124">[WSL2] Linux VM에 할당된 기본 메모리 양을 호스트 메모리의 80%로 조정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-124">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="5e6fb-125">[WSL2] 잘못된 호출자가 서버를 중지할 수 없게 시간 제한이 있는 요청을 처리하도록 interop 서버 수정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-125">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="5e6fb-126">빌드 19018</span><span class="sxs-lookup"><span data-stu-id="5e6fb-126">Build 19018</span></span>
<span data-ttu-id="5e6fb-127">빌드 19018에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-127">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="5e6fb-128">[WSL2] 9p 탑재의 기본값으로 cache=mmap을 사용하여 dotnet 앱 수정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-128">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="5e6fb-129">[WSL2] localhost 릴레이 수정 [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-129">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="5e6fb-130">[WSL2] 크로스 배포판 공유 tmpfs 탑재를 도입하여 배포판 사이에서 상태 공유</span><span class="sxs-lookup"><span data-stu-id="5e6fb-130">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="5e6fb-131">\\\\wsl$에 대한 영구 네트워크 드라이브 복원 수정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-131">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="5e6fb-132">빌드 19013</span><span class="sxs-lookup"><span data-stu-id="5e6fb-132">Build 19013</span></span>
<span data-ttu-id="5e6fb-133">빌드 19013에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-133">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="5e6fb-134">[WSL2] WSL 유틸리티 VM의 메모리 성능을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-134">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="5e6fb-135">더 이상 사용하지 않는 메모리는 호스트로 다시 해제됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-135">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="5e6fb-136">[WSL2] 커널 버전을 4.19.79로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-136">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="5e6fb-137">(CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK 및 CONFIG_BRIDGE_VLAN_FILTERING 추가).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-137">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="5e6fb-138">[WSL2] stdin이 닫혀 있지 않은 파이프 핸들인 경우를 처리하기 위해 입력 릴레이를 수정합니다.[GH 4424]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-138">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="5e6fb-139">\\\\wsl$ 대/소문자를 구분하지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-139">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="5e6fb-140">빌드 19002</span><span class="sxs-lookup"><span data-stu-id="5e6fb-140">Build 19002</span></span>
<span data-ttu-id="5e6fb-141">빌드 19002에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-141">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="5e6fb-142">[WSL] 일부 유니코드 문자 처리 이슈 해결: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="5e6fb-142">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="5e6fb-143">[WSL] 빌드 간 업그레이드 후 바로 시작할 경우 드물게 배포판이 등록 취소되는 사례를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-143">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="5e6fb-144">[WSL] 인스턴스 유휴 타이머가 취소되지 않은 wsl.exe --shutdown의 사소한 이슈를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-144">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="5e6fb-145">빌드 18995</span><span class="sxs-lookup"><span data-stu-id="5e6fb-145">Build 18995</span></span>
<span data-ttu-id="5e6fb-146">빌드 18995에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-146">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="5e6fb-147">[WSL2] 작업이 중단된 후 DrvFs 탑재가 중지되는 문제 해결(예: ctrl-c) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-147">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="5e6fb-148">[WSL2] 매우 큰 hvsocket 메시지 처리 문제 해결 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-148">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="5e6fb-149">[WSL2] stdin이 파일인 경우 interop 문제 해결 [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-149">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="5e6fb-150">[WSL2] 예기치 않은 네트워크 상태가 발생한 경우 서비스 충돌 문제 해결 [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-150">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="5e6fb-151">[WSL2] 현재 프로세스에 환경 변수가 없는 경우 interop 서버에서 배포 이름 쿼리</span><span class="sxs-lookup"><span data-stu-id="5e6fb-151">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="5e6fb-152">[WSL2] stdin이 파일인 경우 interop 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5e6fb-152">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="5e6fb-153">[WSL2] Linux 커널 버전을 4.19.72로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5e6fb-153">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="5e6fb-154">[WSL2] .wslconfig를 통해 추가 커널 명령줄 매개 변수를 지정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="5e6fb-154">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="5e6fb-155">빌드 18990</span><span class="sxs-lookup"><span data-stu-id="5e6fb-155">Build 18990</span></span>
<span data-ttu-id="5e6fb-156">빌드 18990에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-156">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="5e6fb-157">\\\\wsl$의 디렉터리 목록의 성능 개선</span><span class="sxs-lookup"><span data-stu-id="5e6fb-157">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="5e6fb-158">[WSL2] 추가 부팅 엔트로피를 주입합니다.[GH 4416]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-158">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="5e6fb-159">[WSL2] su/sudo를 사용할 때 Windows 인터럽트를 수정합니다.[GH 4465]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-159">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="5e6fb-160">빌드 18980</span><span class="sxs-lookup"><span data-stu-id="5e6fb-160">Build 18980</span></span>
<span data-ttu-id="5e6fb-161">빌드 18980에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-161">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="5e6fb-162">FILE_READ_DATA를 거부하는 읽기 symlink를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-162">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="5e6fb-163">여기에는 "C:\Document and Settings"처럼 이전 버전과의 호환성을 위해 Windows에서 만드는 모든 symlink와 사용자 프로필 디렉터리의 symlink가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-163">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="5e6fb-164">예기치 않은 파일 시스템 상태를 심각하지 않은 상태로 표시합니다. [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-164">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="5e6fb-165">[WSL2] CPU/펌웨어가 가상화를 지원하는 경우 arm64에 대한 지원이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-165">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="5e6fb-166">[WSL2] 권한 없는 사용자가 커널 로그를 볼 수 있도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-166">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="5e6fb-167">[WSL2] stdout/stderr 소켓이 닫혀 있을 때 발생하는 출력 릴레이를 수정했습니다. [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-167">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="5e6fb-168">[WSL2] 배터리 및 AC 어댑터 통과를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-168">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="5e6fb-169">[WSL2] Linux 커널을 4.19.67로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-169">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="5e6fb-170">다음과 같이 /etc/wsl.conf에서 기본 사용자 이름을 설정하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-170">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="5e6fb-171">빌드 18975</span><span class="sxs-lookup"><span data-stu-id="5e6fb-171">Build 18975</span></span>
<span data-ttu-id="5e6fb-172">빌드 18975에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-172">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="5e6fb-173">[WSL2] 여러 localhost 안정성 이슈를 해결했습니다. [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-173">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="5e6fb-174">빌드 18970</span><span class="sxs-lookup"><span data-stu-id="5e6fb-174">Build 18970</span></span>
<span data-ttu-id="5e6fb-175">빌드 18970에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-175">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="5e6fb-176">[WSL2] 시스템이 절전 모드에서 다시 시작될 때 시간을 호스트 시간과 동기화합니다. [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-176">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="5e6fb-177">[WSL2] 가능한 경우 Windows 볼륨에 NT symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-177">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="5e6fb-178">[WSL2] UTS, IPC, PID 및 탑재 네임스페이스에서 배포판을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-178">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="5e6fb-179">[WSL2] 서버가 localhost에 직접 바인딩할 때 localhost 포트 릴레이를 수정합니다. [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-179">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="5e6fb-180">[WSL2] 출력이 리디렉션될 때 interop를 수정합니다. [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-180">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="5e6fb-181">[WSL2] 절대 NT symlink 변환을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-181">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="5e6fb-182">[WSL2] 커널을 4.19.59로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-182">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="5e6fb-183">[WSL2] eth0에 대한 서브넷 마스크를 적절히 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-183">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="5e6fb-184">[WSL2] 종료 이벤트가 신호를 받으면 콘솔 작업자 루프를 중단하도록 논리를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-184">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="5e6fb-185">[WSL2] 배포판이 실행되고 있지 않으면 배포용 vhd를 배출합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-185">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="5e6fb-186">[WSL2] 빈 값을 올바르게 처리하도록 구성 구문 분석 라이브러리를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-186">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="5e6fb-187">[WSL2] 교차 배포판 탑재를 만들어 Docker 데스크톱을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-187">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="5e6fb-188">다음 줄을 /etc/wsl.conf 파일에 추가하여 배포판에서 이 동작을 옵트인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-188">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="5e6fb-189">빌드 18945</span><span class="sxs-lookup"><span data-stu-id="5e6fb-189">Build 18945</span></span>
<span data-ttu-id="5e6fb-190">빌드 18945에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-190">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-191">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-191">WSL</span></span>
* <span data-ttu-id="5e6fb-192">[WSL2] localhost:port를 사용하여 호스트에서 액세스할 수 있도록 WSL2에서 수신 대기 tcp 소켓을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-192">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="5e6fb-193">[WSL2] 향후 이슈를 추적하도록 설치/변환 오류 및 추가 진단을 수정합니다. [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-193">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="5e6fb-194">[WSL2] WSL2 네트워크 이슈 진단 기능을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-194">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="5e6fb-195">[WSL2] 커널 버전을 4.19.55로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-195">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="5e6fb-196">[WSL2] docker에 필요한 구성 옵션으로 커널을 업데이트합니다. [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-196">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="5e6fb-197">[WSL2] 경량 유틸리티 VM에 할당된 CPU 수를 호스트와 동일하게 늘립니다(이전에는 커널 구성의 CONFIG_NR_CPUS에 의해 8로 제한). [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-197">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="5e6fb-198">[WSL2] WSL2 경량 VM에 대한 스왑 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-198">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="5e6fb-199">[WSL2] 사용자가 \\\\wsl$\\distro를 통해 탑재를 볼 수 있도록 허용합니다(예: sshfs). [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-199">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="5e6fb-200">[WSL2] 9p 파일 시스템 성능을 개선합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-200">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="5e6fb-201">[WSL2] vhd ACL이 무한으로 확장되지 않도록 보장합니다. [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-201">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="5e6fb-202">[WSL2] squashfs 및 xt_conntrack을 지원하도록 커널 구성을 업데이트합니다. [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-202">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="5e6fb-203">[WSL2] interop.enabled /etc/wsl.conf 옵션을 수정합니다. [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-203">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="5e6fb-204">[WSL2] 파일 시스템에서 EA를 지원하지 않는 경우 ENOTSUP를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-204">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="5e6fb-205">[WSL2] \\\\wsl$를 사용하여 CopyFile 중단을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-205">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="5e6fb-206">기본 umask를 0022로 전환하고 /etc/wsl.conf에 filesystem.umask 설정을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-206">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="5e6fb-207">symlink를 적절하게 확인하도록 wslpath를 수정합니다.이것은 19h1에서 회귀되었습니다. [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-207">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="5e6fb-208">WSL2 설정을 수정하기 위한 %UserProfile%\\.wslconfig 파일을 도입합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-208">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="5e6fb-209">빌드 18917</span><span class="sxs-lookup"><span data-stu-id="5e6fb-209">Build 18917</span></span>
<span data-ttu-id="5e6fb-210">빌드 18917에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-210">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-211">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-211">WSL</span></span>
* <span data-ttu-id="5e6fb-212">이제 WSL 2를 사용할 수 있습니다!</span><span class="sxs-lookup"><span data-stu-id="5e6fb-212">WSL 2 is now available!</span></span> <span data-ttu-id="5e6fb-213">자세한 내용은 [블로그](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-213">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="5e6fb-214">symlink를 통해 Windows 프로세스를 시작하면 올바르게 작동하지 않는 성능 문제를 해결합니다. [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-214">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="5e6fb-215">wsl.exe에 wsl.exe --list --verbose, wsl.exe --list --quiet 및 wsl.exe --import --version 옵션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-215">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="5e6fb-216">wsl.exe --shutdown 옵션을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-216">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="5e6fb-217">플랜 9: 쓰기가 성공하도록 디렉터리 열기를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-217">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="5e6fb-218">빌드 18890</span><span class="sxs-lookup"><span data-stu-id="5e6fb-218">Build 18890</span></span>
<span data-ttu-id="5e6fb-219">빌드 18890에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-219">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-220">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-220">WSL</span></span>
* <span data-ttu-id="5e6fb-221">비차단 소켓 유실 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-221">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="5e6fb-222">터미널의 EOF 입력이 후속 읽기를 차단할 수 있습니다. [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-222">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="5e6fb-223">wsl.conf를 참조하도록 resolv.conf 헤더를 업데이트합니다. [GH 3928에서 설명]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-223">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="5e6fb-224">epoll 삭제 코드의 교착 상태 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-224">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="5e6fb-225">--import 및 –export에 대한 인수의 공백을 처리합니다. [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-225">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="5e6fb-226">mmap’d 파일을 확장하면 올바르게 작동하지 않습니다. [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-226">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="5e6fb-227">ARM64 \\\\wsl$ 액세스가 올바르게 작동하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="5e6fb-227">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="5e6fb-228">wsl.exe에 대한 개선된 기본 아이콘을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-228">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="5e6fb-229">빌드 18342</span><span class="sxs-lookup"><span data-stu-id="5e6fb-229">Build 18342</span></span>
<span data-ttu-id="5e6fb-230">빌드 18342에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-230">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-231">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-231">WSL</span></span>
* <span data-ttu-id="5e6fb-232">사용자가 Windows에서 WSL 배포판의 Linux 파일에 액세스할 수 있는 기능을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-232">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="5e6fb-233">이러한 파일은 명령줄을 통해 액세스할 수 있으며 파일 탐색기, VSCode 등의 Windows 앱에서도 이러한 파일과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-233">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="5e6fb-234">\\\\wsl$\\<distro_name>으로 이동하여 파일에 액세스하거나, \\\\wsl$로 이동하여 실행 중인 배포판 목록을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-234">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="5e6fb-235">추가 CPU 정보 태그를 추가하고 Cpus_allowed[_list] 값을 수정합니다. [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-235">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="5e6fb-236">리더가 아닌 스레드의 exec를 지원합니다. [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-236">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="5e6fb-237">구성 업데이트 실패를 심각하지 않은 오류로 처리합니다. [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-237">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="5e6fb-238">오프셋을 적절하게 처리하도록 binfmt를 업데이트합니다. [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-238">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="5e6fb-239">플랜 9에 매핑 네트워크 드라이브를 사용합니다. [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-239">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="5e6fb-240">바인딩 마운트를 위한 Windows > Linux 및 Linux > Windows 경로 변환을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-240">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="5e6fb-241">읽기 전용으로 열린 파일의 매핑에 대한 읽기 전용 섹션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-241">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="5e6fb-242">빌드 18334</span><span class="sxs-lookup"><span data-stu-id="5e6fb-242">Build 18334</span></span>
<span data-ttu-id="5e6fb-243">빌드 18334에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-243">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-244">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-244">WSL</span></span>
* <span data-ttu-id="5e6fb-245">Windows 표준 시간대가 Linux 표준 시간대에 매핑되는 방식을 다시 디자인합니다. [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-245">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="5e6fb-246">메모리 누수를 해결하고 새 문자열 변환 함수를 추가합니다. [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-246">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="5e6fb-247">스레드 없는 threadgroup의 SIGCONT는 no-op입니다. [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-247">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="5e6fb-248">/proc/self/fd에 소켓 및 epoll 파일 설명자를 올바르게 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-248">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="5e6fb-249">빌드 18305</span><span class="sxs-lookup"><span data-stu-id="5e6fb-249">Build 18305</span></span>
<span data-ttu-id="5e6fb-250">빌드 18305에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-250">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-251">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-251">WSL</span></span>
* <span data-ttu-id="5e6fb-252">주 스레드가 종료되면 pthread가 파일에 액세스할 수 없습니다. [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-252">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="5e6fb-253">TIOCSCTTY는 꼭 필요한 경우 외에는 "force" 매개 변수를 무시해야 합니다. [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-253">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="5e6fb-254">wsl.exe 명령줄 기능이 개선되고 가져오기/내보내기 함수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-254">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="5e6fb-255">빌드 18277</span><span class="sxs-lookup"><span data-stu-id="5e6fb-255">Build 18277</span></span>
<span data-ttu-id="5e6fb-256">빌드 18277에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-256">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-257">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-257">WSL</span></span>
* <span data-ttu-id="5e6fb-258">빌드 18272에서 발생하는 "해당 인터페이스를 지원하지 않습니다" 오류를 해결합니다. [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-258">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="5e6fb-259">umount syscall에 대한 MNT_FORCE 플래그를 무시합니다. [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-259">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="5e6fb-260">공식 CreatePseudoConsole API를 사용하도록 WSL interop를 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-260">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="5e6fb-261">FUTEX_WAIT가 다시 시작할 때 시간 제한 값을 유지하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-261">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="5e6fb-262">빌드 18272</span><span class="sxs-lookup"><span data-stu-id="5e6fb-262">Build 18272</span></span>
<span data-ttu-id="5e6fb-263">빌드 18272에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-263">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-264">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-264">WSL</span></span>
* <span data-ttu-id="5e6fb-265">**경고:** 이 빌드에는 WSL이 작동하지 않는 문제가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-265">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="5e6fb-266">배포를 시작하려고 하면 "해당 인터페이스를 지원하지 않습니다" 오류가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-266">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="5e6fb-267">이 이슈는 해결되었으며 다음 주의 초기 참가자 빌드에 포함될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-267">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="5e6fb-268">이 빌드를 설치한 경우 설정->업데이트 & 보안->복구에서 "이전 버전의 Windows 10으로 되돌리기"를 사용하여 이전 Windows 빌드로 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-268">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="5e6fb-269">빌드 18267</span><span class="sxs-lookup"><span data-stu-id="5e6fb-269">Build 18267</span></span>
<span data-ttu-id="5e6fb-270">빌드 18267에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-270">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-271">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-271">WSL</span></span>
* <span data-ttu-id="5e6fb-272">좀비 프로세스가 제거되지 않고 무기한으로 유지되는 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-272">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="5e6fb-273">오류 메시지가 최대 길이를 초과하는 경우 WslRegisterDistribution이 중지됩니다. [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-273">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="5e6fb-274">DrvFs에서 읽기 전용 파일에 대해 fsync가 성공하도록 허용합니다. [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-274">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="5e6fb-275">symlink를 만들기 전에 /bin 및 /sbin 디렉터리가 존재하는지 확인합니다. [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-275">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="5e6fb-276">WSL 인스턴스에 대한 인스턴스 종료 시간 제한 메커니즘이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-276">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="5e6fb-277">현재 시간 제한은 15초로 설정되어 있습니다. 즉, 마지막 WSL 프로세스가 종료된 후 15초 후에 인스턴스가 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-277">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="5e6fb-278">배포를 즉시 종료하려면 다음을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-278">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="5e6fb-279">빌드 17763(1809)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-279">Build 17763 (1809)</span></span>
<span data-ttu-id="5e6fb-280">빌드 17763에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-280">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-281">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-281">WSL</span></span>
* <span data-ttu-id="5e6fb-282">동일한 스레드 우선 순위를 변경하기 위한 Setpriority syscall 권한 검사가 너무 엄격합니다. [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-282">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="5e6fb-283">clock_gettime(CLOCK_BOOTTIME)에 대한 음수 값이 반환되지 않도록, 부팅 시간에 비편향 인터럽트 시간을 사용하도록 확인합니다. [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-283">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="5e6fb-284">WSL binfmt 인터프리터의 symlink를 처리합니다. [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-284">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="5e6fb-285">threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-285">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="5e6fb-286">오버플로를 방지하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용하도록 WSL을 전환합니다. [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-286">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="5e6fb-287">Ptrace attach로 인해 시스템 호출에서 잘못된 값이 반환될 수 있습니다. [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-287">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="5e6fb-288">여러 AF_UNIX 관련 이슈를 해결합니다. [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-288">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="5e6fb-289">현재 작업 디렉터리 길이가 5자 미만인 경우 WSL interop가 실패할 수 있는 이슈를 해결합니다. [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-289">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="5e6fb-290">존재하지 않는 포트에 대한 루프백 연결이 실패하지 않도록 1초 지연을 방지합니다. [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-290">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="5e6fb-291">/proc/sys/fs/file-max 스텁 파일을 추가합니다. [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-291">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="5e6fb-292">보다 정확한 IPV6 범위 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-292">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="5e6fb-293">PR_SET_PTRACER를 지원합니다. [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-293">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="5e6fb-294">파이프 파일 시스템이 의도치 않게 에지에서 트리거한 epoll 이벤트를 삭제합니다. [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-294">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="5e6fb-295">NTFS symlink를 통해 시작된 Win32 실행 파일이 symlink 이름을 준수하지 않습니다. [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-295">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="5e6fb-296">좀비 지원이 개선되었습니다. [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-296">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="5e6fb-297">Windows interop 동작을 제어하기 위한 wsl.conf 항목을 추가합니다. [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-297">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="5e6fb-298">getsockname이 경우에 따라 UNIX 소켓 패밀리 유형을 반환하지 않는 문제를 해결합니다. [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-298">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="5e6fb-299">TIOCSTI 지원이 추가됩니다. [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-299">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="5e6fb-300">연결 중인 비차단 소켓은 쓰기 시도에 대한 EAGAIN을 반환해야 합니다. [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-300">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="5e6fb-301">탑재된 VHD에서 interop를 지원합니다. [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-301">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="5e6fb-302">루트 폴더에 대한 권한 확인 이슈를 해결합니다. [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-302">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="5e6fb-303">TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대한 지원이 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-303">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="5e6fb-304">Windows UI 앱은 백그라운드에서 시작된 경우에도 실행되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-304">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="5e6fb-305">wsl -u 또는 --user 옵션이 추가됩니다. [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-305">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="5e6fb-306">빠른 시작을 사용하는 경우 WSL 시작 이슈를 해결합니다. [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-306">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="5e6fb-307">Unix 소켓은 연결 해제된 피어 자격 증명을 유지해야 합니다. [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-307">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="5e6fb-308">비차단 Unix 소켓이 EAGAIN과 함께 무기한 실패합니다. [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-308">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="5e6fb-309">case=off는 새로운 기본 drvfs 탑재 유형입니다. [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-309">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="5e6fb-310">자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-310">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="5e6fb-311">실행 중인 배포를 중지하려면 wslconfig /terminate를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-311">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="5e6fb-312">공백이 포함된 경로를 올바르게 처리하지 않는 WSL 셸 팝업 메뉴 항목의 이슈를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-312">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="5e6fb-313">디렉터리별 대/소문자 구분을 확장 특성으로 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-313">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="5e6fb-314">ARM64: 캐시 유지 관리 작업을 에뮬레이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-314">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="5e6fb-315">[dotnet 이슈](https://github.com/dotnet/core/issues/1561)를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-315">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="5e6fb-316">DrvFs: 프라이빗 범위에서 이스케이프된 문자에 해당하는 문자만 unescape합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-316">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="5e6fb-317">ELF 파서 인터프리터 길이 유효성 검사의 OB1 오류를 수정합니다. [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-317">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="5e6fb-318">과거 시간이 포함된 WSL 절대 타이머가 시작되지 않습니다. [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-318">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="5e6fb-319">새로 만든 재분석 지점이 부모 디렉터리에 표시되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-319">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="5e6fb-320">DrvFs에 대/소문자를 구분하는 디렉터리를 원자 단위로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-320">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="5e6fb-321">파일이 있어도 다중 스레드 작업에서 ENOENT를 반환할 수 있는 추가 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-321">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="5e6fb-322">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-322">[GH 2712]</span></span>
* <span data-ttu-id="5e6fb-323">UMCI를 사용하는 경우 WSL 시작이 실패하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-323">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="5e6fb-324">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-324">[GH 3020]</span></span>
* <span data-ttu-id="5e6fb-325">WSL을 시작하는 탐색기 팝업 메뉴를 추가합니다. [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="5e6fb-325">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="5e6fb-326">사용하려면 탐색기 창에서 Shift 키를 누른 상태로 마우스 오른쪽 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-326">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="5e6fb-327">Unix 소켓 비차단 동작을 수정합니다. [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-327">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="5e6fb-328">GH 2026에 보고된 것처럼 NETLINK 명령이 중지되는 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-328">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="5e6fb-329">탑재 전파 플래그에 대한 지원이 추가됩니다. [GH 2911]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-329">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="5e6fb-330">자르기가 Inotify 이벤트를 발생시키지 않는 이슈를 해결합니다. [GH 2978]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-330">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="5e6fb-331">wsl.exe가 셸 없이 단일 이진 파일을 호출하는 --exec 옵션이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-331">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="5e6fb-332">wsl.exe가 특정 배포판을 선택하는 --distribution 옵션이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-332">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="5e6fb-333">dmesg에 대한 지원이 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-333">Limited support for dmesg.</span></span> <span data-ttu-id="5e6fb-334">이제 애플리케이션에서 dmesg에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-334">Applications can now log to dmesg.</span></span> <span data-ttu-id="5e6fb-335">WSL 드라이버는 제한된 정보를 dmesg에 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-335">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="5e6fb-336">이후에 드라이버의 다른 정보/진단을 수행하도록 이 기능이 확장될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-336">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="5e6fb-337">참고: dmesg는 현재 `/dev/kmsg` 디바이스 인터페이스를 통해 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-337">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="5e6fb-338">`syslog` syscall 인터페이스는 아직 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-338">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="5e6fb-339">따라서 `-S`, `-C` 같은 `dmesg` 명령줄 옵션 중 일부는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-339">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="5e6fb-340">네이티브와 일치하도록 직렬 디바이스의 기본 그리드 및 모드를 변경합니다. [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-340">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="5e6fb-341">DrvFs는 이제 확장된 특성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-341">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="5e6fb-342">참고: DrvFs는 확장 특성의 이름에 대한 몇 가지 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-342">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="5e6fb-343">일부 문자(예: '/', ':' 및 '\*')는 허용되지 않으며, 확장 특성 이름은 DrvFs에서 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-343">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="5e6fb-344">빌드 18252(앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-344">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="5e6fb-345">빌드 18252에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-345">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-346">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-346">WSL</span></span>
* <span data-ttu-id="5e6fb-347">lxssmanager dll에서 init 및 bsdtar 이진 파일을 별도의 도구 폴더로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-347">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="5e6fb-348">CLONE_FILES를 사용할 때 파일 설명자를 닫는 동안 경합을 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-348">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="5e6fb-349">DrvFs 경로를 변환할 때 /proc/pid/mountinfo의 선택적 필드를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-349">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="5e6fb-350">S_IFREG에 대한 메타데이터 지원 없이 DrvFs mknod가 성공하도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-350">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="5e6fb-351">DrvFs에서 만든 읽기 전용 파일에는 readonly 특성 세트가 있어야 합니다. [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-351">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="5e6fb-352">DrvFs 탑재를 처리하는 /sbin/mount.drvfs 도우미가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-352">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="5e6fb-353">DrvFs에서 POSIX rename을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-353">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="5e6fb-354">볼륨 GUID 없이 볼륨의 경로 변환을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-354">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="5e6fb-355">빌드 17738(패스트)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-355">Build 17738 (Fast)</span></span>
<span data-ttu-id="5e6fb-356">빌드 17738에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-356">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-357">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-357">WSL</span></span>
* <span data-ttu-id="5e6fb-358">동일한 스레드 우선 순위를 변경하기 위한 Setpriority syscall 권한 검사가 너무 엄격합니다. [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-358">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="5e6fb-359">clock_gettime(CLOCK_BOOTTIME)에 대한 음수 값이 반환되지 않도록, 부팅 시간에 비편향 인터럽트 시간을 사용하도록 확인합니다. [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-359">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="5e6fb-360">WSL binfmt 인터프리터의 symlink를 처리합니다. [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-360">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="5e6fb-361">threadgroup 리더 파일 설명자 정리를 보다 효율적으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-361">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="5e6fb-362">빌드 17728(패스트)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-362">Build 17728 (Fast)</span></span>
<span data-ttu-id="5e6fb-363">빌드 17728에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-363">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-364">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-364">WSL</span></span>
* <span data-ttu-id="5e6fb-365">오버플로를 방지하기 위해 KeQueryPerformanceCounter 대신 KeQueryInterruptTimePrecise를 사용하도록 WSL을 전환합니다. [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-365">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="5e6fb-366">Ptrace attach로 인해 시스템 호출에서 잘못된 값이 반환될 수 있습니다. [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-366">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="5e6fb-367">여러 AF_UNIX 관련 이슈를 해결합니다. [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-367">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="5e6fb-368">현재 작업 디렉터리 길이가 5자 미만인 경우 WSL interop가 실패할 수 있는 이슈를 해결합니다. [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-368">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="5e6fb-369">빌드 18204(앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-369">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="5e6fb-370">빌드 18204에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-370">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-371">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-371">WSL</span></span>
* <span data-ttu-id="5e6fb-372">파이프 파일 시스템이 의도치 않게 에지에서 트리거한 epoll 이벤트를 삭제합니다. [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-372">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="5e6fb-373">NTFS symlink를 통해 시작된 Win32 실행 파일이 symlink 이름을 준수하지 않습니다. [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-373">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="5e6fb-374">빌드 17723(패스트)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-374">Build 17723 (Fast)</span></span>
<span data-ttu-id="5e6fb-375">빌드 17723에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-375">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-376">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-376">WSL</span></span>
* <span data-ttu-id="5e6fb-377">존재하지 않는 포트에 대한 루프백 연결이 실패하지 않도록 1초 지연을 방지합니다. [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-377">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="5e6fb-378">/proc/sys/fs/file-max 스텁 파일을 추가합니다. [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-378">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="5e6fb-379">보다 정확한 IPV6 범위 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-379">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="5e6fb-380">PR_SET_PTRACER를 지원합니다. [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-380">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="5e6fb-381">파이프 파일 시스템이 의도치 않게 에지에서 트리거한 epoll 이벤트를 삭제합니다. [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-381">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="5e6fb-382">NTFS symlink를 통해 시작된 Win32 실행 파일이 symlink 이름을 준수하지 않습니다. [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-382">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="5e6fb-383">빌드 17713</span><span class="sxs-lookup"><span data-stu-id="5e6fb-383">Build 17713</span></span>
<span data-ttu-id="5e6fb-384">빌드 17713에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-384">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-385">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-385">WSL</span></span>
* <span data-ttu-id="5e6fb-386">좀비 지원이 개선되었습니다. [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-386">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="5e6fb-387">Windows interop 동작을 제어하기 위한 wsl.conf 항목을 추가합니다. [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-387">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="5e6fb-388">getsockname이 경우에 따라 UNIX 소켓 패밀리 유형을 반환하지 않는 문제를 해결합니다. [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-388">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="5e6fb-389">TIOCSTI 지원이 추가됩니다. [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-389">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="5e6fb-390">연결 중인 비차단 소켓은 쓰기 시도에 대한 EAGAIN을 반환해야 합니다. [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-390">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="5e6fb-391">탑재된 VHD에서 interop를 지원합니다. [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-391">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="5e6fb-392">루트 폴더에 대한 권한 확인 이슈를 해결합니다. [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-392">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="5e6fb-393">TTY 키보드 ioctls KDGKBTYPE, KDGKBMODE 및 KDSKBMODE에 대한 지원이 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-393">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="5e6fb-394">Windows UI 앱은 백그라운드에서 시작된 경우에도 실행되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-394">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="5e6fb-395">빌드 17704</span><span class="sxs-lookup"><span data-stu-id="5e6fb-395">Build 17704</span></span>
<span data-ttu-id="5e6fb-396">빌드 17704에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-396">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-397">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-397">WSL</span></span>
* <span data-ttu-id="5e6fb-398">wsl -u 또는 --user 옵션이 추가됩니다. [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-398">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="5e6fb-399">빠른 시작을 사용하는 경우 WSL 시작 이슈를 해결합니다. [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-399">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="5e6fb-400">Unix 소켓은 연결 해제된 피어 자격 증명을 유지해야 합니다. [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-400">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="5e6fb-401">비차단 Unix 소켓이 EAGAIN과 함께 무기한 실패합니다. [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-401">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="5e6fb-402">case=off는 새로운 기본 drvfs 탑재 유형입니다. [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-402">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="5e6fb-403">자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-403">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="5e6fb-404">실행 중인 배포를 중지하려면 wslconfig /terminate를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-404">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="5e6fb-405">빌드 17692</span><span class="sxs-lookup"><span data-stu-id="5e6fb-405">Build 17692</span></span>
<span data-ttu-id="5e6fb-406">빌드 17692에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-406">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-407">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-407">WSL</span></span>
* <span data-ttu-id="5e6fb-408">공백이 포함된 경로를 올바르게 처리하지 않는 WSL 셸 팝업 메뉴 항목의 이슈를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-408">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="5e6fb-409">디렉터리별 대/소문자 구분을 확장 특성으로 노출합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-409">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="5e6fb-410">ARM64: 캐시 유지 관리 작업을 에뮬레이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-410">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="5e6fb-411">[dotnet 이슈](https://github.com/dotnet/core/issues/1561)를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-411">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="5e6fb-412">DrvFs: 프라이빗 범위에서 이스케이프된 문자에 해당하는 문자만 unescape합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-412">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="5e6fb-413">빌드 17686</span><span class="sxs-lookup"><span data-stu-id="5e6fb-413">Build 17686</span></span>
<span data-ttu-id="5e6fb-414">빌드 17686에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-414">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-415">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-415">WSL</span></span>
* <span data-ttu-id="5e6fb-416">ELF 파서 인터프리터 길이 유효성 검사의 OB1 오류를 수정합니다. [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-416">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="5e6fb-417">과거 시간이 포함된 WSL 절대 타이머가 시작되지 않습니다. [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-417">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="5e6fb-418">새로 만든 재분석 지점이 부모 디렉터리에 표시되는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-418">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="5e6fb-419">DrvFs에 대/소문자를 구분하는 디렉터리를 원자 단위로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-419">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="5e6fb-420">빌드 17677</span><span class="sxs-lookup"><span data-stu-id="5e6fb-420">Build 17677</span></span>
<span data-ttu-id="5e6fb-421">빌드 17677에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-421">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-422">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-422">WSL</span></span>
* <span data-ttu-id="5e6fb-423">파일이 있어도 다중 스레드 작업에서 ENOENT를 반환할 수 있는 추가 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-423">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="5e6fb-424">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-424">[GH 2712]</span></span>
* <span data-ttu-id="5e6fb-425">UMCI를 사용하는 경우 WSL 시작이 실패하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-425">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="5e6fb-426">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-426">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="5e6fb-427">빌드 17666</span><span class="sxs-lookup"><span data-stu-id="5e6fb-427">Build 17666</span></span>
<span data-ttu-id="5e6fb-428">빌드 17666에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-428">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-429">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-429">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="5e6fb-430">경고: 일부 AMD 칩셋에서 WSL이 실행되지 않는 이슈가 있습니다 [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="5e6fb-430">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="5e6fb-431">해결 방법이 준비되어 있으며 참가자 빌드 분기에 적용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-431">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="5e6fb-432">WSL을 시작하는 탐색기 팝업 메뉴를 추가합니다. [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="5e6fb-432">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="5e6fb-433">사용하려면 탐색기 창에서 Shift 키를 누른 상태로 마우스 오른쪽 단추를 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-433">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="5e6fb-434">Unix 소켓 비차단 동작을 수정합니다. [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-434">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="5e6fb-435">GH 2026에 보고된 것처럼 NETLINK 명령이 중지되는 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-435">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="5e6fb-436">탑재 전파 플래그에 대한 지원이 추가됩니다. [GH 2911]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-436">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="5e6fb-437">자르기가 Inotify 이벤트를 발생시키지 않는 이슈를 해결합니다. [GH 2978]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-437">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="5e6fb-438">wsl.exe가 셸 없이 단일 이진 파일을 호출하는 --exec 옵션이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-438">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="5e6fb-439">wsl.exe가 특정 배포판을 선택하는 --distribution 옵션이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-439">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="5e6fb-440">빌드 17655(앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-440">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="5e6fb-441">빌드 17655에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-441">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-442">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-442">WSL</span></span>
* <span data-ttu-id="5e6fb-443">dmesg에 대한 지원이 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-443">Limited support for dmesg.</span></span> <span data-ttu-id="5e6fb-444">이제 애플리케이션에서 dmesg에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-444">Applications can now log to dmesg.</span></span> <span data-ttu-id="5e6fb-445">WSL 드라이버는 제한된 정보를 dmesg에 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-445">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="5e6fb-446">이후에 드라이버의 다른 정보/진단을 수행하도록 이 기능이 확장될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-446">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="5e6fb-447">참고: dmesg는 현재 `/dev/kmsg` 디바이스 인터페이스를 통해 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-447">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="5e6fb-448">`syslog` syscall 인터페이스는 아직 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-448">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="5e6fb-449">따라서 `-S`, `-C` 같은 `dmesg` 명령줄 옵션 중 일부는 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-449">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="5e6fb-450">파일이 있어도 다중 스레드 작업에서 ENOENT를 반환할 수 있는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-450">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="5e6fb-451">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-451">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="5e6fb-452">빌드 17639(앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-452">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="5e6fb-453">빌드 17639에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-453">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-454">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-454">WSL</span></span>
* <span data-ttu-id="5e6fb-455">네이티브와 일치하도록 직렬 디바이스의 기본 그리드 및 모드를 변경합니다. [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-455">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="5e6fb-456">DrvFs는 이제 확장된 특성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-456">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="5e6fb-457">참고: DrvFs는 확장 특성의 이름에 대한 몇 가지 제한이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-457">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="5e6fb-458">특히 일부 문자(예: '/', ':' 및 '\*')는 허용되지 않으며, 확장 특성 이름은 DrvFs에서 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-458">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="5e6fb-459">빌드 17133(패스트)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-459">Build 17133 (Fast)</span></span>
<span data-ttu-id="5e6fb-460">빌드 17133에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-460">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-461">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-461">WSL</span></span>
* <span data-ttu-id="5e6fb-462">WSL의 중단 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-462">Fix for hang in WSL.</span></span> <span data-ttu-id="5e6fb-463">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-463">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="5e6fb-464">빌드 17128(패스트)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-464">Build 17128 (Fast)</span></span>
<span data-ttu-id="5e6fb-465">빌드 17128에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-465">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-466">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-466">WSL</span></span>
* <span data-ttu-id="5e6fb-467">없음</span><span class="sxs-lookup"><span data-stu-id="5e6fb-467">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="5e6fb-468">빌드 17627(앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-468">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="5e6fb-469">빌드 17627에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-469">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-470">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-470">WSL</span></span>
* <span data-ttu-id="5e6fb-471">futex pi 인식 작업에 대한 지원이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-471">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="5e6fb-472">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-472">[GH 1006]</span></span>
    * <span data-ttu-id="5e6fb-473">우선 순위는 현재 지원되는 WSL 기능이 아니므로 제한이 있지만, 표준 사용의 차단을 해제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-473">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="5e6fb-474">Windows 방화벽은 WSL 프로세스를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-474">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="5e6fb-475">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-475">[GH 1852]</span></span>
    * <span data-ttu-id="5e6fb-476">예를 들어 WSL python 프로세스가 모든 포트에서 수신 대기하도록 허용하려면 관리자 권한 Windows cmd ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-476">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="5e6fb-477">방화벽 규칙을 추가하는 방법에 대한 자세한 내용은 [링크](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-477">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="5e6fb-478">wsl.exe를 사용할 때 사용자의 기본 셸을 준수합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-478">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="5e6fb-479">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-479">[GH 2372]</span></span>
* <span data-ttu-id="5e6fb-480">모든 네트워크 인터페이스를 이더넷으로 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-480">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="5e6fb-481">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-481">[GH 2996]</span></span>
* <span data-ttu-id="5e6fb-482">손상된 /etc/passwd 파일을 보다 효율적으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-482">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="5e6fb-483">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-483">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-484">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-484">Console</span></span>
* <span data-ttu-id="5e6fb-485">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-486">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-486">LTP Results:</span></span>
<span data-ttu-id="5e6fb-487">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-487">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="5e6fb-488">빌드 17618(앞으로 건너뛰기)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-488">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="5e6fb-489">빌드 17618에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-489">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-490">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-490">WSL</span></span>
* <span data-ttu-id="5e6fb-491">NT interop에 대한 pseudoconsole 기능을 도입합니다. [GH 988, 1366, 1433, 1542, 2370, 2406]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-491">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="5e6fb-492">레거시 설치 메커니즘(lxrun.exe)은 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-492">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="5e6fb-493">배포판 설치를 위한 메커니즘은 Microsoft Store를 통해 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-493">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-494">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-494">Console</span></span>
* <span data-ttu-id="5e6fb-495">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-496">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-496">LTP Results:</span></span>
<span data-ttu-id="5e6fb-497">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-497">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="5e6fb-498">빌드 17110</span><span class="sxs-lookup"><span data-stu-id="5e6fb-498">Build 17110</span></span>
<span data-ttu-id="5e6fb-499">빌드 17110에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-499">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-500">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-500">WSL</span></span>
* <span data-ttu-id="5e6fb-501">Windows에서 /init를 종료할 수 있습니다. [GH 2928]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-501">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="5e6fb-502">이제 DrvFs는 기본적으로 디렉터리 단위 대/소문자 구분을 사용합니다(“case=dir” 탑재 옵션과 동일).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-502">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="5e6fb-503">“case=force”(이전 동작)를 사용하려면 레지스트리 키를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-503">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="5e6fb-504">"case=force"를 사용해야 하는 경우 reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1 명령을 실행하여 "case=force"를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-504">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="5e6fb-505">이전 버전의 Windows에서 WSL을 사용하여 만든 기존 디렉터리가 있고 대/소문자를 구분해야 하는 경우 다음 fsutil.exe를 사용하여 대/소문자를 구분하도록 설정합니다. fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="5e6fb-505">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="5e6fb-506">NULL은 uname syscall에서 반환된 문자열을 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-506">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-507">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-507">Console</span></span>
* <span data-ttu-id="5e6fb-508">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-508">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-509">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-509">LTP Results:</span></span>
<span data-ttu-id="5e6fb-510">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-510">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="5e6fb-511">빌드 17107</span><span class="sxs-lookup"><span data-stu-id="5e6fb-511">Build 17107</span></span>
<span data-ttu-id="5e6fb-512">빌드 17107에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-512">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-513">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-513">WSL</span></span>
* <span data-ttu-id="5e6fb-514">마스터 pty 엔드포인트에서 TCSETSF 및 TCSETSW를 지원합니다. [GH 2552]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-514">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="5e6fb-515">동시 interop 프로세스를 시작하면 EINVAL이 발생할 수 있습니다. [GH 2813]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-515">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="5e6fb-516">/proc/pid/status에서 적절한 추적 상태를 표시하도록 PTRACE_ATTACH를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-516">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="5e6fb-517">CLEARTID 및 SETTID 플래그를 모두 사용하여 복제된 단기 프로세스가 TID 주소를 지우지 않고 종료될 수 있는 경합을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-517">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="5e6fb-518">17093 이전 빌드에서 이동할 때 Linux 파일 시스템 디렉터리를 업그레이드하는 동안 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-518">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="5e6fb-519">17093 파일 시스템 변경 내용에 대한 자세한 내용은 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) 릴리스 정보를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-519">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-520">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-520">Console</span></span>
* <span data-ttu-id="5e6fb-521">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-521">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-522">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-522">LTP Results:</span></span>
<span data-ttu-id="5e6fb-523">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-523">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="5e6fb-524">빌드 17101</span><span class="sxs-lookup"><span data-stu-id="5e6fb-524">Build 17101</span></span>
<span data-ttu-id="5e6fb-525">빌드 17101에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-525">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-526">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-526">WSL</span></span>
* <span data-ttu-id="5e6fb-527">signalfd를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-527">Support for signalfd.</span></span> <span data-ttu-id="5e6fb-528">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-528">[GH 129]</span></span>
* <span data-ttu-id="5e6fb-529">지원되지 않는 NTFS 문자가 포함된 파일 이름을 프라이빗 유니코드 문자로 인코딩하여 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-529">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="5e6fb-530">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-530">[GH 1514]</span></span>
* <span data-ttu-id="5e6fb-531">쓰기가 지원되지 않는 경우 자동 탑재는 읽기 전용으로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-531">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="5e6fb-532">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-532">[GH 2603]</span></span>
* <span data-ttu-id="5e6fb-533">유니코드 서로게이트 쌍(예:이모지 문자)을 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-533">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="5e6fb-534">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-534">[GH 2765]</span></span>
* <span data-ttu-id="5e6fb-535">/proc 및 /sys의 의사 파일은 select, poll, epoll 등에서 read and write ready를 반환해야 합니다. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-535">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="5e6fb-536">레지스트리가 변조되거나 손상된 경우 서비스가 무한 루프에 빠질 수 있는 이슈를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-536">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="5e6fb-537">최신 버전의 iproute2(업스트림 4.14)를 사용하도록 netlink 메시지를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-537">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-538">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-538">Console</span></span>
* <span data-ttu-id="5e6fb-539">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-539">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-540">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-540">LTP Results:</span></span>
<span data-ttu-id="5e6fb-541">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-541">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="5e6fb-542">빌드 17093</span><span class="sxs-lookup"><span data-stu-id="5e6fb-542">Build 17093</span></span>
<span data-ttu-id="5e6fb-543">빌드 17093에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-543">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="5e6fb-544">중요:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-544">Important:</span></span>
<span data-ttu-id="5e6fb-545">이 빌드로 업그레이드한 후 처음으로 WSL을 시작할 때 Linux 파일 시스템 디렉터리를 업그레이드하는 작업을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-545">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="5e6fb-546">이 작업은 몇 분 정도 걸릴 수 있으므로 WSL이 느리게 시작되는 것처럼 보일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-546">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="5e6fb-547">이 작업은 스토어에서 설치한 배포판마다 한 번씩만 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-547">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="5e6fb-548">DrvFs의 대/소문자 구분 지원이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-548">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="5e6fb-549">이제 DrvFs는 디렉터리 단위 대/소문자 구분을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-549">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="5e6fb-550">이 새로운 플래그를 디렉터리에 설정하여 해당 디렉터리의 모든 작업을 대/소문자 구분으로 나타낼 수 있으며, 이렇게 하면 Windows 애플리케이션에서도 대/소문자만 다른 파일을 올바르게 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-550">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="5e6fb-551">DrvFs에는 디렉터리 단위로 대/소문자 구분을 제어하는 다음과 같은 새로운 탑재 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-551">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="5e6fb-552">case=force: 모든 디렉터리가 대/소문자 구분으로 처리됩니다(드라이브 루트 제외).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-552">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="5e6fb-553">WSL에서 만든 새 디렉터리는 대/소문자를 구분하는 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-553">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="5e6fb-554">새 디렉터리를 대/소문자 구분으로 표시하는 것만 제외하면 레거시 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-554">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="5e6fb-555">case=dir: 디렉터리 단위 대/소문자 구분 플래그가 있는 디렉터리만 대/소문자 구분으로 처리되고, 다른 디렉터리는 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-555">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="5e6fb-556">WSL에서 만든 새 디렉터리는 대/소문자를 구분하는 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-556">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="5e6fb-557">case=off: 디렉터리 단위 대/소문자 구분 플래그가 있는 디렉터리만 대/소문자 구분으로 처리되고, 다른 디렉터리는 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-557">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="5e6fb-558">WSL로 만든 새 디렉터리는 대/소문자를 구분하지 않는 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-558">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="5e6fb-559">참고: 이전 릴리스의 WSL에서 만든 디렉터리는 이 플래그가 설정되지 않았으므로 "case=dir" 옵션을 사용하는 경우 대/소문자를 구분하는 것으로 간주되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-559">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="5e6fb-560">기존 디렉터리에 이 플래그를 설정하는 방법이 곧 제공될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-560">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="5e6fb-561">이러한 옵션을 사용하는 탑재 예제로는 sudo mount -t drvfs C: /mnt/c -o case=dir이 있습니다(기존 드라이브의 경우 먼저 탑재 해제해야만 다른 옵션으로 탑재 가능).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-561">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="5e6fb-562">현재는 case=force가 여전히 기본 옵션입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-562">For now, case=force is still the default option.</span></span> <span data-ttu-id="5e6fb-563">향후 case=dir로 변경될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-563">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="5e6fb-564">이제 DrvFs를 탑재할 때 Windows 경로에 슬래시를 사용할 수 있습니다(예: sudo mount -t drvfs //server/share /mnt/share).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-564">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="5e6fb-565">이제 인스턴스를 시작하는 동안 WSL에서 /etc/fstab 파일을 처리합니다. [GH 2636]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-565">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="5e6fb-566">이 작업은 DrvFs 드라이브를 자동으로 탑재하기 전에 수행됩니다. fstab을 통해 이미 탑재된 드라이브는 자동으로 다시 탑재되지 않으므로 특정 드라이브의 탑재 지점을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-566">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="5e6fb-567">이 동작은 wsl.conf를 사용하여 해제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-567">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="5e6fb-568">/proc의 mount, mountinfo 및 mountstats 파일은 백슬래시 및 공백과 같은 특수 문자를 적절히 이스케이프합니다. [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-568">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="5e6fb-569">DrvFs를 사용하여 만든 특수 파일(예: WSL 기호화된 링크) 또는 메타데이터를 사용하는 경우 fifos 및 소켓을 이제 Windows에서 복사하여 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-569">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="5e6fb-570">wsl.conf를 사용하여 보다 유연하게 WSL 구성 가능</span><span class="sxs-lookup"><span data-stu-id="5e6fb-570">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="5e6fb-571">하위 시스템을 시작할 때마다 적용되는 WSL의 특정 기능을 자동으로 구성하는 방법이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-571">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="5e6fb-572">여기에는 자동 탑재 옵션 및 네트워크 구성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-572">This includes automount options and network configuration.</span></span> <span data-ttu-id="5e6fb-573">블로그 게시물 https://aka.ms/wslconf 에서 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-573">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="5e6fb-574">AF_UNIX를 사용하면 WSL의 Linux 프로세스와 Windows 네이티브 프로세스 간에 소켓 연결이 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-574">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="5e6fb-575">WSL 및 Windows 애플리케이션은 이제 Unix 소켓을 통해 서로 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-575">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="5e6fb-576">Windows에서 서비스를 실행하고 Windows 및 WSL 앱 모두에서 이 서비스를 제공하려 한다고 가정해 보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-576">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="5e6fb-577">이제 Unix 소켓을 사용하면 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-577">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="5e6fb-578">블로그 게시물 https://aka.ms/afunixinterop 에서 자세히 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-578">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-579">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-579">WSL</span></span>
* <span data-ttu-id="5e6fb-580">MAP_NORESERVE를 통해 mmap() 지원 [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-580">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="5e6fb-581">CLONE_PTRACE 및 CLONE_UNTRACED 지원 [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-581">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="5e6fb-582">복제 시 비-SIGCHLD 종료 신호 처리 [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-582">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="5e6fb-583">/proc/sys/fs/inotify/max_user_instances 및 /proc/sys/fs/inotify/max_user_watches를 스텁합니다. [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-583">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="5e6fb-584">0이 아닌 오프셋이 있는 로드 헤더가 포함된 ELF 이진 파일을 로드하는 동안 오류 발생 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-584">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="5e6fb-585">이미지를 로드할 때 후행 페이지 바이트 삭제</span><span class="sxs-lookup"><span data-stu-id="5e6fb-585">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="5e6fb-586">execve가 자동으로 프로세스를 종료하는 사례 감소</span><span class="sxs-lookup"><span data-stu-id="5e6fb-586">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-587">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-587">Console</span></span>
* <span data-ttu-id="5e6fb-588">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-588">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-589">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-589">LTP Results:</span></span>
<span data-ttu-id="5e6fb-590">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-590">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="5e6fb-591">빌드 17083</span><span class="sxs-lookup"><span data-stu-id="5e6fb-591">Build 17083</span></span>
<span data-ttu-id="5e6fb-592">빌드 17083에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-592">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-593">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-593">WSL</span></span>
* <span data-ttu-id="5e6fb-594">epoll 관련 버그 검사 수정 [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-594">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="5e6fb-595">ASLR을 끄면 중단되는 문제 해결 [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-595">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="5e6fb-596">mmap 작업이 원자성으로 표시되는지 확인 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-596">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-597">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-597">Console</span></span>
* <span data-ttu-id="5e6fb-598">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-598">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-599">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-599">LTP Results:</span></span>
<span data-ttu-id="5e6fb-600">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-600">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="5e6fb-601">빌드 17074</span><span class="sxs-lookup"><span data-stu-id="5e6fb-601">Build 17074</span></span>
<span data-ttu-id="5e6fb-602">빌드 17074에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-602">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-603">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-603">WSL</span></span>
* <span data-ttu-id="5e6fb-604">DrvFs 메타데이터의 스토리지 형식 수정 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-604">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="5e6fb-605">**중요:** 이 빌드 전에 만들어진 DrvFs 메타데이터는 잘못 표시되거나 전혀 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-605">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="5e6fb-606">영향을 받는 파일을 수정하려면 chmod 및 chown을 사용하여 메타데이터를 다시 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-606">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="5e6fb-607">여러 신호 및 다시 시작 가능한 syscall 관련 이슈 해결</span><span class="sxs-lookup"><span data-stu-id="5e6fb-607">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-608">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-608">Console</span></span>
* <span data-ttu-id="5e6fb-609">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-609">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-610">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-610">LTP Results:</span></span>
<span data-ttu-id="5e6fb-611">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-611">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="5e6fb-612">빌드 17063</span><span class="sxs-lookup"><span data-stu-id="5e6fb-612">Build 17063</span></span>
<span data-ttu-id="5e6fb-613">빌드 17063에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-613">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="5e6fb-614">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-614">WSL</span></span>
* <span data-ttu-id="5e6fb-615">DrvFs는 추가 Linux 메타데이터를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-615">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="5e6fb-616">따라서 chmod/chown을 사용하여 파일의 소유자와 모드를 설정할 수 있으며, fifos, unix 소켓, 디바이스 파일 등의 특수 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-616">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="5e6fb-617">이 기능은 아직 실험 중이므로 지금은 기본적으로 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-617">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="5e6fb-618">**참고:**  DrvFs에서 사용하는 메타데이터 형식의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-618">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="5e6fb-619">메타데이터는 이 빌드에서 실험에 사용되지만, 향후 빌드는 이 빌드에서 생성된 메타데이터를 올바르게 읽을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-619">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="5e6fb-620">수정된 파일의 소유자를 수동으로 업데이트하고 사용자 지정 디바이스 ID를 사용하는 디바이스를 다시 만들어야 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-620">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="5e6fb-621">DrvFs를 사용하려면 다음과 같이 메타데이터 옵션으로 DrvFs를 탑재합니다(기존 탑재에서 DrvFs를 사용하려면 먼저 DrvFs를 분리해야 함).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-621">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="5e6fb-622">Linux 권한은 파일에 추가 메타데이터로 추가되며, Windows 권한에 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-622">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="5e6fb-623">Windows 편집기를 사용하여 파일을 편집하면 메타데이터가 제거될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-623">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="5e6fb-624">이 경우 파일이 기본 권한으로 되돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-624">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="5e6fb-625">메타데이터를 사용하지 않고 파일을 제어하는 탑재 옵션이 DrvFs에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-625">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="5e6fb-626">uid: 모든 파일의 소유자에게 사용되는 사용자 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-626">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="5e6fb-627">gid: 모든 파일의 소유자에게 사용되는 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-627">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="5e6fb-628">umask: 모든 파일과 디렉터리에서 제외할 권한의 8진수 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-628">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="5e6fb-629">fmask: 모든 일반 파일에서 제외할 권한의 8진수 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-629">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="5e6fb-630">dmask: 모든 디렉터리에서 제외할 권한의 8진수 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-630">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="5e6fb-631">예:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-631">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="5e6fb-632">메타데이터 없이 파일에 대한 기본 권한을 지정하려면 메타데이터 옵션과 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-632">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="5e6fb-633">WSL과 Win32 간에 환경 변수가 어떻게 흐르는지 구성하는 새 환경 변수 `WSLENV`가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-633">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="5e6fb-634">예:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-634">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="5e6fb-635">`WSLENV`는 WSL의 Win32 또는 Win32 프로세스에서 WSL 프로세스를 시작할 때 포함할 수 있는 콜론으로 구분된 환경 변수 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-635">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="5e6fb-636">각 변수에 슬래시를 접미사로 붙이고 그 뒤에 플래그를 사용하여 변환 방식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-636">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="5e6fb-637">p: 이 값은 WSL 경로와 Win32 경로 간에 변환해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-637">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="5e6fb-638">l: 이 값은 경로 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-638">l: The value is a list of paths.</span></span> <span data-ttu-id="5e6fb-639">WSL에서는 콜론으로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-639">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="5e6fb-640">Win32에서는 세미콜론으로 구분된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-640">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="5e6fb-641">u: 이 값은 Win32에서 WSL을 호출할 때만 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-641">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="5e6fb-642">w: 이 값은 WSL에서 Win32를 호출할 때만 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-642">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="5e6fb-643">.bashrc 또는 사용자 지정 Windows 환경에서 사용자에 대한 `WSLENV`를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-643">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="5e6fb-644">drvfs 탑재는 tar, cp-p의 타임스탬프를 올바르게 유지합니다. (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-644">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="5e6fb-645">drvfs symlink는 올바른 크기를 보고합니다. (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-645">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="5e6fb-646">매우 큰 IO 크기에 대한 읽기/쓰기가 작동합니다. (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-646">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="5e6fb-647">waitpid는 프로세스 그룹 ID와 함께 작동합니다. (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-647">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="5e6fb-648">큰 예약 영역에 대한 mmap 성능이 크게 향상되었습니다. ghc 성능이 향상됩니다. (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-648">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="5e6fb-649">퍼스낼리티에서 READ_IMPLIES_EXEC를 지원합니다. maxima 및 clisp를 수정합니다. (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-649">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="5e6fb-650">mprotect에서 PROT_GROWSDOWN을 지원합니다. clisp를 수정합니다. (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-650">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="5e6fb-651">오버커밋 모드의 페이지 오류를 수정합니다. sbcl을 수정합니다. (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-651">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="5e6fb-652">복제에서 더 많은 플래그 조합을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-652">clone supports more flags combinations</span></span>
* <span data-ttu-id="5e6fb-653">epoll 파일의 select/epoll을 지원합니다(이전에는 no-op).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-653">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="5e6fb-654">ptrace에 구현되지 않은 syscall을 알립니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-654">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="5e6fb-655">resolv.conf 이름 서버를 생성할 때 작동하지 않는 인터페이스를 무시합니다. [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-655">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="5e6fb-656">실제 주소가 없는 네트워크 인터페이스를 열거합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-656">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="5e6fb-657">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-657">[GH 2685]</span></span>
* <span data-ttu-id="5e6fb-658">추가로 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-658">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="5e6fb-659">Windows 기반 개발자가 사용할 수 있는 Linux 도구</span><span class="sxs-lookup"><span data-stu-id="5e6fb-659">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="5e6fb-660">Windows 명령줄 도구 체인에는 bsdtar(tar) 및 curl이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-660">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="5e6fb-661">이 [블로그](https://aka.ms/tarcurlwindows)를 읽고 새로 추가된 이 두 가지 도구에 대해 자세히 살펴보고 두 도구가 Windows에서 어떤 개발자 환경을 제공하는지 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-661">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="5e6fb-662">`AF_UNIX`는 Windows 참가자 SDK(17061+)에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-662">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="5e6fb-663">이 [블로그](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)를 읽고 `AF_UNIX`에 대해 자세히 살펴보고 Windows 기반의 개발자가 어떻게 사용할 수 있는지 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-663">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="5e6fb-664">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-664">Console</span></span>
* <span data-ttu-id="5e6fb-665">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-665">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-666">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-666">LTP Results:</span></span>
<span data-ttu-id="5e6fb-667">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-667">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="5e6fb-668">빌드 17046</span><span class="sxs-lookup"><span data-stu-id="5e6fb-668">Build 17046</span></span>

<span data-ttu-id="5e6fb-669">빌드 17046에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-669">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="5e6fb-670">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-670">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-671">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-671">WSL</span></span>
- <span data-ttu-id="5e6fb-672">활성 터미널 없이 프로세스를 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-672">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="5e6fb-673">[GH 709, 1007, 1511, 2252, 2391 등]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-673">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="5e6fb-674">CLONE_VFORK 및 CLONE_VM에 대한 지원이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-674">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="5e6fb-675">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-675">[GH 1878, 2615]</span></span>
- <span data-ttu-id="5e6fb-676">WSL 네트워킹 작업을 위한 TDI 필터 드라이버를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-676">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="5e6fb-677">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-677">[GH 1554]</span></span>
- <span data-ttu-id="5e6fb-678">특정 조건이 충족되면 DrvFs에서 NT symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-678">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="5e6fb-679">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-679">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="5e6fb-680">연결 대상은 상대 경로여야 하고, 탑재 지점이나 symlink와 교차해서는 안 되며, 존재해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-680">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="5e6fb-681">개발자 모드가 켜져 있지 않으면 사용자에게 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE가 있어야 합니다(일반적으로 관리자 권한으로 wsl.exe를 실행해야 함).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-681">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="5e6fb-682">그 외의 상황에서는 DrvFs가 여전히 WSL symlink를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-682">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="5e6fb-683">관리자 권한 및 비관리자 권한 WSL 인스턴스를 동시에 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-683">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="5e6fb-684">/proc/sys/kernel/yama/ptrace_scope를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-684">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="5e6fb-685">WSL<->Windows 경로를 변환하는 wslpath가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-685">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="5e6fb-686">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-686">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="5e6fb-687">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-687">Console</span></span>
- <span data-ttu-id="5e6fb-688">수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-688">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-689">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-689">LTP Results:</span></span>
<span data-ttu-id="5e6fb-690">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-690">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="5e6fb-691">빌드 17040</span><span class="sxs-lookup"><span data-stu-id="5e6fb-691">Build 17040</span></span>

<span data-ttu-id="5e6fb-692">빌드 17040에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-692">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-693">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-694">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-694">WSL</span></span>
- <span data-ttu-id="5e6fb-695">17035 이후로는 수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-695">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-696">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-696">Console</span></span>
- <span data-ttu-id="5e6fb-697">17035 이후로는 수정 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-697">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-698">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-698">LTP Results:</span></span>
<span data-ttu-id="5e6fb-699">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-699">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="5e6fb-700">빌드 17035</span><span class="sxs-lookup"><span data-stu-id="5e6fb-700">Build 17035</span></span>

<span data-ttu-id="5e6fb-701">빌드 17035에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-701">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-702">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-702">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-703">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-703">WSL</span></span>
- <span data-ttu-id="5e6fb-704">DrvFs의 파일에 액세스할 때 가끔 EINVAL과 함께 액세스가 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-704">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="5e6fb-705">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-705">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-706">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-706">Console</span></span>
- <span data-ttu-id="5e6fb-707">VT 모드에서 줄을 삽입/삭제할 때 일부 색이 손실됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-707">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-708">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-708">LTP Results:</span></span>
<span data-ttu-id="5e6fb-709">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-709">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="5e6fb-710">빌드 17025</span><span class="sxs-lookup"><span data-stu-id="5e6fb-710">Build 17025</span></span>

<span data-ttu-id="5e6fb-711">빌드 17025에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-711">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-712">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-712">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-713">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-713">WSL</span></span>
- <span data-ttu-id="5e6fb-714">새 포그라운드 프로세스 그룹에서 초기 프로세스를 시작합니다. [GH 1653, 2510]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-714">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="5e6fb-715">SIGHUP 전송 픽스 [GH 2496]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-715">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="5e6fb-716">제공된 이름이 없으면 기본 가상 브리지 이름을 생성합니다. [GH 2497]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-716">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="5e6fb-717">/proc/sys/kernel/random/boot_id를 구현합니다. [GH 2518]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-717">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="5e6fb-718">더 많은 interop stdout/stderr 파이프 픽스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-718">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="5e6fb-719">syncfs 시스템 호출을 스텁합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-719">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-720">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-720">Console</span></span>
- <span data-ttu-id="5e6fb-721">타사 콘솔에 대한 입력 VT 변환을 수정합니다. [GH 111]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-721">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-722">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-722">LTP Results:</span></span>
<span data-ttu-id="5e6fb-723">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-723">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="5e6fb-724">빌드 17017</span><span class="sxs-lookup"><span data-stu-id="5e6fb-724">Build 17017</span></span>

<span data-ttu-id="5e6fb-725">빌드 17017에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-725">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-726">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-726">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-727">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-727">WSL</span></span>
- <span data-ttu-id="5e6fb-728">빈 ELF 프로그램 헤더를 무시합니다. [GH 330]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-728">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="5e6fb-729">LxssManager가 비 대화형 사용자에 대한 WSL 인스턴스를 만들도록 허용합니다(ssh 및 예약된 작업 지원). [GH 777, 1602]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-729">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="5e6fb-730">WSL->Win32>WSL("개시") 시나리오를 지원합니다. [GH 1228]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-730">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="5e6fb-731">Interop를 통해 호출되는 콘솔 앱의 종료를 제한적으로 지원합니다. [GH 1614]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-731">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="5e6fb-732">devpts에 대한 탑재 옵션을 지원합니다. [GH 1948]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-732">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="5e6fb-733">Ptrace가 자식 시작을 차단합니다. [GH 2333]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-733">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="5e6fb-734">EPOLLET에 일부 이벤트가 없습니다. [GH 2462]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-734">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="5e6fb-735">PTRACE_GETSIGINFO에 대한 더 많은 데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-735">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="5e6fb-736">lseek를 사용하는 Getdents가 잘못된 결과를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-736">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="5e6fb-737">일부 Win32 interop 앱이 중단되고, 더 이상 데이터가 없는 파이프에서 입력을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-737">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="5e6fb-738">tty/pty 파일에 O_ASYNC가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-738">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="5e6fb-739">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-739">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-740">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-740">Console</span></span>
- <span data-ttu-id="5e6fb-741">이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-741">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-742">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-742">LTP Results:</span></span>
<span data-ttu-id="5e6fb-743">테스트를 진행 중입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-743">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="5e6fb-744">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="5e6fb-744">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="5e6fb-745">빌드 16288</span><span class="sxs-lookup"><span data-stu-id="5e6fb-745">Build 16288</span></span>

<span data-ttu-id="5e6fb-746">빌드 16288에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-746">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-747">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-747">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-748">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-748">WSL</span></span>
- <span data-ttu-id="5e6fb-749">소켓 파일 설명자에 대한 uid, gid 및 모드를 올바르게 초기화하고 보고합니다. [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-749">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="5e6fb-750">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-750">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-751">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-751">Console</span></span>
- <span data-ttu-id="5e6fb-752">이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-752">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-753">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-753">LTP Results:</span></span>
<span data-ttu-id="5e6fb-754">16273 이후로 변경된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-754">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="5e6fb-755">빌드 16278</span><span class="sxs-lookup"><span data-stu-id="5e6fb-755">Build 16278</span></span>

<span data-ttu-id="5e6fb-756">빌드 162738에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-756">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-757">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-757">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-758">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-758">WSL</span></span>
- <span data-ttu-id="5e6fb-759">LX MM 상태를 해제할 때 파일 지원 섹션의 매핑된 보기를 명시적으로 매핑 해제합니다. [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-759">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="5e6fb-760">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-760">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-761">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-761">Console</span></span>
- <span data-ttu-id="5e6fb-762">이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-762">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-763">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-763">LTP Results:</span></span>
<span data-ttu-id="5e6fb-764">16273 이후로 변경된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-764">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="5e6fb-765">빌드 16275</span><span class="sxs-lookup"><span data-stu-id="5e6fb-765">Build 16275</span></span>

<span data-ttu-id="5e6fb-766">빌드 162735에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-766">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-767">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-767">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-768">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-768">WSL</span></span>
- <span data-ttu-id="5e6fb-769">이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-769">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-770">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-770">Console</span></span>
- <span data-ttu-id="5e6fb-771">이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-771">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-772">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-772">LTP Results:</span></span>
<span data-ttu-id="5e6fb-773">16273 이후로 변경된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-773">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="5e6fb-774">빌드 16273</span><span class="sxs-lookup"><span data-stu-id="5e6fb-774">Build 16273</span></span>

<span data-ttu-id="5e6fb-775">빌드 16273에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-775">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-776">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-776">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-777">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-777">WSL</span></span>
- <span data-ttu-id="5e6fb-778">DrvFs에서 가끔 디렉터리의 파일 형식을 잘못 보고하는 이슈가 해결되었습니다. [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-778">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="5e6fb-779">uevent를 사용하는 프로그램의 차단을 해제하는 NETLINK_KOBJECT_UEVENT 소켓을 만들 수 있습니다. [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-779">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="5e6fb-780">비차단 연결에 대한 지원이 추가되었습니다. [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-780">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="5e6fb-781">CLONE_FS 복제 시스템 호출 플래그를 구현했습니다. [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-781">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="5e6fb-782">NT interop에서 탭 또는 따옴표를 올바르게 처리하지 않는 이슈를 해결했습니다. [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-782">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="5e6fb-783">WSL 인스턴스를 다시 시작하려고 할 때 발생하는 액세스 거부 오류를 해결했습니다. [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-783">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="5e6fb-784">futex FUTEX_REQUEUE 및 FUTEX_CMP_REQUEUE 작업을 구현했습니다. [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-784">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="5e6fb-785">다양한 SysFs 파일에 대한 권한을 수정했습니다. [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-785">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="5e6fb-786">설치하는 동안 Haskell 스택이 중단되는 오류를 수정했습니다. [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-786">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="5e6fb-787">binfmt_misc 'C' 'O' 및 'P' 플래그를 구현했습니다. [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-787">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="5e6fb-788">/proc/sys/kernel /shmmax /shmmni 및 /threads-max를 추가했습니다. [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-788">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="5e6fb-789">ioprio_set 시스템 호출에 대한 부분 지원을 추가했습니다. [GH 498]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-789">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="5e6fb-790">SO_REUSEPORT를 스텁하고 netlink 소켓에 대한 SO_PASSCRED 지원이 추가되었습니다. [GH 69]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-790">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="5e6fb-791">현재 배포판을 설치 중이거나 제거 중일 때 RegisterDistribuiton에서 다른 오류 코드를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-791">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="5e6fb-792">wslconfig.exe를 통해 부분적으로 설치된 WSL 배포판을 등록 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-792">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="5e6fb-793">udp::msg_peek에서 python 소켓 테스트가 중단되는 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-793">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="5e6fb-794">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-794">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-795">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-795">Console</span></span>
- <span data-ttu-id="5e6fb-796">이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-796">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-797">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-797">LTP Results:</span></span>
<span data-ttu-id="5e6fb-798">총 테스트: 1904</span><span class="sxs-lookup"><span data-stu-id="5e6fb-798">Total Tests: 1904</span></span><br/>
<span data-ttu-id="5e6fb-799">건너뛴 총 테스트: 209</span><span class="sxs-lookup"><span data-stu-id="5e6fb-799">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="5e6fb-800">총 실패 횟수: 229</span><span class="sxs-lookup"><span data-stu-id="5e6fb-800">Total Failures: 229</span></span><br/>
[<span data-ttu-id="5e6fb-801">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-801">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="5e6fb-802">빌드 16257</span><span class="sxs-lookup"><span data-stu-id="5e6fb-802">Build 16257</span></span>

<span data-ttu-id="5e6fb-803">빌드 16257에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-803">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-804">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-804">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-805">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-805">WSL</span></span>
- <span data-ttu-id="5e6fb-806">prlimit64 시스템 호출을 구현했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-806">Implement prlimit64 system call</span></span>
- <span data-ttu-id="5e6fb-807">ulimit -n에 대한 지원이 추가되었습니다(setrlimit RLIMIT_NOFILE). [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-807">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="5e6fb-808">TCP 소켓에 대한 MSG_MORE를 스텁합니다. [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-808">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="5e6fb-809">잘못된 AT_EXECFN 보조 벡터 동작을 수정합니다. [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-809">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="5e6fb-810">콘솔/tty의 복사/붙여넣기 동작을 수정하고, 보다 효율적인 전체 버퍼 처리를 추가합니다. [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-810">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="5e6fb-811">set-user-ID 및 set-group-ID 프로그램의 보조 벡터에서 AT_SECURE를 설정합니다. [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-811">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="5e6fb-812">Psuedo-terminal 마스터 엔드포인트에서 TIOCPGRP를 처리하지 않습니다. [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-812">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="5e6fb-813">lseek가 LxFs의 디렉터리를 되감는 오류를 수정했습니다. [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-813">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="5e6fb-814">사용량이 많은 후 /dev/ptmx가 잠깁니다. [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-814">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="5e6fb-815">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-815">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-816">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-816">Console</span></span>
- <span data-ttu-id="5e6fb-817">모든 곳에서 가로 선/밑줄을 수정했습니다. [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-817">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="5e6fb-818">프로세스 순서가 변경되면 NPM을 닫기 어려워지는 문제를 수정했습니다. [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-818">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="5e6fb-819">새로운 색 구성표를 추가했습니다(https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/ ).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-819">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-820">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-820">LTP Results:</span></span>
<span data-ttu-id="5e6fb-821">16251 이후로 변경된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-821">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-822">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-822">Syscall Support</span></span>
<span data-ttu-id="5e6fb-823">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-823">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-824">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-824">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="5e6fb-825">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="5e6fb-825">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="5e6fb-826">GitHub 이슈 2392: WSL에서 Windows 폴더를 인식할 수 없음...</span><span class="sxs-lookup"><span data-stu-id="5e6fb-826">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="5e6fb-827">빌드 16257의 경우 WSL에서 `/mnt/c/...` 명령을 통해 Windows 파일/폴더를 열거할 때 이슈가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-827">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="5e6fb-828">이 이슈가 해결되었으며, 2017년 8월 14일부터 일주일 동안 참가자 빌드에서 릴리스해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-828">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="5e6fb-829">빌드 16251</span><span class="sxs-lookup"><span data-stu-id="5e6fb-829">Build 16251</span></span>

<span data-ttu-id="5e6fb-830">빌드 16251에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-830">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-831">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-831">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-832">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-832">WSL</span></span>
- <span data-ttu-id="5e6fb-833">WSL 선택적 구성 요소에서 베타 태그를 제거했습니다. 자세한 내용은 [블로그 게시물](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-833">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="5e6fb-834">exec의 set-user-ID 및 set-group-ID 이진 파일에 대한 saved-set uid 및 gid를 올바르게 초기화합니다. [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-834">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="5e6fb-835">ptrace PTRACE_O_TRACEEXIT에 대한 지원이 추가되었습니다. [GH 555]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-835">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="5e6fb-836">NT_FPREGSET를 사용하는 ptrace PTRACE_GETFPREGS 및 PTRACE_GETREGSET에 대한 지원이 추가되었습니다. [GH 555]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-836">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="5e6fb-837">무시된 신호에서 중지하도록 ptrace를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-837">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="5e6fb-838">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-838">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-839">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-839">Console</span></span>
- <span data-ttu-id="5e6fb-840">이 릴리스에는 콘솔과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-840">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-841">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-841">LTP Results:</span></span>
<span data-ttu-id="5e6fb-842">통과한 테스트 수: 768</span><span class="sxs-lookup"><span data-stu-id="5e6fb-842">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="5e6fb-843">실패한 테스트 수: 244</span><span class="sxs-lookup"><span data-stu-id="5e6fb-843">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="5e6fb-844">건너뛴 테스트 수: 96</span><span class="sxs-lookup"><span data-stu-id="5e6fb-844">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="5e6fb-845">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-845">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="5e6fb-846">빌드 16241</span><span class="sxs-lookup"><span data-stu-id="5e6fb-846">Build 16241</span></span>

<span data-ttu-id="5e6fb-847">빌드 16241에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-847">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-848">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-848">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="5e6fb-849">WSL</span><span class="sxs-lookup"><span data-stu-id="5e6fb-849">WSL</span></span>
- <span data-ttu-id="5e6fb-850">이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-850">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="5e6fb-851">콘솔</span><span class="sxs-lookup"><span data-stu-id="5e6fb-851">Console</span></span>
- <span data-ttu-id="5e6fb-852">교차 줄 DEC에 대해 잘못된 문자를 출력하는 문제가 해결되었으며, 이 문제는 [여기](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)에 처음 보고되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-852">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="5e6fb-853">코드 페이지 65001(utf8)에 출력 텍스트가 표시되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-853">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="5e6fb-854">선택 변경 시 한 색의 RGB 값에 적용한 변경 내용을 색상표의 다른 부분으로 전송하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-854">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="5e6fb-855">이렇게 하면 콘솔 속성 시트를 훨씬 쉽게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-855">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="5e6fb-856">Ctrl+S가 제대로 작동하지 않는 것 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-856">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="5e6fb-857">ANSI 이스케이프 코드에서 Un-Bold/-Dim이 완전히 없어졌습니다. [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-857">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="5e6fb-858">콘솔이 Vim 컬러 테마를 올바르게 지원하지 않습니다. [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-858">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="5e6fb-859">특정 문자를 붙여넣을 수 없습니다. [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-859">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="5e6fb-860">항목이 편집/명령줄에 있는 경우 재배치 크기 조정이 bash 창 크기 조정과 이상하게 상호 작용합니다. [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-860">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="5e6fb-861">Ctrl-L 키를 누르면 화면이 더티 상태로 유지됩니다. [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-861">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="5e6fb-862">HDPI에서 VT를 표시할 때 콘솔 렌더링 버그가 있습니다. [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-862">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="5e6fb-863">유니코드 문자 U+30FB를 사용할 때 일본어 문자가 이상하게 보입니다. [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-863">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="5e6fb-864">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-864">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="5e6fb-865">빌드 16237</span><span class="sxs-lookup"><span data-stu-id="5e6fb-865">Build 16237</span></span>

<span data-ttu-id="5e6fb-866">빌드 16237에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-866">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-867">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-867">Fixed</span></span>
- <span data-ttu-id="5e6fb-868">lxfs에서 EA가 없는 파일에는 기본 특성을 사용합니다(root, root, 0000).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-868">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="5e6fb-869">확장된 특성을 사용하는 배포에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-869">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="5e6fb-870">getdents 및 getdents64에서 반환된 항목의 여백이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-870">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="5e6fb-871">shmctl SHM_STAT 시스템 호출에 대한 권한 확인이 수정되었습니다. [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-871">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="5e6fb-872">ttys에 대한 잘못된 초기 epoll 상태가 수정되었습니다. [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-872">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="5e6fb-873">DrvFs readdir이 일부 항목을 반환하지 않는 문제가 수정되었습니다. [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-873">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="5e6fb-874">파일의 연결이 끊어질 때 발생하는 LxFs readdir 문제가 수정되었습니다. [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-874">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="5e6fb-875">연결되지 않은 drvfs 파일을 procfs를 통해 다시 열 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-875">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="5e6fb-876">WSL 기능을 사용하지 않도록 설정하기 위한 글로벌 레지스트리 키 재정의가 추가되었습니다(interop/드라이브 탑재).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-876">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="5e6fb-877">DrvFs(및 LxFs)에 대한 "통계"의 잘못된 블록 수를 수정했습니다. [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-877">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="5e6fb-878">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-878">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="5e6fb-879">빌드 16232</span><span class="sxs-lookup"><span data-stu-id="5e6fb-879">Build 16232</span></span>

<span data-ttu-id="5e6fb-880">빌드 16232에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-880">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-881">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-881">Fixed</span></span>
- <span data-ttu-id="5e6fb-882">이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-882">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="5e6fb-883">빌드 16226</span><span class="sxs-lookup"><span data-stu-id="5e6fb-883">Build 16226</span></span>

<span data-ttu-id="5e6fb-884">빌드 16226에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-884">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-885">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-885">Fixed</span></span>
- <span data-ttu-id="5e6fb-886">xattr 관련 syscall 지원이 추가되었습니다(getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-886">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="5e6fb-887">security.capablity xattr 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-887">security.capablity xattr support.</span></span>
- <span data-ttu-id="5e6fb-888">비-MS SMB 서버를 비롯한 특정 파일 시스템 및 필터와의 호환성이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-888">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="5e6fb-889">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-889">[GH #1952]</span></span>
- <span data-ttu-id="5e6fb-890">OneDrive 자리 표시자, GVFS 자리 표시자 및 컴팩트 OS 압축 파일에 대한 지원이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-890">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="5e6fb-891">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-891">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="5e6fb-892">빌드 16215</span><span class="sxs-lookup"><span data-stu-id="5e6fb-892">Build 16215</span></span>

<span data-ttu-id="5e6fb-893">빌드 16215에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-893">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-894">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-894">Fixed</span></span>
- <span data-ttu-id="5e6fb-895">WSL에서 더 이상 개발자 모드를 요구하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-895">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="5e6fb-896">drvfs에서 디렉터리 연결을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-896">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="5e6fb-897">WSL 배포 appx 패키지의 제거를 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-897">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="5e6fb-898">프라이빗 및 공유 매핑을 표시하도록 procfs를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-898">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="5e6fb-899">부분적으로 설치 또는 제거된 배포판을 정리하는 wslconfig.exe 기능을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-899">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="5e6fb-900">TCP 소켓에 대한 IP_MTU_DISCOVER 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-900">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="5e6fb-901">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-901">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="5e6fb-902">AF_INADDR 경로에 대한 프로토콜 패밀리를 유추합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-902">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="5e6fb-903">직렬 디바이스가 개선되었습니다. [GH 1929]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-903">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="5e6fb-904">빌드 16199</span><span class="sxs-lookup"><span data-stu-id="5e6fb-904">Build 16199</span></span>

<span data-ttu-id="5e6fb-905">빌드 16199에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-905">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-906">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-906">Fixed</span></span>
- <span data-ttu-id="5e6fb-907">이 릴리스에는 WSL과 관련된 변경 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-907">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="5e6fb-908">빌드 16193</span><span class="sxs-lookup"><span data-stu-id="5e6fb-908">Build 16193</span></span>

<span data-ttu-id="5e6fb-909">빌드 16193에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-909">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-910">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-910">Fixed</span></span>
- <span data-ttu-id="5e6fb-911">SIGCONT 전송과 threadgroup 종료 간의 경합 상태 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-911">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="5e6fb-912">FILE_DEVICE_CONSOLE 대신 FILE_DEVICE_NAMED_PIPE를 보고하도록 tty 및 pty 디바이스를 변경합니다. [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-912">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="5e6fb-913">IP_OPTIONS에 대한 SSH 픽스</span><span class="sxs-lookup"><span data-stu-id="5e6fb-913">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="5e6fb-914">DrvFs 탑재를 Init daemon으로 이동했습니다. [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-914">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="5e6fb-915">DrvFs에 다음 NT symlink에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-915">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="5e6fb-916">빌드 16184</span><span class="sxs-lookup"><span data-stu-id="5e6fb-916">Build 16184</span></span>

<span data-ttu-id="5e6fb-917">빌드 16184에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-917">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-918">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-918">Fixed</span></span>
- <span data-ttu-id="5e6fb-919">apt 패키지 유지 관리 작업(lxrun.exe/update)을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-919">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="5e6fb-920">node.js의 Windows 프로세스에서 출력이 표시되지 않는 문제를 해결했습니다. [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-920">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="5e6fb-921">lxcore의 맞춤 요구 사항이 완화됩니다. [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-921">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="5e6fb-922">여러 시스템 호출에서 AT_EMPTY_PATH 플래그 처리가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-922">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="5e6fb-923">열린 핸들로 DrvFs 파일을 삭제하면 파일이 정의되지 않은 동작을 보이는 이슈가 수정되었습니다. [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-923">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="5e6fb-924">이제 /etc/hosts는 Windows 호스트 파일(%windir%\system32\drivers\etc\hosts)의 항목을 상속합니다. [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-924">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="5e6fb-925">빌드 16179</span><span class="sxs-lookup"><span data-stu-id="5e6fb-925">Build 16179</span></span>

<span data-ttu-id="5e6fb-926">빌드 16179에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-926">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-927">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-927">Fixed</span></span>
- <span data-ttu-id="5e6fb-928">이번 주에는 WSL이 변경되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-928">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="5e6fb-929">빌드 16176</span><span class="sxs-lookup"><span data-stu-id="5e6fb-929">Build 16176</span></span>

<span data-ttu-id="5e6fb-930">빌드 16176에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-930">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-931">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-931">Fixed</span></span>

- [<span data-ttu-id="5e6fb-932">직렬 지원을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-932">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="5e6fb-933">IP 소켓 옵션 IP_OPTIONS가 추가되었습니다. [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-933">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="5e6fb-934">pwritev 함수를 구현했습니다(파일을 nginx/PHP-FPM으로 업로드하는 동안). [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-934">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="5e6fb-935">IP 소켓 옵션 IP_MULTICAST_IF 및 IPV6_MULTICAST_IF가 추가되었습니다. [GH 990]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-935">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="5e6fb-936">소켓 옵션 IP_MULTICAST_LOOP 및 IPV6_MULTICAST_LOOP에 대한 지원이 추가되었습니다. [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-936">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="5e6fb-937">앱 노드, traceroute, dig, nslookup, host에 대한 IP(V6)_MTU 소켓 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-937">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="5e6fb-938">IP 소켓 옵션 IPV6_UNICAST_HOPS가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-938">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="5e6fb-939">파일 시스템이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-939">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="5e6fb-940">UNC 경로 탑재 허용</span><span class="sxs-lookup"><span data-stu-id="5e6fb-940">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="5e6fb-941">drvfs에서 CDFS 지원 사용</span><span class="sxs-lookup"><span data-stu-id="5e6fb-941">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="5e6fb-942">drvfs의 네트워크 파일 시스템에 대한 권한을 올바르게 처리</span><span class="sxs-lookup"><span data-stu-id="5e6fb-942">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="5e6fb-943">drvfs에 원격 드라이브에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="5e6fb-943">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="5e6fb-944">drvfs에서 FAT 지원 사용</span><span class="sxs-lookup"><span data-stu-id="5e6fb-944">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="5e6fb-945">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-945">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-946">LTP 결과</span><span class="sxs-lookup"><span data-stu-id="5e6fb-946">LTP Results</span></span>
<span data-ttu-id="5e6fb-947">15042 이후에는 변경된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-947">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="5e6fb-948">빌드 16170</span><span class="sxs-lookup"><span data-stu-id="5e6fb-948">Build 16170</span></span>

<span data-ttu-id="5e6fb-949">빌드 16170에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-949">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="5e6fb-950">WSL 테스트에 대해 설명하는 새로운 [블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)을 발표했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-950">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="5e6fb-951">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-951">Fixed</span></span>

- <span data-ttu-id="5e6fb-952">소켓 옵션 IP_ADD_MEMBERSHIP 및 IPV6_ADD_MEMBERSHIP를 지원합니다. [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-952">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="5e6fb-953">PTRACE_OLDSETOPTIONS에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-953">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="5e6fb-954">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-954">[GH 1692]</span></span>
- <span data-ttu-id="5e6fb-955">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-955">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-956">LTP 결과</span><span class="sxs-lookup"><span data-stu-id="5e6fb-956">LTP Results</span></span>
<span data-ttu-id="5e6fb-957">15042 이후에는 변경된 내용이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-957">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="5e6fb-958">빌드 15046에서 Windows 10 크리에이터스 업데이트로 변경</span><span class="sxs-lookup"><span data-stu-id="5e6fb-958">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="5e6fb-959">Windows 10 크리에이터스 업데이트에 포함하기로 계획된 WSL 수정 사항 또는 기능이 더 이상 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-959">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="5e6fb-960">WSL 릴리스 정보는 그 다음 주요 Windows 업데이트를 대상으로 하는 추가 기능을 위해 향후 몇 주 이내에 다시 시작될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-960">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="5e6fb-961">빌드 15046 및 향후 참가자 릴리스에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-961">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="5e6fb-962">빌드 15042</span><span class="sxs-lookup"><span data-stu-id="5e6fb-962">Build 15042</span></span>

<span data-ttu-id="5e6fb-963">빌드 15042에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-963">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-964">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-964">Fixed</span></span>

- <span data-ttu-id="5e6fb-965">"..."로 끝나는 경로를 제거할 때 발생하는 교착 상태를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-965">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="5e6fb-966">성공 시 FIONBIO에서 0을 반환하지 않는 이슈를 해결했습니다. [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-966">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="5e6fb-967">inet 데이터 그램 소켓의 길이가 0인 읽기와 관련된 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-967">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="5e6fb-968">drvfs inode lookup의 경합 상태 때문에 발생 가능한 교착 상태를 수정했습니다. [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-968">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="5e6fb-969">unix 소켓 보조 데이터에 대한 지원이 확장되었습니다(SCM_CREDENTIALS 및 SCM_RIGHTS). [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-969">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="5e6fb-970">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-970">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-971">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-971">LTP Results:</span></span>
<span data-ttu-id="5e6fb-972">통과한 테스트 수: 737</span><span class="sxs-lookup"><span data-stu-id="5e6fb-972">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="5e6fb-973">통과하지 못한 테스트 수(실패, 건너뜀 등): 255</span><span class="sxs-lookup"><span data-stu-id="5e6fb-973">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="5e6fb-974">빌드 15031</span><span class="sxs-lookup"><span data-stu-id="5e6fb-974">Build 15031</span></span>

<span data-ttu-id="5e6fb-975">빌드 15031에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-975">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-976">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-976">Fixed</span></span>

- <span data-ttu-id="5e6fb-977">시간(2)이 우발적으로 오작동하는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-977">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="5e6fb-978">\*SIGPROCMASK syscall이 신호 마스크를 손상시킬 수 있는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-978">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="5e6fb-979">이제 WSL 프로세스 만들기 알림에서 전체 명령줄 길이를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-979">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="5e6fb-980">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-980">[GH 1632]</span></span>
- <span data-ttu-id="5e6fb-981">이제 WSL은 GDB 정지에 대해 ptrace를 통해 스레드 종료를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-981">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="5e6fb-982">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-982">[GH 1196]</span></span>
- <span data-ttu-id="5e6fb-983">많은 tmux IO 후에 ptys가 중단되는 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-983">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="5e6fb-984">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-984">[GH 1358]</span></span>
- <span data-ttu-id="5e6fb-985">여러 시스템 호출(futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)의 시간 제한 유효성 검사를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-985">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="5e6fb-986">eventfd EFD_SEMAPHORE 지원이 추가되었습니다. [GH 452]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-986">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="5e6fb-987">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-987">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-988">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-988">LTP Results:</span></span>
<span data-ttu-id="5e6fb-989">통과한 테스트 수: 737</span><span class="sxs-lookup"><span data-stu-id="5e6fb-989">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="5e6fb-990">통과하지 못한 테스트 수(실패, 건너뜀 등): 255</span><span class="sxs-lookup"><span data-stu-id="5e6fb-990">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e6fb-991">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-991">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="5e6fb-992">빌드 15025</span><span class="sxs-lookup"><span data-stu-id="5e6fb-992">Build 15025</span></span>

<span data-ttu-id="5e6fb-993">빌드 15025에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-993">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-994">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-994">Fixed</span></span>

- <span data-ttu-id="5e6fb-995">grep 2.27을 손상시킨 버그를 수정했습니다. [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-995">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="5e6fb-996">eventfd2 syscall에 대한 EFD_SEMAPHORE 플래그를 구현했습니다. [GH 452]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-996">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="5e6fb-997">/proc/[pid]/net/ipv6_route를 구현했습니다. [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-997">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="5e6fb-998">unix 스트림 소켓에 대한 신호 구동 IO 지원이 추가되었습니다. [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-998">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="5e6fb-999">F_GETPIPE_SZ 및 F_SETPIPE_SZ를 지원합니다. [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-999">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="5e6fb-1000">recvmmsg() syscall을 구현했습니다. [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1000">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="5e6fb-1001">epoll_wait()가 대기하지 않는 버그를 수정했습니다. [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1001">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="5e6fb-1002">/proc/version_signature를 구현했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1002">Implement /proc/version_signature</span></span>
- <span data-ttu-id="5e6fb-1003">두 파일 설명자가 같은 파이프를 참조하는 경우 이제 syscall에서 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1003">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="5e6fb-1004">Unix 소켓에 대한 SO_PEERCRED의 올바른 동작을 구현했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1004">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="5e6fb-1005">tkill syscall 잘못된 매개 변수 처리를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1005">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="5e6fb-1006">drvfs의 성능을 높이기 위한 변경 작업을 수행했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1006">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="5e6fb-1007">Ruby IO 차단에 대한 사소한 수정 사항이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1007">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="5e6fb-1008">recvmsg()에서 inet 소켓의 MSG_DONTWAIT 플래그에 대해 EINVAL을 반환하는 문제를 수정했습니다. [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1008">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="5e6fb-1009">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1009">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1010">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1010">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1011">통과한 테스트 수: 732</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1011">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="5e6fb-1012">통과하지 못한 테스트 수(실패, 건너뜀 등): 255</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1012">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e6fb-1013">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1013">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="5e6fb-1014">빌드 15019</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1014">Build 15019</span></span>

<span data-ttu-id="5e6fb-1015">빌드 15019에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1015">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1016">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1016">Fixed</span></span>

- <span data-ttu-id="5e6fb-1017">htop 같은 도구에 대한 procfs에서 CPU 사용량을 잘못 보고하는 버그가 수정되었습니다. (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1017">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="5e6fb-1018">기존 파일에서 O_TRUNC를 사용하여 open()을 호출하면 이제 inotify가 IN_MODIFY를 IN_OPEN보다 먼저 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1018">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="5e6fb-1019">postgress를 사용하도록 unix 소켓 getsockopt SO_ERROR가 수정되었습니다. [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1019">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="5e6fb-1020">GO 언어에 대한 /proc/sys/net/core/somaxconn이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1020">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="5e6fb-1021">이제 Apt-get 패키지 업데이트 백그라운드 작업이 보기에서 숨겨진 상태로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1021">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="5e6fb-1022">ipv6 localhost의 범위를 지웁니다(Spring-Framework(Java) 오류).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1022">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="5e6fb-1023">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1024">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1024">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1025">통과한 테스트 수: 714</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1025">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="5e6fb-1026">통과하지 못한 테스트 수(실패, 건너뜀 등): 249</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1026">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="5e6fb-1027">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="5e6fb-1028">빌드 15014</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1028">Build 15014</span></span>

<span data-ttu-id="5e6fb-1029">빌드 15014에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1029">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1030">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1030">Fixed</span></span>

- <span data-ttu-id="5e6fb-1031">이제 Ctrl+C가 의도한 대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1031">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="5e6fb-1032">이제 htop 및 ps auxw가 올바른 리소스 사용률을 표시합니다. (GH #516)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1032">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="5e6fb-1033">기본적으로 NT 예외를 신호로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1033">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="5e6fb-1034">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1034">(GH #513)</span></span>
- <span data-ttu-id="5e6fb-1035">이제 공간이 부족하면 fallocate가 EINVAL 대신 ENOSPC와 함께 실패합니다. (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1035">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="5e6fb-1036">/proc/sys/kernel/sem이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1036">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="5e6fb-1037">semop 및 semtimedop 시스템 호출이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1037">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="5e6fb-1038">IP_RECVTOS & IPV6_RECVTCLASS 소켓 옵션을 사용하여 nslookup 오류를 수정했습니다. (GH 69)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1038">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="5e6fb-1039">소켓 옵션 IP_RECVTTL 및 IPV6_RECVHOPLIMIT에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1039">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="5e6fb-1040">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1040">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1041">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1041">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1042">통과한 테스트 수: 709</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1042">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="5e6fb-1043">통과하지 못한 테스트 수(실패, 건너뜀 등): 255</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1043">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e6fb-1044">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="5e6fb-1045">Syscall 요약</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1045">Syscall Summary</span></span>
<span data-ttu-id="5e6fb-1046">총 Syscall: 384</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1046">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="5e6fb-1047">총 구현: 235</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1047">Total Implemented: 235</span></span> </br>
<span data-ttu-id="5e6fb-1048">총 스텁: 22</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1048">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="5e6fb-1049">총 미구현: 127</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1049">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="5e6fb-1050">자세한 분석</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1050">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="5e6fb-1051">빌드 15007</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1051">Build 15007</span></span>

<span data-ttu-id="5e6fb-1052">빌드 15007에 대한 일반적인 Windows 정보는 [Windows 블로그]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1052">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="5e6fb-1053">알려진 이슈</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1053">Known Issue</span></span>

- <span data-ttu-id="5e6fb-1054">콘솔에서 일부 Ctrl + <key> 입력을 인식하지 못하는 알려진 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1054">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="5e6fb-1055">여기에는 일반적인 'c' 키누름 역할을 하는 ctrl-c 명령이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1055">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="5e6fb-1056">해결 방법: 대체 키를 Ctrl+C에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1056">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="5e6fb-1057">예를 들어 Ctrl+K를 Ctrl+C에 매핑하려면 `stty intr \^k`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1057">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="5e6fb-1058">이 매핑은 터미널 단위로 수행되며 bash가 시작될 *때마다* 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1058">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="5e6fb-1059">사용자는 옵션을 살펴보고 `.bashrc`에 포함시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1059">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1060">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1060">Fixed</span></span>

- <span data-ttu-id="5e6fb-1061">WSL을 실행하면 CPU 코어를 100% 사용하는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1061">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="5e6fb-1062">소켓 옵션 IP_PKTINFO, IPV6_RECVPKTINFO가 이제 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1062">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="5e6fb-1063">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1063">(GH #851, 987)</span></span>
- <span data-ttu-id="5e6fb-1064">lxcore에서 네트워크 인터페이스 실제 주소를 16바이트로 자릅니다. (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1064">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="5e6fb-1065">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1065">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1066">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1066">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1067">통과한 테스트 수: 709</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1067">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="5e6fb-1068">통과하지 못한 테스트 수(실패, 건너뜀 등): 255</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1068">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="5e6fb-1069">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1069">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="5e6fb-1070">빌드 15002</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1070">Build 15002</span></span>

<span data-ttu-id="5e6fb-1071">빌드 15002에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1071">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="5e6fb-1072">알려진 이슈</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1072">Known Issue</span></span>

<span data-ttu-id="5e6fb-1073">알려진 두 가지 이슈:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1073">Two known issues:</span></span>
- <span data-ttu-id="5e6fb-1074">콘솔에서 일부 Ctrl + <key> 입력을 인식하지 못하는 알려진 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1074">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="5e6fb-1075">여기에는 일반적인 'c' 키누름 역할을 하는 ctrl-c 명령이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1075">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="5e6fb-1076">해결 방법: 대체 키를 Ctrl+C에 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1076">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="5e6fb-1077">예를 들어 Ctrl+K를 Ctrl+C에 매핑하려면 `stty intr \^k`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1077">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="5e6fb-1078">이 매핑은 터미널 단위로 수행되며 bash가 시작될 *때마다* 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1078">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="5e6fb-1079">사용자는 옵션을 살펴보고 `.bashrc`에 포함시킬 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1079">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="5e6fb-1080">WSL이 실행되는 동안 시스템 스레드에서 CPU 코어를 100% 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1080">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="5e6fb-1081">내부적으로 근본 원인을 찾아 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1081">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1082">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1082">Fixed</span></span>

- <span data-ttu-id="5e6fb-1083">이제 모든 bash 세션을 동일한 권한 수준에서 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1083">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="5e6fb-1084">다른 수준에서 세션을 시작하려고 하면 차단됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1084">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="5e6fb-1085">즉, 관리자 콘솔과 비관리자 콘솔을 동시에 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1085">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="5e6fb-1086">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1086">(GH #626)</span></span>
<br/>
- <span data-ttu-id="5e6fb-1087">다음 NETLINK_ROUTE 메시지를 구현했습니다(Windows 관리자 필요).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1087">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="5e6fb-1088">RTM_NEWADDR(`ip addr add` 지원)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1088">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="5e6fb-1089">RTM_NEWROUTE(`ip route add` 지원)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1089">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="5e6fb-1090">RTM_DELADDR(`ip addr del` 지원)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1090">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="5e6fb-1091">RTM_DELROUTE(`ip route del` 지원)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1091">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="5e6fb-1092">업데이트할 패키지의 예약된 작업 확인이 더 이상 요금제 연결에서 실행되지 않습니다. (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1092">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="5e6fb-1093">파이핑이 중단되는 오류(예: bash -c "ls -alR /" | bash -c "cat")를 수정했습니다. (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1093">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="5e6fb-1094">TCP_KEEPCNT 소켓 옵션을 구현했습니다. (GH #843)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1094">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="5e6fb-1095">IP_MTU_DISCOVER INET 소켓 옵션을 구현했습니다. (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1095">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="5e6fb-1096">NT 경로 조회를 사용하여 init에서 NT 이진 파일을 실행하는 레거시 기능을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1096">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="5e6fb-1097">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1097">(GH #1325)</span></span>
- <span data-ttu-id="5e6fb-1098">그룹/기타 읽기 액세스(0644)를 허용하도록 /dev/kmsg 모드를 수정했습니다. (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1098">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="5e6fb-1099">/proc/sys/kernel/random/uuid를 구현했습니다. (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1099">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="5e6fb-1100">프로세스 시작 시간이 2432년으로 표시되는 오류를 수정했습니다. (GH #974)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1100">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="5e6fb-1101">기본 TERM 환경 변수를 xterm-256color로 전환했습니다. (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1101">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="5e6fb-1102">프로세스 포크 중에 프로세스 커밋이 계산되는 방식이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1102">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="5e6fb-1103">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1103">(GH #1286)</span></span>
- <span data-ttu-id="5e6fb-1104">/proc/sys/vm/overcommit_memory를 구현했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1104">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="5e6fb-1105">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1105">(GH #1286)</span></span>
- <span data-ttu-id="5e6fb-1106">/proc/net/route 파일을 구현했습니다. (GH #69)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1106">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="5e6fb-1107">바로 가기 이름이 잘못 번역된 오류를 수정했습니다. (GH #696)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1107">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="5e6fb-1108">프로그램 헤더의 유효성을 잘못 검사하는 elf 구문 분석 논리는 PATH_MAX보다 작거나 같아야 하도록 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1108">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="5e6fb-1109">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1109">(GH #1048)</span></span>
- <span data-ttu-id="5e6fb-1110">procfs, sysfs, cgroupfs 및 binfmtfs에 대한 statfs 콜백을 구현했습니다. (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1110">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="5e6fb-1111">닫히지 않는 AptPackageIndexUpdate 창을 수정했습니다. (GH #1184, GH #1193에서도 설명)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1111">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="5e6fb-1112">ASLR 퍼스낼리티 ADDR_NO_RANDOMIZE 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1112">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="5e6fb-1113">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1113">(GH #1148, 1128)</span></span>
- <span data-ttu-id="5e6fb-1114">AV 중에 gdb 스택을 적절하게 추적하도록 PTRACE_GETSIGINFO, SIGSEGV를 개선했습니다. (GH #875)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1114">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="5e6fb-1115">patchelf 이진 파일에 대한 Elf 구문 분석이 더 이상 실패하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1115">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="5e6fb-1116">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1116">(GH #471)</span></span>
- <span data-ttu-id="5e6fb-1117">VPN DNS가 /etc/resolv.conf로 전파되었습니다. (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1117">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="5e6fb-1118">보다 안정적인 데이터 전송을 위해 TCP 닫기가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1118">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="5e6fb-1119">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1119">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="5e6fb-1120">이제 파일을 너무 많이 열었을 때 올바른 오류 코드가 반환됩니다(EMFILE).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1120">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="5e6fb-1121">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1121">(GH #1126, 2090)</span></span>
- <span data-ttu-id="5e6fb-1122">이제 Windows 감사 로그가 프로세스 만들기 감사에서 이미지 이름을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1122">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="5e6fb-1123">이제 bash 창 내에서 bash.exe를 시작할 때 정상적으로 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1123">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="5e6fb-1124">interop가 LxFs 아래의 작업 디렉터리(예: notepad.exe .bashrc)에 액세스할 수 없는 경우에 표시되는 오류 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1124">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="5e6fb-1125">WSL에서 Windows 경로가 잘리는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1125">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="5e6fb-1126">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1126">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1127">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1127">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1128">통과한 테스트 수: 690</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1128">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="5e6fb-1129">통과하지 못한 테스트 수(실패, 건너뜀 등): 274</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1129">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="5e6fb-1130">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1130">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1131">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1131">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1132">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1132">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1133">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1133">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="5e6fb-1134">빌드 14986</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1134">Build 14986</span></span>

<span data-ttu-id="5e6fb-1135">빌드 14986에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1135">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1136">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1136">Fixed</span></span>

- <span data-ttu-id="5e6fb-1137">Netlink 및 Pty IOCTL의 버그 검사를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1137">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="5e6fb-1138">이제 커널 버전은 Xenial과의 일관성 때문에 4.4.0-43을 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1138">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="5e6fb-1139">이제 입력이 'nul:'로 전달되면 Bash.exe가 시작됩니다. (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1139">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="5e6fb-1140">이제 스레드 ID가 procfs에서 올바르게 보고됩니다. (GH #967)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1140">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="5e6fb-1141">이제 inotify_add_watch()에서 IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 플래그가 지원됩니다. (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1141">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="5e6fb-1142">timer_create 및 관련 시스템 호출이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1142">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="5e6fb-1143">따라서 GHC가 지원됩니다. (GH #307)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1143">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="5e6fb-1144">ping이 0.000ms 시간을 반환하는 이슈를 해결했습니다. (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1144">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="5e6fb-1145">파일을 너무 많이 열었을 때 올바른 오류 코드가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1145">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="5e6fb-1146">인터페이스의 하드웨어 주소가 32바이트인 경우(예: Teredo 인터페이스) 네트워크 인터페이스 데이터에 대한 Netlink 요청이 EINVAL과 함께 실패하는 WSL 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1146">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="5e6fb-1147">Linux "ip" 유틸리티에는 WSL에서 32바이트 하드웨어 주소를 보고하면 충돌하는 버그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1147">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="5e6fb-1148">이것은 WSL이 아니라 "ip"의 버그입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1148">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="5e6fb-1149">“ip” 유틸리티는 하드웨어 주소를 인쇄하는 데 사용되는 문자열 버퍼의 길이를 하드 코딩하는데, 이 버퍼가 너무 작아서 32바이트 하드웨어 주소를 인쇄할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1149">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="5e6fb-1150">그 외에도 여러 문제를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1150">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1151">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1151">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1152">통과한 테스트 수: 669</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1152">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="5e6fb-1153">통과하지 못한 테스트 수(실패, 건너뜀 등): 258</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1153">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="5e6fb-1154">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1154">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1155">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1155">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1156">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1156">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1157">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1157">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="5e6fb-1158">빌드 14971</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1158">Build 14971</span></span>

<span data-ttu-id="5e6fb-1159">빌드 14971에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1159">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1160">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1160">Fixed</span></span>

 - <span data-ttu-id="5e6fb-1161">Microsoft에서 통제할 수 없는 상황으로 인해 이 빌드에는 Linux용 Windows 하위 시스템에 대한 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1161">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="5e6fb-1162">정기적으로 예약된 업데이트는 다음 릴리스에서 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1162">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1163">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1163">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1164">14965에서 변한 것이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1164">Unchanged from 14965</span></span> </br>
<span data-ttu-id="5e6fb-1165">통과한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1165">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="5e6fb-1166">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1167">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="5e6fb-1168">빌드 14965</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1168">Build 14965</span></span>

<span data-ttu-id="5e6fb-1169">빌드 14965에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1169">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1170">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1170">Fixed</span></span>

- <span data-ttu-id="5e6fb-1171">Netlink 소켓 NETLINK_ROUTE 프로토콜의 RTM_GETLINK 및 RTM_GETADDR에 대한 지원이 추가되었습니다. (GH #468)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1171">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="5e6fb-1172">네트워크 열거에 ifconfig 및 ip 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1172">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="5e6fb-1173">자세한 내용은 [WSL 네트워킹 블로그 게시물](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1173">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="5e6fb-1174">/sbin은 이제 기본적으로 사용자의 경로에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1174">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="5e6fb-1175">이제 NT 사용자 경로가 기본적으로 WSL 경로에 추가됩니다. 즉, Linux 경로에 System32를 추가하지 않고 notepad.exe를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1175">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="5e6fb-1176">/proc/sys/kernel/cap_last_cap에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1176">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="5e6fb-1177">현재 작업 디렉터리에 비 ansi 문자가 포함되어 있으면 이제 WSL에서 NT 이진 파일을 시작할 수 있습니다. (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1177">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="5e6fb-1178">연결되지 않은 unix 스트림 소켓에서 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1178">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="5e6fb-1179">PR_GET_PDEATHSIG에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1179">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="5e6fb-1180">CLONE_PARENT에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1180">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="5e6fb-1181">파이핑이 중단되는 오류(예: bash -c "ls -alR /" | bash -c "cat")를 수정했습니다. (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1181">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="5e6fb-1182">현재 터미널에 연결하라는 요청을 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1182">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="5e6fb-1183">/proc/<pid>/oom_score_adj를 쓰기 가능으로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1183">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="5e6fb-1184">/sys/fs/cgroup 폴더를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1184">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="5e6fb-1185">sched_setaffinity는 선호도 비트 마스크 수를 반환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1185">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="5e6fb-1186">인터프리터 경로를 잘못 가정하는 ELF 유효성 검사 논리는 64자 미만이어야 하도록 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1186">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="5e6fb-1187">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1187">(GH #743)</span></span>
- <span data-ttu-id="5e6fb-1188">Open file 설명자는 콘솔 창을 열어 둘 수 있습니다. (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1188">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="5e6fb-1189">rename()이 대상 이름에 후행 슬래시를 사용하여 실패하는 오류를 수정했습니다. (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1189">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="5e6fb-1190">/proc/net/dev 파일을 구현했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1190">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="5e6fb-1191">타이머 해상도로 인한 0.000ms ping을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1191">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="5e6fb-1192">/proc/self/environ을 구현했습니다. (GH #730)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1192">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="5e6fb-1193">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1193">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1194">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1194">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1195">통과한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1195">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="5e6fb-1196">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1196">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1197">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1197">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="5e6fb-1198">빌드 14959</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1198">Build 14959</span></span>

<span data-ttu-id="5e6fb-1199">빌드 14959에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1199">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1200">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1200">Fixed</span></span>

- <span data-ttu-id="5e6fb-1201">Windows에 대한 Pico 프로세스 알림이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1201">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="5e6fb-1202">추가 정보는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1202">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="5e6fb-1203">Windows 상호 운용성 덕분에 안정성이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1203">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="5e6fb-1204">EDP(엔터프라이즈 데이터 보호)를 사용하는 경우 bash.exe를 시작할 때 발생하는 0x80070057 오류를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1204">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="5e6fb-1205">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1205">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1206">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1206">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1207">통과한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1207">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e6fb-1208">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1208">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1209">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1209">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="5e6fb-1210">빌드 14955</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1210">Build 14955</span></span>

<span data-ttu-id="5e6fb-1211">빌드 14955에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1211">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1212">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1212">Fixed</span></span>

 - <span data-ttu-id="5e6fb-1213">Microsoft에서 통제할 수 없는 상황으로 인해 이 빌드에는 Linux용 Windows 하위 시스템에 대한 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1213">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="5e6fb-1214">정기적으로 예약된 업데이트는 다음 릴리스에서 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1214">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1215">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1215">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1216">통과한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1216">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e6fb-1217">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1217">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1218">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1218">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="5e6fb-1219">빌드 14951</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1219">Build 14951</span></span>

<span data-ttu-id="5e6fb-1220">빌드 14951에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1220">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="5e6fb-1221">새 기능: Windows/Ubuntu 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1221">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="5e6fb-1222">이제 WSL 명령줄에서 직접 Windows 이진 파일을 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1222">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="5e6fb-1223">덕분에 사용자는 이전에는 불가능하던 방식으로 Windows 환경 및 시스템과 상호 작용할 수 있게 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1223">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="5e6fb-1224">간단한 예제로, 이제 사용자가 다음 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1224">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="5e6fb-1225">자세한 내용은 아래에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1225">More information can be found at:</span></span>

- [<span data-ttu-id="5e6fb-1226">Interop에 대한 WSL 팀 블로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1226">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="5e6fb-1227">MSDN Interop 설명서</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1227">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1228">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1228">Fixed</span></span>

- <span data-ttu-id="5e6fb-1229">이제 모든 새 WSL 인스턴스에 대해 Ubuntu 16.04(Xenial)가 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1229">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="5e6fb-1230">기존 14.04(Trusty) 인스턴스를 사용하는 사용자는 자동으로 업그레이드되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1230">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="5e6fb-1231">이제 설치 중에 설정된 로캘이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1231">Locale set during install is now displayed</span></span>
- <span data-ttu-id="5e6fb-1232">WSL 프로세스를 파일로 리디렉션하는 기능이 가끔 작동하지 않는 버그를 포함하여 터미널이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1232">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="5e6fb-1233">콘솔 수명은 bash.exe 수명에 연결되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1233">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="5e6fb-1234">콘솔 창 크기는 버퍼 크기가 아닌 가시 크기를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1234">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="5e6fb-1235">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1235">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1236">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1236">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1237">통과한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1237">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e6fb-1238">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1238">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1239">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1239">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="5e6fb-1240">빌드 14946</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1240">Build 14946</span></span>

<span data-ttu-id="5e6fb-1241">빌드 14946에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1241">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1242">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1242">Fixed</span></span>

- <span data-ttu-id="5e6fb-1243">NT 사용자 이름에 공백이나 따옴표가 포함된 사용자에 대한 WSL 사용자 계정을 만들 수 없는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1243">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="5e6fb-1244">통계에서 디렉터리의 링크 수로 0을 반환하도록 VolFs 및 DrvFs를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1244">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="5e6fb-1245">IPV6_MULTICAST_HOPS 소켓 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1245">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="5e6fb-1246">tty당 단일 콘솔 I/O 루프로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1246">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="5e6fb-1247">예: 다음 명령을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1247">Example: the following command is possible:</span></span>
  - <span data-ttu-id="5e6fb-1248">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1248">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="5e6fb-1249">공백을 /proc/cpuinfo의 탭으로 바꿉니다. (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1249">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="5e6fb-1250">이제 DrvFs는 탑재된 Windows 볼륨과 일치하는 이름으로 mountinfo에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1250">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="5e6fb-1251">이제 /home 및 /root가 올바른 이름으로 mountinfo에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1251">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="5e6fb-1252">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1252">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1253">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1253">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1254">통과한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1254">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e6fb-1255">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1255">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1256">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1256">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="5e6fb-1257">빌드 14942</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1257">Build 14942</span></span>

<span data-ttu-id="5e6fb-1258">빌드 14942에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/onefourninefourtwoooooo)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1258">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1259">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1259">Fixed</span></span>

- <span data-ttu-id="5e6fb-1260">SSH를 차단하는 “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” 네트워킹 충돌을 포함하여 여러 버그 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1260">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="5e6fb-1261">현재 DrvFs가 있는 Windows 애플리케이션에서 생성된 알림에 inotifiy가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1261">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="5e6fb-1262">mongod에 대한 TCP_KEEPIDLE 및 TCP_KEEPINTVL이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1262">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="5e6fb-1263">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1263">(GH #695)</span></span>
- <span data-ttu-id="5e6fb-1264">pivot_root 시스템 호출이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1264">Implement the pivot_root system call</span></span>
- <span data-ttu-id="5e6fb-1265">SO_DONTROUTE에 대한 소켓 옵션이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1265">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="5e6fb-1266">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1266">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1267">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1267">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1268">통과한 테스트 수: 665</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1268">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="5e6fb-1269">통과하지 못한 테스트 수(실패, 건너뜀 등): 263</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1269">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="5e6fb-1270">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1270">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1271">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1271">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1272">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1272">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1273">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1273">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="5e6fb-1274">빌드 14936</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1274">Build 14936</span></span>

<span data-ttu-id="5e6fb-1275">빌드 14936에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1275">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="5e6fb-1276">참고: 향후 릴리스에서 WSL은 Ubuntu 14.04(Trusty) 대신 Ubuntu 16.04(Xenial)를 설치할 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1276">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="5e6fb-1277">이 변경 내용은 새 인스턴스를 설치하는(lxrun.exe /install 또는 bash.exe를 처음으로 실행) 참가자에게 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1277">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="5e6fb-1278">Trusty를 사용하는 기존 인스턴스는 자동으로 업그레이드되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1278">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="5e6fb-1279">사용자는 do-release-upgrade 명령을 사용하여 Trusty 이미지를 Xenial로 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1279">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="5e6fb-1280">알려진 이슈</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1280">Known Issue</span></span>
<span data-ttu-id="5e6fb-1281">WSL에서 일부 소켓 구현에 이슈가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1281">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="5e6fb-1282">버그 검사는 “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” 오류와 함께 자신을 충돌로 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1282">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="5e6fb-1283">이 이슈의 가장 일반적인 징후는 ssh를 사용할 때 발생하는 충돌입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1283">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="5e6fb-1284">근본 원인은 내부 빌드에서 수정되었으며, 기회가 되는 대로 참가자에게 푸시할 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1284">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1285">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1285">Fixed</span></span>

- <span data-ttu-id="5e6fb-1286">chroot 시스템 호출이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1286">Implemented the chroot system call</span></span>
- <span data-ttu-id="5e6fb-1287">현재 ~~DrvFs의 Windows 애플리케이션에서 생성된 알림에 대한 지원을 포함하여~~ inotifiy가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1287">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="5e6fb-1288">수정 사항: Windows 애플리케이션에서 시작된 변경 내용에 대한 Inotify 지원은 현재 제공되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1288">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="5e6fb-1289">IPV6에 대한 소켓 바인딩:<port n> 이제 IPV6_V6ONLY를 지원합니다. (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1289">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="5e6fb-1290">waitid systemcall에 대한 WNOWAIT 동작이 구현되었습니다. (GH #638)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1290">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="5e6fb-1291">IP 소켓 옵션 IP_HDRINCL 및 IP_TTL에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1291">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="5e6fb-1292">길이가 0인 read()는 즉시 반환되어야 합니다. (GH #975).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1292">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="5e6fb-1293">.tar 파일에 NULL 종결자가 포함되지 않은 파일 이름 및 파일 이름 접두사를 올바르게 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1293">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="5e6fb-1294">/dev/snull에 epoll이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1294">epoll support for /dev/null</span></span>
- <span data-ttu-id="5e6fb-1295">/dev/alarm 시간 원본이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1295">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="5e6fb-1296">이제 Bash -c가 파일로 리디렉션할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1296">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="5e6fb-1297">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1297">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1298">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1298">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1299">통과한 테스트 수: 664</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1299">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="5e6fb-1300">통과하지 못한 테스트 수(실패, 건너뜀 등): 264</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1300">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="5e6fb-1301">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1301">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1302">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1302">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1303">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1303">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1304">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1304">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="5e6fb-1305">빌드 14931</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1305">Build 14931</span></span>

<span data-ttu-id="5e6fb-1306">빌드 14931에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1306">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1307">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1307">Fixed</span></span>

 - <span data-ttu-id="5e6fb-1308">Microsoft에서 통제할 수 없는 상황으로 인해 이 빌드에는 Linux용 Windows 하위 시스템에 대한 업데이트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1308">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="5e6fb-1309">정기적으로 예약된 업데이트는 다음 릴리스에서 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1309">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="5e6fb-1310">빌드 14926</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1310">Build 14926</span></span>

<span data-ttu-id="5e6fb-1311">빌드 14926에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1311">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1312">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1312">Fixed</span></span>

- <span data-ttu-id="5e6fb-1313">이제 Ping은 관리자 권한이 없는 콘솔에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1313">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="5e6fb-1314">이제 Ping6가 지원되며, 관리자 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1314">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="5e6fb-1315">WSL을 통해 수정된 파일에 Inotify가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1315">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="5e6fb-1316">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1316">(GH #216)</span></span>
  - <span data-ttu-id="5e6fb-1317">지원되는 플래그:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1317">Flags supported:</span></span>
    - <span data-ttu-id="5e6fb-1318">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1318">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="5e6fb-1319">inotify_add_watch 이벤트: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1319">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="5e6fb-1320">inotify_add_watch 특성: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1320">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="5e6fb-1321">출력 읽기: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1321">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="5e6fb-1322">알려진 이슈: Windows 애플리케이션의 파일을 수정해도 이벤트가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1322">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="5e6fb-1323">이제 Unix 소켓이 SCM_CREDENTIALS를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1323">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="5e6fb-1324">LTP 결과:</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1324">LTP Results:</span></span>
<span data-ttu-id="5e6fb-1325">통과한 테스트 수: 651</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1325">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="5e6fb-1326">통과하지 못한 테스트 수(실패, 건너뜀 등): 258</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1326">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="5e6fb-1327">LTP 테스트 실행 로그</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1327">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="5e6fb-1328">빌드 14915</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1328">Build 14915</span></span>

<span data-ttu-id="5e6fb-1329">빌드 14915에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1329">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1330">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1330">Fixed</span></span>
-  <span data-ttu-id="5e6fb-1331">unix 데이터 그램 소켓용 Socketpair가 제공됩니다. (GH #262)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1331">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="5e6fb-1332">SO_REUSEADDR에 Unix 소켓이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1332">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="5e6fb-1333">SO_BROADCAST에 UNIX 소켓이 지원됩니다. (GH #568)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1333">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="5e6fb-1334">SOCK_SEQPACKET에 Unix 소켓이 지원됩니다. (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1334">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="5e6fb-1335">unix 데이터 그램 전송, 수신 및 종료에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1335">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="5e6fb-1336">고정되지 않은 주소에 대한 잘못된 mmap 매개 변수 유효성 검사로 인한 버그 검사를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1336">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="5e6fb-1337">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1337">(GH #847)</span></span>
- <span data-ttu-id="5e6fb-1338">터미널 상태의 일시 중단/다시 시작을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1338">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="5e6fb-1339">화면 유틸리티의 차단을 해제하는 TIOCPKT ioctl을 지원합니다. (GH #774)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1339">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="5e6fb-1340">알려진 이슈: 기능 키가 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1340">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="5e6fb-1341">해제된 멤버 'ReaderReady'에 LxpTimerFdWorkerRoutine이 액세스할 수 있게 되는 원인인 TimerFd의 경합을 수정했습니다. (GH #814)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1341">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="5e6fb-1342">futex, poll 및 clock_nanosleep에 대한 다시 시작 가능한 시스템 호출을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1342">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="5e6fb-1343">바인드 탑재 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1343">Added bind mount support</span></span>
- <span data-ttu-id="5e6fb-1344">탑재 네임스페이스 지원에 대한 공유가 해제되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1344">unshare for mount namespace support</span></span>
    - <span data-ttu-id="5e6fb-1345">알려진 이슈: `unshare(CLONE_NEWNS)`를 사용하여 새 탑재 네임스페이스를 만들 때 현재 작업 디렉터리는 이전 네임스페이스를 계속 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1345">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="5e6fb-1346">추가적으로 기능이 개선되고 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1346">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="5e6fb-1347">빌드 14905</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1347">Build 14905</span></span>

<span data-ttu-id="5e6fb-1348">빌드 14905에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1348">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1349">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1349">Fixed</span></span>
- <span data-ttu-id="5e6fb-1350">다시 시작 가능한 시스템 호출이 이제 지원됩니다. (GH #349, GH #520).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1350">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="5e6fb-1351">/로 끝나는 디렉터리에 대한 Symlink가 이제 작동합니다. (GH #650)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1351">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="5e6fb-1352">/dev/random에 대한 RNDGETENTCNT ioctl이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1352">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="5e6fb-1353">/proc/[pid]/mounts, /proc/[pid]/mountinfo 및 /proc/[pid]/mountstats 파일이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1353">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="5e6fb-1354">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1354">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="5e6fb-1355">빌드 14901</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1355">Build 14901</span></span>
<span data-ttu-id="5e6fb-1356">Windows 10 1주년 업데이트 이후에 출시된 첫 번째 참가자 빌드입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1356">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="5e6fb-1357">빌드 14901에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1357">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1358">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1358">Fixed</span></span>
- <span data-ttu-id="5e6fb-1359">후행 슬래시 이슈를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1359">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="5e6fb-1360">이제 `$ mv a/c/ a/b/` 같은 명령이 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1360">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="5e6fb-1361">이제 설치 시 Ubuntu 로캘을 Windows 로캘로 설정해야 하는지 여부를 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1361">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="5e6fb-1362">ns 폴더에 procfs가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1362">Procfs support for ns folder</span></span>
- <span data-ttu-id="5e6fb-1363">tmpfs, procfs 및 sysfs 파일 시스템에 탑재 및 탑재 해제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1363">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="5e6fb-1364">mknod[at] 32비트 ABI 서명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1364">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="5e6fb-1365">Unix 소켓이 디스패치 모델로 전환되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1365">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="5e6fb-1366">setsockopt를 사용하여 설정된 INET 소켓 수신 버퍼 크기를 준수해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1366">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="5e6fb-1367">MSG_CMSG_CLOEXEC unix 소켓 수신 메시지 플래그가 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1367">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="5e6fb-1368">Linux 프로세스 stdin/stdout 파이프 리디렉션 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1368">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="5e6fb-1369">CMD에서 bash -c 명령을 파이핑할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1369">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="5e6fb-1370">예:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1370">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="5e6fb-1371">이제 여러 개의 페이지 파일이 있는 시스템에 Bash를 설치할 수 있습니다. (GH #538, #358).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1371">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="5e6fb-1372">기본 INET 소켓 버퍼 크기가 기본 Ubuntu 설정의 크기와 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1372">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="5e6fb-1373">xattr syscall을 listxattr에 맞춥니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1373">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="5e6fb-1374">SIOCGIFCONF의 유효한 IPv4 주소가 있는 인터페이스만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1374">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="5e6fb-1375">ptrace에서 삽입할 때 신호 기본 작업을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1375">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="5e6fb-1376">/proc/sys/vm/min_free_kbytes가 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1376">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="5e6fb-1377">sigreturn에서 컨텍스트를 복원할 때 머신 컨텍스트 레지스터 값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1377">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="5e6fb-1378">이렇게 하면 일부 사용자의 java 및 javac가 중단되는 이슈를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1378">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="5e6fb-1379">/proc/sys/kernel/hostname이 구현되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1379">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1380">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1380">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1381">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1381">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1382">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1382">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="5e6fb-1383">빌드 14388에서 Windows 10 1주년 업데이트로 전환</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1383">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="5e6fb-1384">빌드 14388에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/14388wip)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1384">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1385">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1385">Fixed</span></span>
- <span data-ttu-id="5e6fb-1386">8월 2일에 Windows 10 1주년 업데이트를 준비하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1386">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="5e6fb-1387">1주년 업데이트의 WSL에 대한 자세한 내용은 [블로그](https://blogs.msdn.microsoft.com/wsl/)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1387">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="5e6fb-1388">빌드 14376</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1388">Build 14376</span></span>
<span data-ttu-id="5e6fb-1389">빌드 14376에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1389">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1390">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1390">Fixed</span></span>
- <span data-ttu-id="5e6fb-1391">apt-get이 중단되는 일부 인스턴스를 제거했습니다. (GH #493)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1391">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="5e6fb-1392">빈 탑재가 올바르게 처리되지 않는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1392">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="5e6fb-1393">ramdisks가 올바르게 탑재되지 않는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1393">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="5e6fb-1394">플래그를 지원하도록 unix 소켓 수용이 변경되었습니다. (부분 GH #451)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1394">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="5e6fb-1395">일반적인 네트워크 관련 블루스크린이 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1395">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="5e6fb-1396">/proc/[pid]/task에 액세스할 때 블루스크린이 발생하는 문제를 해결했습니다. (GH #523)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1396">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="5e6fb-1397">일부 pty 시나리오에서 CPU 사용률이 높은 문제를 해결했습니다. (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1397">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="5e6fb-1398">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1398">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="5e6fb-1399">빌드 14371</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1399">Build 14371</span></span>
<span data-ttu-id="5e6fb-1400">빌드 14371에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1400">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1401">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1401">Fixed</span></span>
- <span data-ttu-id="5e6fb-1402">ptrace를 사용할 때 SIGCHLD 및 wait()를 사용하여 타이밍 경합을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1402">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="5e6fb-1403">경로에 후행 /가 있을 때 발생하는 몇 가지 동작을 수정했습니다. (GH #432)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1403">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="5e6fb-1404">자식에 대한 열린 핸들로 인해 이름 바꾸기/연결 해제가 실패하는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1404">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="5e6fb-1405">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1405">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="5e6fb-1406">빌드 14366</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1406">Build 14366</span></span>
<span data-ttu-id="5e6fb-1407">빌드 14366에 대한 일반적인 Windows 정보는 [Windows 블로그](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1407">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1408">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1408">Fixed</span></span>
- <span data-ttu-id="5e6fb-1409">symlink를 통한 파일 만들기를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1409">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="5e6fb-1410">Python에 대한 listxattr을 추가했습니다. (GH 385)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1410">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="5e6fb-1411">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1411">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1412">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1412">Syscall Support</span></span>
-   <span data-ttu-id="5e6fb-1413">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1413">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1414">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1414">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="5e6fb-1415">빌드 14361</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1415">Build 14361</span></span>
<span data-ttu-id="5e6fb-1416">빌드 14361에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14361)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1416">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1417">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1417">Fixed</span></span>
- <span data-ttu-id="5e6fb-1418">이제 DrvFs는 Windows 기반의 Ubuntu에서 Bash로 실행될 때 대/소문자를 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1418">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="5e6fb-1419">사용자는 /mnt/c 드라이브에서 case.txt 및 CASE.TXT를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1419">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="5e6fb-1420">대/소문자 구분은 Windows 기반 Ubuntu의 Bash 내에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1420">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="5e6fb-1421">Bash 외부에 있는 경우 NTFS가 파일을 올바르게 보고하지만, 예기치 않은 동작이 발생하여 Windows의 파일과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1421">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="5e6fb-1422">각 볼륨의 루트(/mnt/c)는 대/소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1422">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="5e6fb-1423">Windows에서 이러한 파일을 처리하는 방법에 대한 자세한 내용은 [여기](https://support.microsoft.com/en-us/kb/100625)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1423">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="5e6fb-1424">pty/tty 지원이 대폭 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1424">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="5e6fb-1425">이제 TMUX 같은 애플리케이션이 지원됩니다. (GH #40)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1425">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="5e6fb-1426">가끔 사용자 계정이 만들어지지 않는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1426">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="5e6fb-1427">매우 긴 인수 목록을 허용하도록 명령줄 인수 구조를 최적화했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1427">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="5e6fb-1428">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1428">(GH #153)</span></span>
- <span data-ttu-id="5e6fb-1429">이제 DrvFs의 read_only 파일을 삭제하고 chmod할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1429">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="5e6fb-1430">연결이 끊어질 때 터미널이 중단되는 일부 인스턴스를 수정했습니다. (GH #43)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1430">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="5e6fb-1431">이제 chmod 및 chown이 tty 디바이스에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1431">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="5e6fb-1432">0\.0.0.0 및 ::에 localhost로 연결할 수 있습니다. (GH #388)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1432">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="5e6fb-1433">이제 Sendmsg/recvmsg는 1보다 큰 IO 벡터 길이를 처리합니다. (부분 GH #376)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1433">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="5e6fb-1434">이제 사용자는 자동 생성된 호스트 파일을 옵트아웃할 수 있습니다. (GH #398)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1434">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="5e6fb-1435">설치하는 동안 자동으로 Linux 로캘을 NT 로캘에 연결합니다. (GH #11)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1435">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="5e6fb-1436">/proc/sys/vm/swappiness 파일이 추가되었습니다. (GH #306)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1436">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="5e6fb-1437">이제 strace가 올바르게 종료됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1437">strace now exits correctly</span></span>
- <span data-ttu-id="5e6fb-1438">/proc/self/fd를 통해 파이프를 다시 열 수 있습니다. (GH #222)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1438">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="5e6fb-1439">DrvFs에서 %LOCALAPPDATA%\lxss 아래에 디렉터리를 숨깁니다. (GH #270)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1439">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="5e6fb-1440">bash.exe ~를 보다 효율적으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1440">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="5e6fb-1441">이제 “bash ~ -c ls” 같은 명령이 지원됩니다. (GH #467)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1441">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="5e6fb-1442">이제 종료하는 동안 소켓이 epoll 읽기를 사용할 수 있음을 알립니다. (GH #271).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1442">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="5e6fb-1443">lxrun /uninstall이 파일 및 폴더 삭제를 보다 효율적으로 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1443">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="5e6fb-1444">ps -f를 수정했습니다. (GH #246)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1444">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="5e6fb-1445">xEmacs 같은 x11 앱에 대한 지원이 개선되었습니다. (GH #481)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1445">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="5e6fb-1446">기본 Ubuntu 설정과 일치하고 get_rlimit syscall에 올바른 크기를 보고하도록 초기 스레드 스택 크기를 업데이트했습니다. (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1446">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="5e6fb-1447">pico 프로세스 이미지 이름의 보고 기능을 개선했습니다(예: 감사).</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1447">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="5e6fb-1448">df 명령에 대한 /proc/mountinfo를 구현했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1448">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="5e6fb-1449">자식 이름에 대한 symlink 오류 코드를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1449">Fixed symlink error code for child name .</span></span> <span data-ttu-id="5e6fb-1450">그리고 ...</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1450">and ..</span></span>
- <span data-ttu-id="5e6fb-1451">버그 및 기능이 추가로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1451">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1452">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1452">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1453">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1453">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1454">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1454">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="5e6fb-1455">빌드 14352</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1455">Build 14352</span></span>
<span data-ttu-id="5e6fb-1456">빌드 14352에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14352)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1456">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1457">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1457">Fixed</span></span>
- <span data-ttu-id="5e6fb-1458">대용량 파일이 올바르게 다운로드/생성되지 않는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1458">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="5e6fb-1459">이제 npm 및 기타 시나리오의 차단을 해제해도 됩니다. (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1459">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="5e6fb-1460">소켓이 중단되는 일부 인스턴스를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1460">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="5e6fb-1461">일부 ptrace 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1461">Corrected some ptrace errors</span></span>
- <span data-ttu-id="5e6fb-1462">255자보다 긴 파일 이름을 허용하는 WSL 이슈를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1462">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="5e6fb-1463">영어가 아닌 문자에 대한 지원이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1463">Improved support for non-English characters</span></span>
- <span data-ttu-id="5e6fb-1464">현재 Windows 표준 시간대 데이터를 추가하고 기본값으로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1464">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="5e6fb-1465">각 탑재 지점에 대한 고유한 디바이스 id (jre 픽스 – GH #49)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1465">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="5e6fb-1466">"." 및</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1466">Correct issue with paths containing “.”</span></span> <span data-ttu-id="5e6fb-1467">“..”가 포함된 경로 이슈를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1467">and “..”</span></span>
- <span data-ttu-id="5e6fb-1468">Fifo 지원이 추가되었습니다. (GH #71)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1468">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="5e6fb-1469">네이티브 Ubuntu 형식과 일치하도록 resolv.conf 형식을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1469">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="5e6fb-1470">일부 procfs를 정리했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1470">Some procfs cleanup</span></span>
- <span data-ttu-id="5e6fb-1471">관리자 콘솔에 ping을 사용합니다. (GH #18)</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1471">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1472">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1472">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1473">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1473">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1474">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1474">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="5e6fb-1475">빌드 14342</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1475">Build 14342</span></span>
<span data-ttu-id="5e6fb-1476">빌드 14342에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14342)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1476">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="5e6fb-1477">VolFs 및 DriveFs에 대한 정보는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1477">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1478">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1478">Fixed</span></span>
- <span data-ttu-id="5e6fb-1479">Windows 사용자의 사용자 이름에 유니코드 문자가 있을 때 발생하는 설치 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1479">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="5e6fb-1480">이제 FAQ의 apt-get update udev 해결 방법이 첫 번째 실행 시 기본적으로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1480">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="5e6fb-1481">DriveFs(/mnt/<drive>) 디렉터리에서 symlink를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1481">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="5e6fb-1482">이제 symlink가 DriveFs와 VolFs 간에 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1482">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="5e6fb-1483">최상위 경로 구문 분석 이슈를 해결했습니다. 이제 ls .//가 예상대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1483">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="5e6fb-1484">이제 DriveFs의 npm 설치와 -g 옵션이 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1484">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="5e6fb-1485">PHP 서버가 시작되지 않는 이슈를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1485">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="5e6fb-1486">네이티브 Ubuntu와 보다 가깝게 일치하도록 $PATH 같은 기본 환경 변수를 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1486">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="5e6fb-1487">apt 패키지 캐시를 업데이트하기 위한 주간 유지 관리 작업이 Windows에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1487">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="5e6fb-1488">ELF 헤더 유효성 검사와 관련된 이슈를 해결했습니다. 이제 WSL은 모든 Melkor 옵션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1488">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="5e6fb-1489">Zsh 셸이 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1489">Zsh shell is functional</span></span>
- <span data-ttu-id="5e6fb-1490">미리 컴파일된 Go 이진 파일이 이제 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1490">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="5e6fb-1491">Bash.exe 첫 실행에 대한 메시지가 이제 올바르게 번역되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1491">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="5e6fb-1492">이제 /proc/meminfo에서 올바른 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1492">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="5e6fb-1493">이제 VFS에서 소켓이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1493">Sockets now supported in VFS</span></span>
- <span data-ttu-id="5e6fb-1494">이제 /dev가 tempfs로 탑재됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1494">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="5e6fb-1495">이제 Fifo가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1495">Fifo now supported</span></span>
- <span data-ttu-id="5e6fb-1496">이제 다중 코어 시스템이 /proc/cpuinfo에 올바르게 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1496">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="5e6fb-1497">첫 번째 실행에서 다운로드와 관련된 기능이 개선되고 오류 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1497">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="5e6fb-1498">Syscall 및 버그 픽스가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1498">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="5e6fb-1499">아래 syscall 목록이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1499">Supported syscall list below.</span></span>
- <span data-ttu-id="5e6fb-1500">그 외에도 여러 버그를 수정하고 기능을 개선했습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1500">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="5e6fb-1501">알려진 문제</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1501">Known Issues</span></span>
- <span data-ttu-id="5e6fb-1502">경우에 따라 DriveFs에서 ‘..’가</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1502">Not resolving ‘..’</span></span> <span data-ttu-id="5e6fb-1503">올바르게 확인되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1503">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1504">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1504">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1505">아래는 WSL에서 일부가 구현된 새 syscall 또는 향상된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1505">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1506">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1506">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="5e6fb-1507">빌드 14332</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1507">Build 14332</span></span>

<span data-ttu-id="5e6fb-1508">빌드 14332에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14332)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1508">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="5e6fb-1509">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1509">Fixed</span></span>
- <span data-ttu-id="5e6fb-1510">DNS 항목 우선 순위 지정을 포함하여 resolv.conf 생성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1510">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="5e6fb-1511">/mnt 드라이브와 비-/mnt 드라이브 간에 파일 및 디렉터리를 이동할 때 발생하는 이슈</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1511">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="5e6fb-1512">이제 symlink를 사용하여 Tar 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1512">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="5e6fb-1513">인스턴스를 만들 때 기본 /run/lock 디렉터리가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1513">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="5e6fb-1514">적절한 통계 정보를 반환하도록 /dev/null이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1514">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="5e6fb-1515">처음 실행하는 동안 다운로드할 때 추가 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1515">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="5e6fb-1516">Syscall 및 버그 픽스가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1516">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="5e6fb-1517">아래 syscall 목록이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1517">Supported syscall list below.</span></span>
- <span data-ttu-id="5e6fb-1518">버그 및 기능이 추가로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1518">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1519">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1519">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1520">다음은 WSL에서 일부가 구현된 새 syscall입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1520">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="5e6fb-1521">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1521">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="5e6fb-1522">빌드 14328</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1522">Build 14328</span></span>

<span data-ttu-id="5e6fb-1523">빌드 14332에 대한 일반적인 Windows 정보는 [Windows 블로그](https://aka.ms/wip14328)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1523">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="5e6fb-1524">새로운 기능</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1524">New Features</span></span>
* <span data-ttu-id="5e6fb-1525">이제 Linux 사용자를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1525">Now support Linux users.</span></span>  <span data-ttu-id="5e6fb-1526">Windows 기반의 Ubuntu에 Bash를 설치하면 Linux 사용자를 만들라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1526">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="5e6fb-1527">자세한 내용은 https://aka.ms/wslusers 에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1527">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="5e6fb-1528">이제 호스트 이름이 Windows 컴퓨터 이름으로 설정됩니다. 더 이상 @localhost는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1528">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="5e6fb-1529">빌드 14328에 대한 자세한 내용은 https://aka.ms/wip14328 에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1529">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="5e6fb-1530">고정</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1530">Fixed</span></span>
* <span data-ttu-id="5e6fb-1531">비 /mnt/<drive> 파일에 대한 Symlink가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1531">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="5e6fb-1532">이제 npm 설치가 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1532">npm install now works</span></span>
    * <span data-ttu-id="5e6fb-1533">이제 [여기](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)에 제공된 지침에 따라 jdk/jre를 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1533">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="5e6fb-1534">알려진 이슈: symlink가 Windows 탑재에 대해 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1534">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="5e6fb-1535">이 기능은 이후 빌드에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1535">Functionality will be available in a later build</span></span>
* <span data-ttu-id="5e6fb-1536">이제 top 및 htop이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1536">top and htop now display</span></span>
* <span data-ttu-id="5e6fb-1537">일부 설치 오류에 대한 오류 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1537">Additional error messages for some install failures</span></span>
* <span data-ttu-id="5e6fb-1538">Syscall 및 버그 픽스가 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1538">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="5e6fb-1539">아래 syscall 목록이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1539">Supported syscall list below.</span></span>
* <span data-ttu-id="5e6fb-1540">버그 및 기능이 추가로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1540">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="5e6fb-1541">Syscall 지원</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1541">Syscall Support</span></span>
<span data-ttu-id="5e6fb-1542">아래는 WSL에서 일부가 구현된 syscall 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1542">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="5e6fb-1543">이 목록의 syscall은 하나 이상의 시나리오에서 지원되지만, 현재 지원되는 매개 변수 중 일부가 없을 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6fb-1543">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
