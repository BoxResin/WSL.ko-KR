---
title: Linux용 Windows 하위 시스템 문제 해결
description: Linux용 Windows 하위 시스템에서 Linux를 실행하는 동안 사용자에게 발생할 수 있는 일반적인 오류 및 문제에 대한 자세한 정보를 제공합니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, Ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: b66392f6ad37af9d61e8b4fb6bb477d0d774ccb6
ms.sourcegitcommit: f1e471bca7a65073135365e49c0d4e59227bdf25
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/25/2020
ms.locfileid: "77575283"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="1933d-104">Linux용 Windows 하위 시스템 문제 해결</span><span class="sxs-lookup"><span data-stu-id="1933d-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="1933d-105">WSL 관련 문제에 대한 지원은 GitHub 리포지토리를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="1933d-106">문제와 관련된 기존 문제 검색</span><span class="sxs-lookup"><span data-stu-id="1933d-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="1933d-107">기술 문제를 해결하려면 https://github.com/Microsoft/wsl/issues 제품 리포지토리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="1933d-108">이 설명서의 내용과 관련된 문제는 https://github.com/MicrosoftDocs/wsl/issues 문서 리포지토리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="1933d-109">버그 보고서 제출</span><span class="sxs-lookup"><span data-stu-id="1933d-109">Submit a bug report</span></span>

<span data-ttu-id="1933d-110">WSL 함수 또는 기능과 관련된 버그는 해당 문제를 https://github.com/Microsoft/wsl/issues 제품 리포지토리에 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="1933d-111">기능 요청 제출</span><span class="sxs-lookup"><span data-stu-id="1933d-111">Submit a feature request</span></span>

<span data-ttu-id="1933d-112">WSL 함수 또는 호환성과 관련된 새로운 기능을 요청하려면 해당 문제를 https://github.com/Microsoft/wsl/issues 제품 리포지토리에 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="1933d-113">문서 작성에 참여</span><span class="sxs-lookup"><span data-stu-id="1933d-113">Contribute to the docs</span></span>

<span data-ttu-id="1933d-114">WSL 설명서에 기여하려면 끌어오기 요청을 https://github.com/MicrosoftDocs/wsl/issues 문서 리포지토리에 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="1933d-115">터미널 또는 명령줄</span><span class="sxs-lookup"><span data-stu-id="1933d-115">Terminal or Command Line</span></span>

<span data-ttu-id="1933d-116">마지막으로, Windows 터미널, Windows 콘솔 또는 명령줄 UI와 관련된 문제가 있는 경우 https://github.com/microsoft/terminal Windows 터미널 리포지토리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="1933d-117">일반적인 문제</span><span class="sxs-lookup"><span data-stu-id="1933d-117">Common issues</span></span>

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="1933d-118">Bash가 VPN에 연결되면 네트워크 연결이 끊어짐</span><span class="sxs-lookup"><span data-stu-id="1933d-118">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="1933d-119">Windows에서 VPN에 연결한 후에 Bash에서 네트워크 연결이 끊어지면 Bash 내에서 다음 해결 방법을 시도해 보세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-119">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="1933d-120">이 해결 방법을 사용하면 `/etc/resolv.conf`를 통해 DNS 확인을 수동으로 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-120">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="1933d-121">`ipconfig.exe /all`을 수행하여 VPN의 DNS 서버를 적어 둡니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-121">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="1933d-122">`sudo cp /etc/resolv.conf /etc/resolv.conf.new`를 수행하여 기존 resolv.conf의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-122">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="1933d-123">`sudo unlink /etc/resolv.conf`를 수행하여 현재 resolv.conf의 연결을 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-123">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="1933d-124">`/etc/resolv.conf`를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-124">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="1933d-125">a.</span><span class="sxs-lookup"><span data-stu-id="1933d-125">a.</span></span> <span data-ttu-id="1933d-126">"\# 이 파일은 WSL에서 자동으로 생성했습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-126">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="1933d-127">이 파일의 자동 생성을 중지하려면 이 줄을 제거하세요."라는 파일의 첫 번째 줄을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-127">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="1933d-128">b.</span><span class="sxs-lookup"><span data-stu-id="1933d-128">b.</span></span> <span data-ttu-id="1933d-129">위 (1)의 DNS 항목을 DNS 서버 목록의 첫 번째 항목으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-129">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="1933d-130">c.</span><span class="sxs-lookup"><span data-stu-id="1933d-130">c.</span></span> <span data-ttu-id="1933d-131">파일을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-131">Close the file.</span></span> <br/>

