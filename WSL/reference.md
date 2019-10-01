---
title: Linux용 Windows 하위 시스템에 대한 명령 참조
description: Linux용 Windows 하위 시스템을 관리하는 명령의 목록입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d74a6926fd797f2e1ede0fd5d8d080d0f1ce3f6b
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269839"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="8f65c-104">Linux용 Windows 하위 시스템에 대한 명령 참조</span><span class="sxs-lookup"><span data-stu-id="8f65c-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="8f65c-105">Linux용 Windows 하위 시스템과 상호 작용하는 가장 좋은 방법은 `wsl.exe` 명령을 사용하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="8f65c-106">Windows 버전 1903에서 `wsl.exe`를 사용하는 경우의 모든 옵션이 포함된 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="8f65c-107">사용: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="8f65c-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="8f65c-108">Linux 이진 파일을 실행하기 위한 인수</span><span class="sxs-lookup"><span data-stu-id="8f65c-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="8f65c-109">**인수 없음**</span><span class="sxs-lookup"><span data-stu-id="8f65c-109">**Without arguments**</span></span>

  <span data-ttu-id="8f65c-110">명령줄이 제공되지 않으면 wsl.exe에서 기본 셸을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="8f65c-111">**--exec, -e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="8f65c-112">기본 Linux 셸을 사용하지 않고 지정된 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="8f65c-113">나머지 명령줄을 있는 그대로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="8f65c-114">또한 위의 명령에는 다음 옵션도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="8f65c-115">**--distribution, -d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="8f65c-116">지정된 배포를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-116">Run the specified distribution.</span></span>

* <span data-ttu-id="8f65c-117">**--user, -u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="8f65c-118">지정된 사용자로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="8f65c-119">Linux용 Windows 하위 시스템을 관리하기 위한 인수</span><span class="sxs-lookup"><span data-stu-id="8f65c-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="8f65c-120">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="8f65c-121">배포를 tar 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="8f65c-122">파일 이름은 표준 출력을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="8f65c-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="8f65c-124">지정된 tar 파일을 새 배포로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="8f65c-125">파일 이름은 표준 입력을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="8f65c-126">**--list, -l [옵션]**</span><span class="sxs-lookup"><span data-stu-id="8f65c-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="8f65c-127">배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-127">Lists distributions.</span></span>

  <span data-ttu-id="8f65c-128">옵션:</span><span class="sxs-lookup"><span data-stu-id="8f65c-128">Options:</span></span>
  * <span data-ttu-id="8f65c-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="8f65c-129">**--all**</span></span>
      
    <span data-ttu-id="8f65c-130">현재 설치 또는 제거 중인 배포를 포함하여 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="8f65c-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="8f65c-131">**--running**</span></span>
      
    <span data-ttu-id="8f65c-132">현재 실행 중인 배포만 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="8f65c-133">**--set-default, -s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-134">배포를 기본값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="8f65c-135">**--terminate, -t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-136">지정된 배포를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="8f65c-137">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-138">배포의 등록을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="8f65c-139">**--help** 사용법 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="8f65c-140">추가 명령</span><span class="sxs-lookup"><span data-stu-id="8f65c-140">Additional Commands</span></span>

<span data-ttu-id="8f65c-141">Linux용 Windows 하위 시스템과 상호 작용하는 기록 명령도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="8f65c-142">이러한 기능은 `wsl.exe`에 포함되어 있지만 여전히 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="8f65c-143">다음 명령을 사용하여 WSL 배포를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="8f65c-144">해당 옵션의 목록은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-144">Below is a list of its options.</span></span>

