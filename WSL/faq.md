---
title: FAQ(질문과 대답)
description: Linux용 Windows 하위 시스템에 대한 질문과 대답입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, FAQ
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: d5c4308c531e4df02acbfb17a76b3f83d912b512
ms.sourcegitcommit: 33290fd88a461a1a36d6106e737490bd57dc77bd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/14/2020
ms.locfileid: "75951249"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="e3fd2-104">Linux용 Windows 하위 시스템에 대한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="e3fd2-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="e3fd2-105">WSL(Linux용 Windows 하위 시스템)이란?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="e3fd2-106">WSL(Linux용 Windows 하위 시스템)은 기존 Windows 데스크톱 및 최신 스토어 앱과 함께 Windows에서 네이티브 Linux 명령줄 도구를 직접 실행할 수 있는 새로운 Windows 10 기능입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="e3fd2-107">자세한 내용은 [정보 페이지](./about.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="e3fd2-108">WSL은 누구를 위한 것인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-108">Who is WSL for?</span></span>
<span data-ttu-id="e3fd2-109">이는 주로 개발자, 특히 웹 개발자 및 오픈 소스 프로젝트에서 작업하는 사용자를 위한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="e3fd2-110">이 도구를 통해 Bash, 일반 Linux 도구(`sed`, `awk` 등) 및 많은 Linux 중심 도구(Ruby, Python 등)를 사용하려거나 사용해야 하는 사용자는 Windows에서 해당 도구 체인을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="e3fd2-111">WSL로 무엇을 할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-111">What can I do with WSL?</span></span>
<span data-ttu-id="e3fd2-112">WSL은 시작할 때 Bash 셸을 실행하는 Windows 콘솔을 여는 Bash.exe라는 애플리케이션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="e3fd2-113">Bash를 사용하면 Linux 명령줄 도구 및 앱을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="e3fd2-114">예를 들어 `lsb_release -a`를 입력하고 Enter 키를 누릅니다. 그러면 현재 실행되고 있는 Linux 배포판의 세부 정보가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![배포판 세부 정보의 스크린샷](media/distro.png)

