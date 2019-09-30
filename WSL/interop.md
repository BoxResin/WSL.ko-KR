---
title: Linux와 Windows의 상호 운용성
description: Linux용 Windows 하위 시스템에서 실행되는 Linux 배포와의 Windows 상호 운용성에 대해 설명합니다.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122729"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="f2bc6-103">Windows와 Linux용 Windows 하위 시스템의 상호 운용성</span><span class="sxs-lookup"><span data-stu-id="f2bc6-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="f2bc6-104">**Fall Creators Update로 업데이트되었습니다.**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="f2bc6-105">크리에이터스 업데이트 또는 1주년 업데이트를 실행하는 경우 [크리에이터스/1주년 업데이트 섹션](interop.md#creators-update-and-anniversary-update)으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="f2bc6-106">WSL(Linux용 Windows 하위 시스템)은 Windows와 Linux 간의 통합을 지속적으로 향상시키고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="f2bc6-107">다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-107">You can:</span></span>

1. <span data-ttu-id="f2bc6-108">Linux 콘솔에서 Windows 이진 파일을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="f2bc6-109">Windows 콘솔에서 Linux 이진 파일을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="f2bc6-110">**Windows 참가자 빌드 17063 이상** Linux와 Windows 간에 환경 변수를 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="f2bc6-111">이렇게 하면 Windows와 WSL 간에 원활한 환경이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="f2bc6-112">기술 세부 정보는 [WSL 블로그](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="f2bc6-113">Windows 명령줄에서 Linux 도구 실행</span><span class="sxs-lookup"><span data-stu-id="f2bc6-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="f2bc6-114">`wsl.exe <command>`를 사용하여 Windows 명령 프롬프트(CMD 또는 PowerShell)에서 Linux 이진 파일을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="f2bc6-115">이진 파일은 다음과 같은 방식으로 호출됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="f2bc6-116">현재 CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="f2bc6-117">WSL 기본 사용자로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="f2bc6-118">호출 프로세스 및 터미널과 동일한 Windows 관리 권한을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="f2bc6-119">예를 들어 다음과 같은 가치를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="f2bc6-120">`wsl.exe` 뒤에 나오는 Linux 명령은 WSL에서 실행되는 명령처럼 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="f2bc6-121">sudo, 파이핑, 파일 리디렉션과 같은 작업이 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="f2bc6-122">sudo를 사용하는 예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="f2bc6-123">WSL 및 Windows 명령을 혼합한 예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="f2bc6-124">`wsl.exe`에 전달된 명령은 수정되지 않고 WSL 프로세스에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="f2bc6-125">파일 경로는 WSL 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="f2bc6-126">경로가 포함된 예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="f2bc6-127">WSL에서 Windows 도구 실행</span><span class="sxs-lookup"><span data-stu-id="f2bc6-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="f2bc6-128">WSL은 `[binary name].exe`를 사용하여 WSL 명령줄에서 Windows 이진 파일을 직접 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="f2bc6-129">예를 들면 `notepad.exe`입니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="f2bc6-130">Windows 실행 파일을 더 쉽게 실행하기 위해 Windows 경로가 Fall Creators Update의 Linux `$PATH`에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="f2bc6-131">이 방식으로 실행되는 애플리케이션에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="f2bc6-132">작업 디렉터리를 WSL 명령 프롬프트로 유지합니다(대부분의 경우에 해당, 예외는 아래에 설명되어 있음).</span><span class="sxs-lookup"><span data-stu-id="f2bc6-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="f2bc6-133">WSL 프로세스와 동일한 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="f2bc6-134">활성 Windows 사용자로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="f2bc6-135">CMD 프롬프트에서 직접 실행한 것처럼 Windows 작업 관리자에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="f2bc6-136">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="f2bc6-137">WSL에서 실행되는 Windows 실행 파일은 네이티브 Linux 실행 파일과 비슷하게 처리됩니다(파이핑, 리디렉션 및 백그라운드 작업이 예상대로 작동).</span><span class="sxs-lookup"><span data-stu-id="f2bc6-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="f2bc6-138">파이프를 사용하는 예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="f2bc6-139">혼합된 Windows와 WSL 명령을 사용하는 예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="f2bc6-140">Windows 이진 파일은 파일 확장명을 포함하고, 파일 대/소문자와 일치하며, 실행 파일이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="f2bc6-141">일괄 처리 스크립트가 포함된 비실행 파일이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="f2bc6-142">`dir`과 같은 CMD 기본 명령은 `cmd.exe /C` 명령을 사용하여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="f2bc6-143">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="f2bc6-144">매개 변수는 수정되지 않은 Windows 이진 파일에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="f2bc6-145">예를 들어 다음 명령은 `notepad.exe`에서 `C:\temp\foo.txt`를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="f2bc6-146">VolFs에 있는 파일(`/mnt/<x>` 아래에 없는 파일)은 WSL에서 Windows 애플리케이션을 사용하여 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="f2bc6-147">기본적으로 WSL은 Windows 이진 파일의 작업 디렉터리를 현재 WSL 디렉터리로 유지하려고 하지만, 작업 디렉터리가 VolFs에 있는 경우 인스턴스 만들기 디렉터리로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="f2bc6-148">예를 들어 `wsl.exe`가 처음에는 `C:\temp`에서 시작되고, 현재 WSL 디렉터리가 사용자의 홈으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="f2bc6-149">사용자의 홈 디렉터리에서 `notepad.exe`를 호출하면 WSL이 자동으로 notepad.exe의 작업 디렉터리인 `C:\temp`로 되돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="f2bc6-150">Windows와 WSL 간의 환경 변수 공유</span><span class="sxs-lookup"><span data-stu-id="f2bc6-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="f2bc6-151">Windows 참가자 빌드 17063 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="f2bc6-152">17063 이전에서는 `PATH`만 WSL에서 액세스할 수 있는 Windows 환경 변수였습니다(이를 통해 WSL 아래에서 Win32 실행 파일을 시작할 수 있었음).</span><span class="sxs-lookup"><span data-stu-id="f2bc6-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="f2bc6-153">17063부터 WSL 및 Windows는 WSL에서 실행되는 Windows 및 Linux 배포판을 연결하기 위해 만든 특수 환경 변수인 `WSLENV`를 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="f2bc6-154">`WSLENV`의 속성:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="f2bc6-155">공유되며, Windows 및 WSL 환경 모두에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="f2bc6-156">Windows와 WSL 간에 공유할 환경 변수의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="f2bc6-157">Windows 및 WSL에서 제대로 작동하도록 환경 변수의 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="f2bc6-158">`WSLENV`에는 해당 환경 변수가 변환되는 방법에 영향을 주는 4개의 플래그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="f2bc6-159">`WSLENV` 플래그:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="f2bc6-160">`/p` - WSL/Linux 스타일 경로 및 Win32 경로 간의 경로를 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="f2bc6-161">`/l` - 환경 변수가 경로 목록임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="f2bc6-162">`/u` - Win32에서 WSL을 실행하는 경우에만 이 환경 변수가 포함되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="f2bc6-163">`/w` - WSL에서 Win32를 실행할 때만 경우에만 이 환경 변수가 포함되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="f2bc6-164">플래그는 필요에 따라 결합할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="f2bc6-165">Interop 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f2bc6-165">Disable Interop</span></span>

<span data-ttu-id="f2bc6-166">사용자는 다음 명령을 루트로 실행하여 단일 WSL 세션에서 Windows 이진 파일을 실행하는 기능을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="f2bc6-167">Windows 이진 파일을 다시 사용하도록 설정하려면 모든 WSL 세션을 종료하고 bash.exe를 다시 실행하거나 다음 명령을 루트로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="f2bc6-168">interop를 사용하지 않도록 설정하는 것은 WSL 세션 간에 유지되지 않습니다. 새 세션이 시작되면 interop가 사용하도록 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="f2bc6-169">크리에이터스 업데이트 및 1주년 업데이트</span><span class="sxs-lookup"><span data-stu-id="f2bc6-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="f2bc6-170">Fall Creators Update 이전의 interop 환경은 최신 interop 환경과 비슷하지만 몇 가지 주요 차이점이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="f2bc6-171">요약하면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-171">To summarize:</span></span>

* <span data-ttu-id="f2bc6-172">`bash.exe`가 더 이상 사용되지 않으며 `wsl.exe`로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="f2bc6-173">`wsl.exe`에는 단일 명령을 실행하기 위한 `-c` 옵션이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="f2bc6-174">Windows 경로가 WSL `$PATH`에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="f2bc6-175">interop를 사용하지 않도록 설정하는 프로세스는 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="f2bc6-176">Windows 명령줄에서 WSL 호출</span><span class="sxs-lookup"><span data-stu-id="f2bc6-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="f2bc6-177">Linux 이진 파일은 Windows 명령 프롬프트 또는 PowerShell에서 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="f2bc6-178">이 방식으로 호출되는 이진 파일에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="f2bc6-179">CMD 또는 PowerShell 프롬프트와 동일한 작업 디렉터리를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="f2bc6-180">WSL 기본 사용자로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="f2bc6-181">호출 프로세스 및 터미널과 동일한 Windows 관리 권한을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="f2bc6-182">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="f2bc6-183">이 방식으로 호출되는 Linux 명령은 다른 Windows 애플리케이션처럼 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="f2bc6-184">입력, 파이핑, 파일 리디렉션과 같은 작업이 예상대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="f2bc6-185">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-185">Examples:</span></span>

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

<span data-ttu-id="f2bc6-186">`bash -c`에 전달된 WSL 명령은 수정되지 않고 WSL 프로세스에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="f2bc6-187">파일 경로는 WSL 형식으로 지정해야 하며, 관련 문자를 이스케이프 방식으로 처리해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="f2bc6-188">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="f2bc6-189">WSL에서 Windows 이진 파일 호출</span><span class="sxs-lookup"><span data-stu-id="f2bc6-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="f2bc6-190">Linux용 Windows 하위 시스템은 WSL 명령줄에서 Windows 이진 파일을 직접 호출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="f2bc6-191">이 방식으로 실행되는 애플리케이션에는 다음과 같은 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="f2bc6-192">아래에 설명된 시나리오를 제외하고는 작업 디렉터리를 WSL 명령 프롬프트로 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="f2bc6-193">`bash.exe` 프로세스와 동일한 권한을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="f2bc6-194">활성 Windows 사용자로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="f2bc6-195">CMD 프롬프트에서 직접 실행한 것처럼 Windows 작업 관리자에 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="f2bc6-196">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="f2bc6-197">WSL에서는 이러한 실행 파일이 네이티브 Linux 실행 파일과 비슷한 방식으로 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="f2bc6-198">즉, 디렉터리를 Linux 경로에 추가하고 명령 간의 파이프가 예상대로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="f2bc6-199">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="f2bc6-200">Windows 이진 파일은 파일 확장명을 포함하고, 파일 대/소문자와 일치하며, 실행 파일이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="f2bc6-201">일괄 처리 스크립트 및 `dir`과 같은 명령이 포함된 비실행 파일은 `/mnt/c/Windows/System32/cmd.exe /C` 명령을 사용하여 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="f2bc6-202">예제:</span><span class="sxs-lookup"><span data-stu-id="f2bc6-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="f2bc6-203">매개 변수는 수정되지 않은 Windows 이진 파일에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="f2bc6-204">예를 들어 다음 명령은 `notepad.exe`에서 `C:\temp\foo.txt`를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="f2bc6-205">VolFs에 있는 파일(`/mnt/<x>` 아래에 없는 파일)은 Windows 애플리케이션을 사용하여 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="f2bc6-206">기본적으로 WSL은 Windows 이진 파일의 작업 디렉터리를 현재 WSL 디렉터리로 유지하려고 하지만, 작업 디렉터리가 VolFs에 있는 경우 인스턴스 만들기 디렉터리로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="f2bc6-207">예를 들어 `bash.exe`가 처음에는 `C:\temp`에서 시작되고, 현재 WSL 디렉터리가 사용자의 홈으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="f2bc6-208">사용자의 홈 디렉터리에서 `notepad.exe`를 호출하면 WSL이 자동으로 notepad.exe의 작업 디렉터리인 `C:\temp`로 되돌아갑니다.</span><span class="sxs-lookup"><span data-stu-id="f2bc6-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