<span data-ttu-id="1933d-132">VPN의 연결을 끊은 후에는 변경 내용을 `/etc/resolv.conf`로 되돌려야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-132">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="1933d-133">이렇게 하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-133">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="1933d-134">WSL을 시작하거나 배포를 설치하면 오류 코드가 반환됨</span><span class="sxs-lookup"><span data-stu-id="1933d-134">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="1933d-135">[이 지침](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)에 따라 자세한 로그를 수집하고 문제를 GitHub에 제출하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-135">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="1933d-136">Windows의 Ubuntu에 있는 Bash 업데이트</span><span class="sxs-lookup"><span data-stu-id="1933d-136">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="1933d-137">Windows의 Ubuntu에 있는 Bash에는 업데이트해야 할 수 있는 두 가지 구성 요소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-137">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="1933d-138">Linux용 Windows 하위 시스템</span><span class="sxs-lookup"><span data-stu-id="1933d-138">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="1933d-139">Windows의 Ubuntu에서 Bash의 이 부분을 업그레이드하면 [릴리스 정보](./release-notes.md)의 새로운 수정에 대한 개요가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-139">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="1933d-140">Windows 참가자 프로그램을 구독하고 빌드가 최신 상태인지 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-140">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="1933d-141">Ubuntu 인스턴스 재설정을 포함하여 매우 자세히 제어하려면 [명령 참조 페이지](./reference.md)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-141">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="1933d-142">Ubuntu 사용자 이진 파일</span><span class="sxs-lookup"><span data-stu-id="1933d-142">The Ubuntu user binaries</span></span>

   <span data-ttu-id="1933d-143">Windows의 Ubuntu에서 Bash의 이 부분을 업그레이드하면 apt-get을 통해 설치한 애플리케이션을 포함하여 Ubuntu 사용자 이진 파일에 대한 모든 업데이트가 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-143">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="1933d-144">업데이트하려면 Bash에서 다음 명령을 실행하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-144">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="1933d-145">apt-get upgrade 오류</span><span class="sxs-lookup"><span data-stu-id="1933d-145">Apt-get upgrade errors</span></span>

<span data-ttu-id="1933d-146">일부 패키지는 아직 구현하지 않은 기능을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-146">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="1933d-147">예를 들어 `udev`는 아직 지원되지 않으므로 여러 `apt-get upgrade` 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-147">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="1933d-148">`udev`와 관련된 문제를 해결하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-148">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="1933d-149">다음을 `/usr/sbin/policy-rc.d`에 작성하고 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-149">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="1933d-150">실행 권한을 `/usr/sbin/policy-rc.d`에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-150">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="1933d-151">다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-151">Run the following commands:</span></span>

   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="1933d-152">"Error: 0x80040306" - 설치 시</span><span class="sxs-lookup"><span data-stu-id="1933d-152">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="1933d-153">이 오류는 레거시 콘솔을 지원하지 않는다는 사실과 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-153">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="1933d-154">레거시 콘솔을 해제하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-154">To turn off legacy console:</span></span>

1. <span data-ttu-id="1933d-155">cmd.exe를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-155">Open cmd.exe</span></span>
1. <span data-ttu-id="1933d-156">마우스 오른쪽 단추로 제목 표시줄-> 속성을 차례로 클릭하고, [레거시 콘솔 사용]의 선택을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-156">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="1933d-157">확인을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-157">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="1933d-158">"Error: 0x80040154" - Windows 업데이트 후</span><span class="sxs-lookup"><span data-stu-id="1933d-158">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="1933d-159">Windows 업데이트 중에 Linux용 Windows 하위 시스템 기능이 사용하지 않도록 설정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-159">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="1933d-160">이 문제가 발생하면 Windows 기능을 다시 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-160">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="1933d-161">Linux용 Windows 하위 시스템을 사용하도록 설정하는 방법에 대한 지침은 [설치 가이드](./install-win10.md)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-161">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="1933d-162">표시 언어 변경</span><span class="sxs-lookup"><span data-stu-id="1933d-162">Changing the display language</span></span>

<span data-ttu-id="1933d-163">WSL 설치는 Windows 설치의 로캘과 일치하도록 Ubuntu 로캘을 자동으로 변경하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-163">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="1933d-164">이 동작을 원하지 않는 경우 설치가 완료된 후 다음 명령을 실행하여 Ubuntu 로캘을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-164">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="1933d-165">이 변경 내용이 적용되려면 bash.exe를 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-165">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="1933d-166">아래 예제에서는 로캘을 en-US로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-166">The below example changes to locale to en-US:</span></span>

