---
title: Linux 배포 관리
description: Linux용 Windows 하위 시스템에서 실행되는 여러 Linux 배포를 나열하고 구성하는 방법에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 51099f21fe44fd8c7e8682332c939fbe6d5e5827
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269873"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="b51c6-104">Linux용 Windows 하위 시스템 관리 및 구성</span><span class="sxs-lookup"><span data-stu-id="b51c6-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="b51c6-105">Windows 10 Fall Creators Update 이상에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="b51c6-106">업데이트된 [설치 가이드](./install_guide.md)를 참조하여 새 관리 기능을 사용해 보고 Microsoft Store에서 여러 Linux 배포의 실행을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="b51c6-107">WSL 실행 방법</span><span class="sxs-lookup"><span data-stu-id="b51c6-107">Ways to run WSL</span></span>

<span data-ttu-id="b51c6-108">Linux용 Windows 하위 시스템을 사용하여 Linux를 실행하는 여러 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="b51c6-109">`[distro]`(예: `ubuntu`)</span><span class="sxs-lookup"><span data-stu-id="b51c6-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="b51c6-110">`wsl.exe` 또는 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="b51c6-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="b51c6-111">`wsl [command]` 또는 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="b51c6-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="b51c6-112">사용해야 하는 방법은 수행하는 작업에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="b51c6-113">배포별 WSL 시작</span><span class="sxs-lookup"><span data-stu-id="b51c6-113">Launch WSL by distribution</span></span>

<span data-ttu-id="b51c6-114">배포판 특정 애플리케이션을 사용하여 배포를 실행하면 자체 콘솔 창에서 해당 배포가 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![시작 메뉴에서 WSL 시작](media/start-launch.png)

<span data-ttu-id="b51c6-116">Microsoft Store에서 "시작"을 클릭하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Microsoft Store에서 WSL 시작](media/store-launch.png)

<span data-ttu-id="b51c6-118">`[distribution].exe`를 실행하여 명령줄에서 배포를 실행할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="b51c6-119">명령줄에서 이 방식으로 배포를 실행하는 경우 작업 디렉터리가 현재 디렉터리에서 배포의 홈 디렉터리로 자동으로 변경된다는 단점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="b51c6-120">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b51c6-120">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="b51c6-121">wsl 및 wsl [명령]</span><span class="sxs-lookup"><span data-stu-id="b51c6-121">wsl and wsl [command]</span></span>

<span data-ttu-id="b51c6-122">명령줄에서 WSL을 실행하는 가장 좋은 방법은 `wsl.exe`를 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="b51c6-123">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b51c6-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="b51c6-124">`wsl`은 현재 작업 디렉터리를 그대로 유지할 뿐만 아니라 Windows 명령과 함께 단일 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="b51c6-125">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b51c6-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="b51c6-126">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b51c6-126">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="b51c6-127">여러 Linux 배포 관리</span><span class="sxs-lookup"><span data-stu-id="b51c6-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="b51c6-128">Windows 10 버전 1903 이상</span><span class="sxs-lookup"><span data-stu-id="b51c6-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="b51c6-129">배포는 WSL(Linux용 Windows 하위 시스템)에서 `wsl.exe`를 사용하여 관리할 수 있습니다. 여기에는 사용 가능한 배포 나열, 기본 배포 설정 및 배포 제거가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="b51c6-130">각 Linux 배포는 자체 구성을 독립적으로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="b51c6-131">배포 관련 명령을 보려면 `[distro.exe] /?`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="b51c6-132">예를 들어 `ubuntu /?`입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="b51c6-133">배포 나열</span><span class="sxs-lookup"><span data-stu-id="b51c6-133">List distributions</span></span>