<span data-ttu-id="e3fd2-116">또한 Linux Bash 셸 내에서 로컬 머신의 파일 시스템에 액세스할 수 있습니다. 이 경우 로컬 드라이브는 `/mnt` 폴더 아래에 탑재되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="e3fd2-117">예를 들어 `C:` 드라이브가 `/mnt/c` 아래에 탑재되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![탑재된 C 드라이브의 스크린샷](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="e3fd2-119">Bash란?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-119">What is Bash?</span></span>
<span data-ttu-id="e3fd2-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)는 널리 사용되는 텍스트 기반 셸 및 명령 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="e3fd2-121">이는 Ubuntu, 기타 Linux 배포판 및 macOS에 포함된 기본 셸입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="e3fd2-122">사용자가 명령을 셸에 입력하여 스크립트를 실행하거나 명령과 도구를 실행하여 많은 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="e3fd2-123">어떻게 작동하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-123">How does this work?</span></span>
<span data-ttu-id="e3fd2-124">기본 기술에 대해 자세히 알아보려면 이 [블로그](https://blogs.msdn.microsoft.com/wsl/)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="e3fd2-125">VM에서 Linux 대신 WSL을 사용하는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="e3fd2-126">WSL에는 전체 가상 머신보다 적은 리소스(CPU, 메모리 및 스토리지)가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="e3fd2-127">또한 WSL을 사용하면 Windows 명령줄, 데스크톱 및 스토어 앱과 함께 Linux 명령줄 도구 및 앱을 실행하고 Linux 내에서 Windows 파일에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="e3fd2-128">이렇게 하면 원하는 경우 동일한 파일 세트에서 Windows 앱 및 Linux 명령줄 도구를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="e3fd2-129">예를 들어 Windows 대신 Linux에서 Ruby를 사용하는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="e3fd2-130">일부 플랫폼 간 도구는 이러한 도구가 실행되는 환경이 Linux처럼 동작한다고 가정하여 구축되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="e3fd2-131">예를 들어 일부 도구에서는 매우 긴 파일 경로에 액세스할 수 있거나 특정 파일/폴더가 있다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="e3fd2-132">이로 인해 Windows에서 Linux와 다르게 동작하는 문제가 발생하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="e3fd2-133">Ruby 및 Node와 같은 많은 언어는 Windows에서 이식되고 매우 효율적으로 실행되는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="e3fd2-134">그러나 일부 Ruby Gem 또는 Node/NPM 라이브러리 소유자는 Windows를 지원하기 위해 라이브러리를 이식하지 않으며 많은 소유자가 Linux 관련 종속성을 사용하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="e3fd2-135">이로 인해 이러한 도구와 라이브러리를 사용하여 빌드된 시스템의 Windows에서 빌드 및 때로는 런타임 오류 또는 원치 않는 동작이 발생하는 경우가 많습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="e3fd2-136">이러한 문제 중 일부는 Windows의 명령줄 도구를 개선하도록 많은 사용자가 Microsoft에 요청하게 하였으며, Windows에서 네이티브 Bash 및 Linux 명령줄 도구를 실행할 수 있도록 하기 위해 Microsoft에서 Canonical과 파트너 관계를 맺게 하였습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="e3fd2-137">PowerShell에서 의미하는 것은 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="e3fd2-138">OSS 프로젝트에서 작업하는 동안 PowerShell 프롬프트에서 Bash를 사용하는 것이 매우 유용한 시나리오가 많이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="e3fd2-139">Bash 지원은 보완적이며 Windows에서 명령줄의 가치를 강화하여 PowerShell 및 PowerShell 커뮤니티에서 널리 사용되는 다른 기술을 활용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="e3fd2-140">자세한 내용은 [Windows용 Bash: 뛰어난 기능 및 PowerShell에 대한 의미는 무엇일까요?](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)라는 PowerShell 팀 블로그를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="e3fd2-141">WSL에서 모든 Linux 앱을 실행할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="e3fd2-142">아니요!</span><span class="sxs-lookup"><span data-stu-id="e3fd2-142">No!</span></span> <span data-ttu-id="e3fd2-143">WSL은 필요한 사용자가 Windows에서 Bash 및 핵심 Linux 명령줄 도구를 실행할 수 있도록 설정하기 위한 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="e3fd2-144">WSL은 GUI 데스크톱 또는 애플리케이션(예: Gnome, KDE 등)을 지원하지 **않습니다**.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="e3fd2-145">또한 널리 사용되는 여러 서버 애플리케이션(예: Redis)을 실행할 수 있지만 프로덕션 서비스 호스팅에는 WSL을 추천하지 않습니다. Microsoft는 Azure, Hyper-V 및 Docker에서 프로덕션 Linux 워크로드를 실행하는 다양한 솔루션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="e3fd2-146">WSL이 포함된 Windows SKU는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="e3fd2-147">Linux용 Windows 하위 시스템은 Windows 10 1주년 및 크리에이터스 업데이트 이상의 Windows 데스크톱 버전에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="e3fd2-148">Fall Creators Update부터 WSL은 Windows의 데스크톱 및 서버 SKU에서 모두 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="e3fd2-149">WSL에서 지원하는 프로세서는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-149">What processors does WSL support?</span></span>
<span data-ttu-id="e3fd2-150">WSL은 x64 및 ARM CPU를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="e3fd2-151">내 C: 드라이브에는 어떻게 액세스하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-151">How do I access my C: drive?</span></span>
<span data-ttu-id="e3fd2-152">로컬 머신의 하드 드라이브에 대한 탑재 지점이 자동으로 만들어져 Windows 파일 시스템에 쉽게 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="e3fd2-153">**/mnt/\<드라이브 문자>/**</span><span class="sxs-lookup"><span data-stu-id="e3fd2-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="e3fd2-154">예를 들어 c:\에 액세스하려면 `cd /mnt/c`를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-154">Example usage would be `cd /mnt/c` to access c:\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="e3fd2-155">Linux 앱에서 Windows 파일을 사용하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="e3fd2-156">WSL의 이점 중 하나는 Windows 및 Linux 앱 또는 도구를 통해 파일에 액세스할 수 있다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="e3fd2-157">WSL은 머신의 고정 드라이브를 Linux 배포판의 `/mnt/<drive>` 폴더 아래에 탑재합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="e3fd2-158">예를 들어 `C:` 드라이브는 `/mnt/c/` 아래에 탑재됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="e3fd2-159">탑재된 드라이브를 사용하면 [Visual Studio](https://visualstudio.microsoft.com/vs/) 또는 [VS Code](https://code.visualstudio.com/)를 사용하여 `C:\dev\myproj\`에서 코드를 편집하고, `/mnt/c/dev/myproj`를 통해 동일한 파일에 액세스하여 Linux에서 해당 코드를 빌드/테스트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="e3fd2-160">**중요 참고 사항**: WSL을 사용하는 경우의 주요 제한 사항 중 하나는 Windows 앱 또는 도구를 사용하여 Linux 배포판의 파일 시스템에 있는 파일에 직접 액세스하여 변경할 수 없다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="e3fd2-161">다음을 참조하세요. [Windows 앱 및 도구를 사용하여 Linux 파일 변경 안 함](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="e3fd2-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="e3fd2-162">Linux 드라이브의 파일이 탑재된 Windows 드라이브와 다른가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="e3fd2-163">Linux 루트(예: `/`) 아래의 파일은 다음을 포함하지만 이에 국한되지 않는 Linux 특정 동작을 모방하는 WSL에서 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="e3fd2-164">잘못된 Windows 파일 이름 문자가 포함된 파일</span><span class="sxs-lookup"><span data-stu-id="e3fd2-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="e3fd2-165">관리자가 아닌 사용자에 대해 만들어진 symlink</span><span class="sxs-lookup"><span data-stu-id="e3fd2-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="e3fd2-166">chmod 및 chown을 통한 파일 특성 변경</span><span class="sxs-lookup"><span data-stu-id="e3fd2-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="e3fd2-167">파일/폴더 대/소문자 구분</span><span class="sxs-lookup"><span data-stu-id="e3fd2-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="e3fd2-168">탑재된 드라이브의 파일은 Windows에서 제어하며 다음과 같은 동작을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="e3fd2-169">대/소문자 구분 지원</span><span class="sxs-lookup"><span data-stu-id="e3fd2-169">Support case sensitivity</span></span>
   * <span data-ttu-id="e3fd2-170">모든 권한이 Windows 권한을 가장 잘 반영하도록 설정됨</span><span class="sxs-lookup"><span data-stu-id="e3fd2-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="e3fd2-171">apt-get upgrade를 실행할 때 많은 오류가 발생하는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="e3fd2-172">일부 패키지는 아직 구현하지 않은 기능을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="e3fd2-173">예를 들어 `udev`는 아직 지원되지 않으므로 여러 `apt-get upgrade` 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="e3fd2-174">`udev`와 관련된 문제를 해결하려면 다음 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="e3fd2-175">다음을 `/usr/sbin/policy-rc.d`에 작성하고 변경 내용을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="e3fd2-176">실행 권한을 `/usr/sbin/policy-rc.d`에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="e3fd2-177">다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="e3fd2-178">WSL 배포를 제거하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="e3fd2-179">1709(16299) 이전의 빌드에서 명령 프롬프트를 열고 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="e3fd2-180">스토어에서 설치된 WSL 배포는 다른 Windows 앱처럼 마우스 오른쪽 단추로 앱 타일을 클릭하고 [제거]를 클릭하거나 [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)을 사용하여 PowerShell을 통해 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="e3fd2-181">ping에서 권한 거부 오류가 생성되는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="e3fd2-182">14926 이전의 WSL 빌드에서 ping은 WSL이 관리자 권한으로 실행되는 콘솔을 통해 실행되도록 요구했습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="e3fd2-183">이 문제는 14926 빌드 이상에서 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="e3fd2-184">OpenSSH 서버를 실행하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="e3fd2-185">WSL에서 OpenSSH를 실행하려면 Windows의 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="e3fd2-186">OpenSSH 서버를 실행하려면 Windows의 Ubuntu에서 관리자 권한으로 Bash를 실행하거나 CMD/PowerShell 프롬프트에서 관리자 권한으로 bash.exe를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="e3fd2-187">설치하려고 하면 "오류: 0x80040306"이 발생하는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="e3fd2-188">WSL은 레거시 콘솔에서 실행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="e3fd2-189">레거시 콘솔을 해제하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="e3fd2-190">WSL, PowerShell 또는 Cmd를 엽니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="e3fd2-191">마우스 오른쪽 단추로 제목 표시줄-> 속성을 차례로 클릭하고, "레거시 콘솔 사용"의 선택을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="e3fd2-192">확인을 클릭합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="e3fd2-193">Windows를 업그레이드한 후 bash.exe를 실행하면 "오류: 0x80040154"가 발생하는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="e3fd2-194">Windows 업데이트 중에 "Linux용 Windows 하위 시스템" 기능이 사용하지 않도록 설정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="e3fd2-195">이 문제가 발생하면 Windows 기능을 다시 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="e3fd2-196">"Linux용 Windows 하위 시스템" 기능을 사용하도록 설정하는 방법에 대한 지침은 [설치 가이드](https://docs.microsoft.com/en-us/windows/wsl/install-win10#install-the-windows-subsystem-for-linux)에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="e3fd2-197">WSL의 표시 언어를 변경하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="e3fd2-198">WSL 설치는 Windows 설치의 로캘과 일치하도록 Ubuntu 로캘을 자동으로 변경하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="e3fd2-199">이 동작을 원하지 않는 경우 설치가 완료된 후 다음 명령을 실행하여 Ubuntu 로캘을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="e3fd2-200">이 변경 내용이 적용되려면 bash.exe를 다시 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="e3fd2-201">아래 예제에서는 로캘을 en-US로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="e3fd2-202">WSL에서 인터넷에 액세스할 수 없는 이유는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="e3fd2-203">일부 사용자가 WSL에서 인터넷 액세스를 차단하는 특정 방화벽 애플리케이션의 문제를 보고했습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="e3fd2-204">보고된 방화벽은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="e3fd2-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="e3fd2-205">Kaspersky</span></span>
1. <span data-ttu-id="e3fd2-206">AVG</span><span class="sxs-lookup"><span data-stu-id="e3fd2-206">AVG</span></span>
1. <span data-ttu-id="e3fd2-207">Avast</span><span class="sxs-lookup"><span data-stu-id="e3fd2-207">Avast</span></span>

<span data-ttu-id="e3fd2-208">방화벽을 해제하면 액세스가 허용되는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="e3fd2-209">단순히 방화벽을 설치하면 경우에 따라 액세스가 차단되는 것처럼 보입니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="e3fd2-210">Windows의 WSL에서 포트에 액세스하려면 어떻게 하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="e3fd2-211">WSL은 Windows에서 실행되는 Windows의 IP 주소를 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="e3fd2-212">따라서 localhost의 모든 포트에 액세스할 수 있습니다. 예를 들어 1234 포트에 웹 콘텐츠가 있는 경우 https://localhost:1234 를 Windows 브라우저에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="e3fd2-213">내 WSL 배포판을 백업하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="e3fd2-214">배포판을 백업하는 가장 좋은 방법은 Windows 버전 1809 이상에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="e3fd2-215">`wsl --export` 명령을 사용하여 전체 배포를 tarball로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="e3fd2-216">그런 다음, `wsl --import` 명령을 사용하여 이 배포판을 WSL로 다시 가져와서 WSL 배포 상태를 백업하고 저장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="e3fd2-217">Appdata 폴더의 파일을 백업하는 기존 백업 서비스(예: Windows Backup)는 Linux 파일을 손상시키지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="e3fd2-218">피드백을 어디에 제공할 수 있나요?</span><span class="sxs-lookup"><span data-stu-id="e3fd2-218">Where can I provide feedback?</span></span>

<span data-ttu-id="e3fd2-219">여러 채널을 통해 피드백을 공유하고 질문할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-219">You can share feedback and ask questions through multiple channels.</span></span>

<span data-ttu-id="e3fd2-220">기술적인 문제가 있거나 새로운 기능을 요청하려면 Github 문제 추적기로 이동하세요.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-220">If you have technical issues, or want to request new features please go to our Github issue tracker:</span></span>
* [<span data-ttu-id="e3fd2-221">GitHub 문제 추적기</span><span class="sxs-lookup"><span data-stu-id="e3fd2-221">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

<span data-ttu-id="e3fd2-222">최신 WSL 뉴스를 최신 상태로 유지하려면 다음을 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-222">If you'd like to stay up to date with the latest WSL news you can do so with:</span></span>
* <span data-ttu-id="e3fd2-223">[명령줄 팀 블로그](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="e3fd2-223">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="e3fd2-224">Twitter.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-224">Twitter.</span></span> <span data-ttu-id="e3fd2-225">Twitter에서 [@craigaloewen](https://twitter.com/craigaloewen)를 팔로우하여 뉴스, 업데이트 등에 대해 알아보세요.</span><span class="sxs-lookup"><span data-stu-id="e3fd2-225">Please follow [@craigaloewen](https://twitter.com/craigaloewen) on Twitter to learn of news, updates, etc.</span></span>