``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="1933d-167">Windows 시스템 복원 후의 설치 문제</span><span class="sxs-lookup"><span data-stu-id="1933d-167">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="1933d-168">`%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` 폴더를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-168">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="1933d-169">**참고: 선택적 기능이 완전히 설치되어 작동하는 경우에는 이 작업을 수행하지 마세요.**</span><span class="sxs-lookup"><span data-stu-id="1933d-169">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="1933d-170">선택적 WSL 기능을 사용하도록 설정합니다(아직 사용하지 않는 경우).</span><span class="sxs-lookup"><span data-stu-id="1933d-170">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="1933d-171">다시 부팅</span><span class="sxs-lookup"><span data-stu-id="1933d-171">Reboot</span></span>
4. <span data-ttu-id="1933d-172">lxrun /uninstall /full을 실행합니다</span><span class="sxs-lookup"><span data-stu-id="1933d-172">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="1933d-173">Bash를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-173">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="1933d-174">WSL에서 인터넷에 액세스할 수 없음</span><span class="sxs-lookup"><span data-stu-id="1933d-174">No internet access in WSL</span></span>

<span data-ttu-id="1933d-175">일부 사용자가 WSL에서 인터넷 액세스를 차단하는 특정 방화벽 애플리케이션의 문제를 보고했습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-175">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="1933d-176">보고된 방화벽은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-176">The firewalls reported are:</span></span>

1. <span data-ttu-id="1933d-177">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="1933d-177">Kaspersky</span></span>
2. <span data-ttu-id="1933d-178">AVG</span><span class="sxs-lookup"><span data-stu-id="1933d-178">AVG</span></span>
3. <span data-ttu-id="1933d-179">Avast</span><span class="sxs-lookup"><span data-stu-id="1933d-179">Avast</span></span>

<span data-ttu-id="1933d-180">방화벽을 해제하면 액세스가 허용되는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-180">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="1933d-181">단순히 방화벽을 설치하면 경우에 따라 액세스가 차단되는 것처럼 보입니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-181">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="1933d-182">ping 사용 시의 권한 거부 오류</span><span class="sxs-lookup"><span data-stu-id="1933d-182">Permission Denied error when using ping</span></span>