<span data-ttu-id="8f65c-145">사용: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="8f65c-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="8f65c-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="8f65c-146">Arguments</span></span>
* <span data-ttu-id="8f65c-147">**/l, /list [옵션]**</span><span class="sxs-lookup"><span data-stu-id="8f65c-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="8f65c-148">등록된 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="8f65c-149">옵션:</span><span class="sxs-lookup"><span data-stu-id="8f65c-149">Options:</span></span>
    * <span data-ttu-id="8f65c-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="8f65c-150">**/all**</span></span>
    
      <span data-ttu-id="8f65c-151">필요에 따라 현재 설치 또는 제거 중인 배포를 포함하여 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="8f65c-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="8f65c-152">**/running**</span></span>
      
      <span data-ttu-id="8f65c-153">현재 실행 중인 배포만 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="8f65c-154">**/s, /setdefault \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-155">배포를 기본값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="8f65c-156">**/t, /terminate \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-157">배포를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-157">Terminates the distribution.</span></span>

* <span data-ttu-id="8f65c-158">**/u, /unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-159">배포의 등록을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="8f65c-160">**/upgrade \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8f65c-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="8f65c-161">배포를 WslFs 파일 시스템 형식으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="8f65c-162">이 명령은 Bash 셸을 시작하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="8f65c-163">이 명령에서 사용할 수 있는 옵션은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="8f65c-164">사용: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="8f65c-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="8f65c-165">**지정된 옵션 없음**</span><span class="sxs-lookup"><span data-stu-id="8f65c-165">**No Option given**</span></span>
  
  <span data-ttu-id="8f65c-166">현재 디렉터리에서 Bash 셸을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="8f65c-167">Bash 셸이 설치되어 있지 않으면 `lxrun /install`이 자동으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="8f65c-168">`bash ~`는 Bash 셸을 사용자의 홈 디렉터리에 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="8f65c-169">`cd ~`를 실행하는 것과 비슷합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="8f65c-170">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="8f65c-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="8f65c-171">명령을 실행하고, 출력한 다음, Windows 명령 프롬프트로 다시 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="8f65c-172">예제: `bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="8f65c-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="8f65c-173">사용되지 않는 명령</span><span class="sxs-lookup"><span data-stu-id="8f65c-173">Deprecated Commands</span></span>

<span data-ttu-id="8f65c-174">`lxrun.exe`는 Linux용 Windows 하위 시스템을 설치하고 관리하는 데 처음으로 사용된 명령이었습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="8f65c-175">Windows 10 1803 이상에서는 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="8f65c-176">`lxrun.exe` 명령은 [WSL(Linux용 Windows 하위 시스템)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)과 직접 상호 작용하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="8f65c-177">이러한 명령은 `\Windows\System32` 디렉터리에 설치되며 Windows 명령 프롬프트 내에서 또는 PowerShell에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="8f65c-178">명령</span><span class="sxs-lookup"><span data-stu-id="8f65c-178">Command</span></span>                     | <span data-ttu-id="8f65c-179">설명</span><span class="sxs-lookup"><span data-stu-id="8f65c-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="8f65c-180">lxrun 명령은 WSL 인스턴스를 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="8f65c-181">다운로드 및 설치 프로세스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="8f65c-182">모든 프롬프트를 무시하려면 **/y**를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="8f65c-183">확인 메시지가 자동으로 수락되고 기본 사용자가 루트로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="8f65c-184">Ubuntu 이미지를 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="8f65c-185">이 명령은 기본적으로 사용자의 Ubuntu 홈 디렉터리를 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="8f65c-186">확인 메시지가 자동으로 수락되도록 하려면 **/y**를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="8f65c-187">**/full**은 사용자의 Ubuntu 홈 디렉터리를 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="8f65c-188">Ubuntu 사용자에 대한 기본 Bash를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="8f65c-189">지정된 사용자가 없는 경우 암호를 입력하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="8f65c-190">자세한 내용은 https://aka.ms/wslusers 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8f65c-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="8f65c-191">**/y**는 암호를 입력하라는 메시지를 무시합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="8f65c-192">사용자가 암호 없이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="8f65c-193">하위 시스템의 패키지 인덱스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8f65c-193">Updates the subsystem's package index</span></span>          |