<span data-ttu-id="b51c6-134">`wsl -l`, `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="b51c6-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="b51c6-135">WSL에 사용할 수 있는 Linux 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="b51c6-136">배포가 나열되면 해당 배포가 설치되어 사용할 준비가 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="b51c6-137">현재 사용할 수 없는 배포를 포함하여 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="b51c6-138">이러한 배포는 설치 중, 제거 중 또는 손상된 상태일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="b51c6-139">현재 실행되고 있는 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="b51c6-140">기본 배포 설정</span><span class="sxs-lookup"><span data-stu-id="b51c6-140">Set a default distribution</span></span>

<span data-ttu-id="b51c6-141">기본 WSL 배포는 명령줄에서 `wsl`을 실행할 때 실행되는 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="b51c6-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="b51c6-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="b51c6-143">기본 배포를 `<DistributionName>`으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="b51c6-144">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b51c6-144">**Example:**</span></span>  
<span data-ttu-id="b51c6-145">`wsl -s Ubuntu`는 기본 배포를 Ubuntu로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="b51c6-146">이제 `wsl npm init`를 실행하면 Ubuntu에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="b51c6-147">`wsl`을 실행하면 Ubuntu 세션이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="b51c6-148">배포 등록 취소 및 다시 설치</span><span class="sxs-lookup"><span data-stu-id="b51c6-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="b51c6-149">Linux 배포는 Microsoft Store를 통해 설치할 수 있지만 이를 통해 제거할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="b51c6-150">WSL Config를 사용하면 배포를 등록 취소/제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="b51c6-151">또한 등록을 취소하면 배포를 다시 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="b51c6-152">**주의:** 등록이 취소되면 해당 배포와 관련된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="b51c6-153">스토어에서 다시 설치하면 배포의 새 복사본이 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="b51c6-154">WSL에서 배포의 등록을 취소하여 해당 배포를 다시 설치하거나 정리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="b51c6-155">예를 들어 `wsl --unregister Ubuntu`는 WSL에서 사용할 수 있는 배포에서 Ubuntu를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="b51c6-156">`wsl --list`를 실행하면 나열되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="b51c6-157">다시 설치하려면 Microsoft Store에서 해당 배포를 찾아서 "시작"을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="b51c6-158">특정 사용자로 실행</span><span class="sxs-lookup"><span data-stu-id="b51c6-158">Run as a specific user</span></span>

<span data-ttu-id="b51c6-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="b51c6-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="b51c6-160">WSL을 지정된 사용자로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-160">Run WSL as the specified user.</span></span> <span data-ttu-id="b51c6-161">사용자는 WSL 배포 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="b51c6-162">특정 배포 실행</span><span class="sxs-lookup"><span data-stu-id="b51c6-162">Run a specific distribution</span></span>

<span data-ttu-id="b51c6-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="b51c6-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="b51c6-164">WSL의 지정된 배포를 실행합니다. 기본값을 변경하지 않고도 명령을 특정 배포로 보내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="b51c6-165">Windows 10 버전 1903의 이전 버전</span><span class="sxs-lookup"><span data-stu-id="b51c6-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="b51c6-166">WSL Config(`wslconfig.exe`)는 WSL(Linux용 Windows 하위 시스템)에서 실행되는 Linux 배포를 관리하기 위한 명령줄 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="b51c6-167">사용 가능한 배포를 나열하고, 기본 배포를 설정하고, 배포를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="b51c6-168">WSL Config는 배포를 확장하거나 조정하는 설정에 유용하지만, 각 Linux 배포는 자체 구성을 독립적으로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="b51c6-169">배포 관련 명령을 보려면 `[distro.exe] /?`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="b51c6-170">예를 들어 `ubuntu /?`입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="b51c6-171">wslconfig에 사용할 수 있는 모든 옵션을 보려면 `wslconfig /?`를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="b51c6-172">배포 나열</span><span class="sxs-lookup"><span data-stu-id="b51c6-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="b51c6-173">WSL에 사용할 수 있는 Linux 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="b51c6-174">배포가 나열되면 해당 배포가 설치되어 사용할 준비가 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="b51c6-175">현재 사용할 수 없는 배포를 포함하여 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="b51c6-176">이러한 배포는 설치 중, 제거 중 또는 손상된 상태일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="b51c6-177">기본 배포 설정</span><span class="sxs-lookup"><span data-stu-id="b51c6-177">Set a default distribution</span></span>

<span data-ttu-id="b51c6-178">기본 WSL 배포는 명령줄에서 `wsl`을 실행할 때 실행되는 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="b51c6-179">기본 배포를 `<DistributionName>`으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="b51c6-180">**예제:**</span><span class="sxs-lookup"><span data-stu-id="b51c6-180">**Example:**</span></span>  
<span data-ttu-id="b51c6-181">`wslconfig /setdefault Ubuntu`는 기본 배포를 Ubuntu로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="b51c6-182">이제 `wsl npm init`를 실행하면 Ubuntu에서 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="b51c6-183">`wsl`을 실행하면 Ubuntu 세션이 열립니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="b51c6-184">배포 등록 취소 및 다시 설치</span><span class="sxs-lookup"><span data-stu-id="b51c6-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="b51c6-185">Linux 배포는 Microsoft Store를 통해 설치할 수 있지만 이를 통해 제거할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="b51c6-186">WSL Config를 사용하면 배포를 등록 취소/제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="b51c6-187">또한 등록을 취소하면 배포를 다시 설치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="b51c6-188">**주의:** 등록이 취소되면 해당 배포와 관련된 모든 데이터, 설정 및 소프트웨어가 영구적으로 손실됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="b51c6-189">스토어에서 다시 설치하면 배포의 새 복사본이 설치됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="b51c6-190">WSL에서 배포의 등록을 취소하여 해당 배포를 다시 설치하거나 정리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="b51c6-191">예를 들어 `wslconfig /unregister Ubuntu`는 WSL에서 사용할 수 있는 배포에서 Ubuntu를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="b51c6-192">`wslconfig /list`를 실행하면 나열되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="b51c6-193">다시 설치하려면 Microsoft Store에서 해당 배포를 찾아서 "시작"을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="b51c6-194">WSL 시작 설정 지정</span><span class="sxs-lookup"><span data-stu-id="b51c6-194">Set WSL launch settings</span></span>

> <span data-ttu-id="b51c6-195">**Windows 참가자 빌드 17093 이상에서 사용할 수 있음**</span><span class="sxs-lookup"><span data-stu-id="b51c6-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="b51c6-196">`wsl.conf`를 사용하여 하위 시스템을 시작할 때마다 적용되는 WSL의 특정 기능을 자동으로 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="b51c6-197">현재 여기에는 자동 탑재 옵션 및 네트워크 구성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="b51c6-198">`wsl.conf`는 `/etc/wsl.conf`의 각 Linux 배포에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="b51c6-199">여기에 파일이 없으면 해당 파일을 직접 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="b51c6-200">WSL은 파일의 존재 여부를 검색하고 해당 내용을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="b51c6-201">파일이 없거나 형식이 잘못된(즉, 잘못된 태그 형식 지정) 경우에도 WSL은 정상적으로 계속 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="b51c6-202">다음은 배포판에 추가할 수 있는 `wsl.conf` 파일 샘플입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="b51c6-203">구성 옵션</span><span class="sxs-lookup"><span data-stu-id="b51c6-203">Configuration Options</span></span>

<span data-ttu-id="b51c6-204">.ini 규칙에 따라 키는 섹션 아래에 선언됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="b51c6-205">WSL은 `automount` 및 `network`의 두 가지 섹션을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="b51c6-206">automount</span><span class="sxs-lookup"><span data-stu-id="b51c6-206">automount</span></span>

<span data-ttu-id="b51c6-207">섹션: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="b51c6-207">Section: `[automount]`</span></span>


| <span data-ttu-id="b51c6-208">키</span><span class="sxs-lookup"><span data-stu-id="b51c6-208">key</span></span>        | <span data-ttu-id="b51c6-209">value</span><span class="sxs-lookup"><span data-stu-id="b51c6-209">value</span></span>                          | <span data-ttu-id="b51c6-210">기본값</span><span class="sxs-lookup"><span data-stu-id="b51c6-210">default</span></span>      | <span data-ttu-id="b51c6-211">참고</span><span class="sxs-lookup"><span data-stu-id="b51c6-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b51c6-212">enabled</span><span class="sxs-lookup"><span data-stu-id="b51c6-212">enabled</span></span>    | <span data-ttu-id="b51c6-213">boolean</span><span class="sxs-lookup"><span data-stu-id="b51c6-213">boolean</span></span>                        | <span data-ttu-id="b51c6-214">true</span><span class="sxs-lookup"><span data-stu-id="b51c6-214">true</span></span>         | <span data-ttu-id="b51c6-215">`true`를 사용하면 고정 드라이브(즉,</span><span class="sxs-lookup"><span data-stu-id="b51c6-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="b51c6-216">`C:/` 또는 `D:/`)가 `/mnt` 아래의 DrvFs에 자동으로 탑재됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="b51c6-217">`false`는 드라이브가 자동으로 탑재되지 않음을 의미하지만, 수동으로 또는 `fstab`를 통해 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="b51c6-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="b51c6-218">mountFsTab</span></span> | <span data-ttu-id="b51c6-219">boolean</span><span class="sxs-lookup"><span data-stu-id="b51c6-219">boolean</span></span>                        | <span data-ttu-id="b51c6-220">true</span><span class="sxs-lookup"><span data-stu-id="b51c6-220">true</span></span>         | <span data-ttu-id="b51c6-221">`true`는 WSL 시작 시 `/etc/fstab`가 처리되도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="b51c6-222">/etc/fstab는 SMB 공유와 같은 다른 파일 시스템을 선언할 수 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="b51c6-223">따라서 시작 시 이러한 파일 시스템을 WSL에 자동으로 탑재할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="b51c6-224">root</span><span class="sxs-lookup"><span data-stu-id="b51c6-224">root</span></span>       | <span data-ttu-id="b51c6-225">문자열</span><span class="sxs-lookup"><span data-stu-id="b51c6-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="b51c6-226">고정 드라이브가 자동으로 탑재될 디렉터리를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="b51c6-227">예를 들어 WSL의 `/windir/`에 디렉터리가 있고 이 디렉터리를 루트로 지정하면 고정 드라이브가 `/windir/c`에 탑재됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="b51c6-228">옵션</span><span class="sxs-lookup"><span data-stu-id="b51c6-228">options</span></span>    | <span data-ttu-id="b51c6-229">쉼표로 구분된 값 목록</span><span class="sxs-lookup"><span data-stu-id="b51c6-229">comma-separated list of values</span></span> | <span data-ttu-id="b51c6-230">빈 문자열</span><span class="sxs-lookup"><span data-stu-id="b51c6-230">empty string</span></span> | <span data-ttu-id="b51c6-231">이 값은 기본 DrvFs 탑재 옵션 문자열에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="b51c6-232">**DrvFs별 옵션만 지정할 수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="b51c6-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="b51c6-233">탑재 이진 파일이 일반적으로 플래그로 구문 분석되는 옵션은 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="b51c6-234">이러한 옵션을 명시적으로 지정하려면 원하는 모든 드라이브를 /etc/fstab에 포함시켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="b51c6-235">기본적으로 WSL은 uid와 gid를 기본 사용자의 값으로 설정합니다(Ubuntu 배포판에서 기본 사용자는 uid=1000, gid=1000으로 만들어짐).</span><span class="sxs-lookup"><span data-stu-id="b51c6-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="b51c6-236">사용자가 이 키를 통해 gid 또는 uid 옵션을 명시적으로 지정하면 연결된 값이 덮어쓰입니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="b51c6-237">그렇지 않으면 항상 기본값이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="b51c6-238">**참고:** 이러한 옵션은 자동으로 탑재된 모든 드라이브에 대한 탑재 옵션으로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="b51c6-239">특정 드라이브에 대한 옵션만 변경하려면 /etc/fstab를 대신 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="b51c6-240">네트워크</span><span class="sxs-lookup"><span data-stu-id="b51c6-240">network</span></span>

<span data-ttu-id="b51c6-241">섹션 레이블: `[network]`</span><span class="sxs-lookup"><span data-stu-id="b51c6-241">Section label: `[network]`</span></span>

| <span data-ttu-id="b51c6-242">키</span><span class="sxs-lookup"><span data-stu-id="b51c6-242">key</span></span> | <span data-ttu-id="b51c6-243">value</span><span class="sxs-lookup"><span data-stu-id="b51c6-243">value</span></span> | <span data-ttu-id="b51c6-244">기본값</span><span class="sxs-lookup"><span data-stu-id="b51c6-244">default</span></span> | <span data-ttu-id="b51c6-245">참고</span><span class="sxs-lookup"><span data-stu-id="b51c6-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="b51c6-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="b51c6-246">generateHosts</span></span> | <span data-ttu-id="b51c6-247">boolean</span><span class="sxs-lookup"><span data-stu-id="b51c6-247">boolean</span></span> | `true` | <span data-ttu-id="b51c6-248">`true`는 WSL에서 `/etc/hosts`를 생성하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="b51c6-249">`hosts` 파일에는 IP 주소에 해당하는 호스트 이름의 정적 맵이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="b51c6-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="b51c6-250">generateResolvConf</span></span> | <span data-ttu-id="b51c6-251">boolean</span><span class="sxs-lookup"><span data-stu-id="b51c6-251">boolean</span></span> | `true` | <span data-ttu-id="b51c6-252">`true`는 WSL에서 `/etc/resolv.conf`를 생성하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="b51c6-253">`resolv.conf`에는 지정된 호스트 이름을 해당 IP 주소로 확인할 수 있는 DNS 목록이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="b51c6-254">interop</span><span class="sxs-lookup"><span data-stu-id="b51c6-254">interop</span></span>

<span data-ttu-id="b51c6-255">섹션 레이블: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="b51c6-255">Section label: `[interop]`</span></span>

<span data-ttu-id="b51c6-256">다음 옵션은 참가자 빌드 17713 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="b51c6-257">키</span><span class="sxs-lookup"><span data-stu-id="b51c6-257">key</span></span> | <span data-ttu-id="b51c6-258">value</span><span class="sxs-lookup"><span data-stu-id="b51c6-258">value</span></span> | <span data-ttu-id="b51c6-259">기본값</span><span class="sxs-lookup"><span data-stu-id="b51c6-259">default</span></span> | <span data-ttu-id="b51c6-260">참고</span><span class="sxs-lookup"><span data-stu-id="b51c6-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="b51c6-261">enabled</span><span class="sxs-lookup"><span data-stu-id="b51c6-261">enabled</span></span> | <span data-ttu-id="b51c6-262">boolean</span><span class="sxs-lookup"><span data-stu-id="b51c6-262">boolean</span></span> | `true` | <span data-ttu-id="b51c6-263">이 키를 설정하면 WSL에서 Windows 프로세스 시작을 지원하는지 여부가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="b51c6-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="b51c6-264">appendWindowsPath</span></span> | <span data-ttu-id="b51c6-265">boolean</span><span class="sxs-lookup"><span data-stu-id="b51c6-265">boolean</span></span> | `true` | <span data-ttu-id="b51c6-266">이 키를 설정하면 WSL에서 Windows 경로 요소를 $PATH 환경 변수에 추가할지 여부가 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b51c6-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