<span data-ttu-id="1933d-183">[Windows 1주년 업데이트, 버전 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update)의 경우 WSL에서 ping을 실행하려면 Windows의 **관리자 권한**이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-183">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="1933d-184">ping을 실행하려면 Windows의 Ubuntu에서 관리자 권한으로 Bash를 실행하거나 CMD/PowerShell 프롬프트에서 관리자 권한으로 bash.exe를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-184">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="1933d-185">이후 버전의 Windows인 [빌드 14926 이상](./release-notes.md#build-14926)의 경우 관리자 권한이 더 이상 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-185">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="1933d-186">Bash가 중지됨</span><span class="sxs-lookup"><span data-stu-id="1933d-186">Bash is hung</span></span>

<span data-ttu-id="1933d-187">Bash로 작업하는 동안 Bash가 중지되거나 교착 상태가 되어 입력에 응답하지 않는 경우 메모리 덤프를 수집하고 보고하여 문제를 진단하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-187">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="1933d-188">다음 단계를 수행하면 시스템의 작동이 중단됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-188">Note that these steps will crash your system.</span></span> <span data-ttu-id="1933d-189">편안하지 않으면 이 작업을 수행하지 않거나 해당 작업을 저장한 후에 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-189">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="1933d-190">메모리 덤프를 수집하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-190">To collect a memory dump</span></span>

1. <span data-ttu-id="1933d-191">메모리 덤프 유형을 "전체 메모리 덤프"로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-191">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="1933d-192">덤프 유형을 변경하는 동안 현재 유형을 적어 둡니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-192">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="1933d-193">이 [단계](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809)를 사용하여 키보드 컨트롤을 사용하는 시스템 작동 중단을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-193">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="1933d-194">중지 또는 교착 상태를 재현합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-194">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="1933d-195">(2)의 키 시퀀스를 사용하여 시스템의 작동을 중단시킵니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-195">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="1933d-196">시스템의 작동이 중단되고 메모리 덤프가 수집됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-196">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="1933d-197">시스템이 다시 부팅되면 memory.dmp를 secure@microsoft.com에 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-197">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="1933d-198">덤프 파일의 기본 위치는 %SystemRoot%\memory.dmp 또는 C:\Windows\memory.dmp(C:가 시스템 드라이브인 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-198">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="1933d-199">이메일에서 덤프는 Windows 팀의 WSL 또는 Bash에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-199">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="1933d-200">메모리 덤프 유형을 원래 설정으로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-200">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="1933d-201">빌드 번호 확인</span><span class="sxs-lookup"><span data-stu-id="1933d-201">Check your build number</span></span>

<span data-ttu-id="1933d-202">PC의 아키텍처 및 Windows 빌드 번호를 확인하려면</span><span class="sxs-lookup"><span data-stu-id="1933d-202">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="1933d-203">**설정** > **시스템** > **정보**를 차례로 엽니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-203">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="1933d-204">**OS 빌드** 및 **시스템 종류** 필드를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-204">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="1933d-205">![빌드 및 시스템 종류 필드의 스크린샷](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="1933d-205">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="1933d-206">Windows Server 빌드 번호를 확인하려면 PowerShell에서 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-206">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="1933d-207">WSL이 사용하도록 설정되었는지 확인</span><span class="sxs-lookup"><span data-stu-id="1933d-207">Confirm WSL is enabled</span></span>

<span data-ttu-id="1933d-208">PowerShell에서 다음을 실행하여 Linux용 Windows 하위 시스템을 사용하도록 설정했는지 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-208">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="1933d-209">OpenSSH 서버 연결 문제</span><span class="sxs-lookup"><span data-stu-id="1933d-209">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="1933d-210">SSH 서버를 연결하려고 하면 "127.0.0.1 포트 22에 의해 연결이 닫혔습니다." 오류로 인해 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-210">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="1933d-211">OpenSSH 서버가 실행되고 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-211">Make sure your OpenSSH Server is running:</span></span>

   ``` BASH
   sudo service ssh status
   ```

   <span data-ttu-id="1933d-212">그리고 https://help.ubuntu.com/lts/serverguide/openssh-server.html.en 자습서를 수행했습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-212">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="1933d-213">sshd 서비스를 중지한 다음, 디버그 모드에서 sshd를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-213">Stop the sshd service and start sshd in debug mode:</span></span>

   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="1933d-214">시작 로그를 확인하고, HostKeys를 사용할 수 있고 다음과 같은 로그 메시지가 표시되지 않는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-214">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

<span data-ttu-id="1933d-215">이러한 메시지가 표시되고 키가 `/etc/ssh/` 아래에 없으면 해당 키를 다시 생성하거나 OpenSSH 서버를 제거 후 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-215">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="1933d-216">WSL 선택적 기능을 사용하도록 설정할 때 "참조된 어셈블리를 찾을 수 없습니다."</span><span class="sxs-lookup"><span data-stu-id="1933d-216">"The referenced assembly could not be found."</span></span> <span data-ttu-id="1933d-217">오류가 발생함</span><span class="sxs-lookup"><span data-stu-id="1933d-217">when enabling the WSL optional feature</span></span>

<span data-ttu-id="1933d-218">이 오류는 잘못된 설치 상태와 관련이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-218">This error is related to being in a bad install state.</span></span> <span data-ttu-id="1933d-219">이 문제를 시도해 보고 해결하려면 다음 단계를 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-219">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="1933d-220">PowerShell에서 WSL 기능 사용 명령을 실행하는 경우 [시작] 메뉴를 열고, 'Windows 기능 사용/사용 안 함'을 검색하여 GUI를 대신 사용해 본 다음, 목록에서 선택적 구성 요소를 설치할 'Linux용 Windows 하위 시스템'을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-220">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="1933d-221">[설정], [업데이트]로 차례로 이동하고, '업데이트 확인'을 클릭하여 Windows 버전을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-221">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="1933d-222">두 단계가 모두 실패하고 WSL에 액세스해야 하는 경우 설치 미디어를 사용하여 Windows 10을 다시 설치하고 '모두 유지'를 선택하여 앱과 파일이 유지되도록 하는 방식으로 업그레이드하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-222">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="1933d-223">이 작업을 수행하는 방법에 대한 지침은 [Windows 10 다시 설치](https://support.microsoft.com/help/4000735/windows-10-reinstall) 페이지에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-223">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="1933d-224">(SSH 관련) 권한 오류 해결</span><span class="sxs-lookup"><span data-stu-id="1933d-224">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="1933d-225">이 오류가 표시되는 경우:</span><span class="sxs-lookup"><span data-stu-id="1933d-225">If you're seeing this error:</span></span>

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="1933d-226">이 문제를 해결하려면 다음을 ```/etc/wsl.conf``` 파일에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-226">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="1933d-227">이 명령을 추가하면 메타데이터가 포함되고 WSL에서 보이는 Windows 파일에 대한 파일 권한이 수정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933d-227">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="1933d-228">자세한 내용은 [파일 시스템 권한](./file-permissions.md)에서 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="1933d-228">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>