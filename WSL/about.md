---
title: Linux용 Windows 하위 시스템 알아보기
description: Linux용 Windows 하위 시스템이 작동하는 방법에 대해 자세히 알아봅니다.
keywords: BashOnWindows, Bash, WSL, Windows, Windows 하위 시스템, GNU, Linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: fbb1ce5cf5d5c83e25d0a6a0cece7b70537a44a1
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200200"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="aed0f-104">Linux용 Windows 하위 시스템 설명서</span><span class="sxs-lookup"><span data-stu-id="aed0f-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="aed0f-105">Linux용 Windows 하위 시스템을 사용하면 개발자가 가상 머신의 오버헤드 없이 대부분의 명령줄 도구, 유틸리티 및 애플리케이션이 포함된 수정되지 않은 GNU/Linux 환경을 Windows에서 직접 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="aed0f-106">다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-106">You can:</span></span>

1. <span data-ttu-id="aed0f-107">[Microsoft Store](https://aka.ms/wslstore)에서 즐겨찾는 GNU/Linux 배포를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="aed0f-108">`grep`, `sed`, `awk` 또는 다른 ELF-64 이진 파일과 같은 일반적인 무료 명령줄 소프트웨어를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="aed0f-109">다음을 포함하여 Bash 셸 스크립트 및 GNU/Linux 명령줄 애플리케이션을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="aed0f-110">도구: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="aed0f-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="aed0f-111">언어: Javascript/node.js, Ruby, Python, C/C++, C# 및 F#, Rust, Go 등</span><span class="sxs-lookup"><span data-stu-id="aed0f-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="aed0f-112">서비스: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="aed0f-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="aed0f-113">자체 GNU/Linux 배포 패키지 관리자를 사용하여 추가 소프트웨어를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="aed0f-114">Unix와 같은 명령줄 셸을 사용하여 Windows 애플리케이션을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="aed0f-115">Windows에서 GNU/Linux 애플리케이션을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="aed0f-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="aed0f-116">시작</span><span class="sxs-lookup"><span data-stu-id="aed0f-116">Getting Started</span></span>

* [<span data-ttu-id="aed0f-117">Windows 10에 Linux 설치</span><span class="sxs-lookup"><span data-stu-id="aed0f-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="aed0f-118">명령 참조 살펴보기</span><span class="sxs-lookup"><span data-stu-id="aed0f-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="aed0f-119">질문과 대답 참조</span><span class="sxs-lookup"><span data-stu-id="aed0f-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="aed0f-120">팀 블로그</span><span class="sxs-lookup"><span data-stu-id="aed0f-120">Team Blogs</span></span>
*  [<span data-ttu-id="aed0f-121">비디오 및 블로그 모음이 포함된 게시물에 대한 개요</span><span class="sxs-lookup"><span data-stu-id="aed0f-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="aed0f-122">[명령줄 블로그](https://blogs.msdn.microsoft.com/commandline/)(활성)</span><span class="sxs-lookup"><span data-stu-id="aed0f-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="aed0f-123">[Linux용 Windows 하위 시스템 블로그](https://blogs.msdn.microsoft.com/wsl/)(기록)</span><span class="sxs-lookup"><span data-stu-id="aed0f-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="aed0f-124">게시물 및 문서</span><span class="sxs-lookup"><span data-stu-id="aed0f-124">Posts & Articles</span></span>
* [<span data-ttu-id="aed0f-125">Windows에서 Ubuntu 기반 Bash 실행</span><span class="sxs-lookup"><span data-stu-id="aed0f-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="aed0f-126">개발자가 Windows 10에서 Bash 및 사용자 모드 Ubuntu Linux 이진 파일을 실행할 수 있음</span><span class="sxs-lookup"><span data-stu-id="aed0f-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="aed0f-127">Windows의 Ubuntu – Windows 개발자를 위한 Ubuntu 사용자 공간</span><span class="sxs-lookup"><span data-stu-id="aed0f-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="aed0f-128">사용자 의견 제공</span><span class="sxs-lookup"><span data-stu-id="aed0f-128">Provide Feedback</span></span>
* [<span data-ttu-id="aed0f-129">GitHub 문제 추적기</span><span class="sxs-lookup"><span data-stu-id="aed0f-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

