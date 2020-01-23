---
title: WSL 1과 WSL 2 간의 UX 변경 내용
description: WSL 1과 WSL 2 사이의 사용자 환경 변경
keywords: BashOnWindows, bash, wsl, wsl2, windows, linux, windowssubsystem, ubuntu, debian, suse, windows 10 용 windows 하위 시스템
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a8f298a69acf44f152da626a0ba571f6bba1970c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520562"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="2974d-104">WSL 1과 WSL 2 사이의 사용자 환경 변경</span><span class="sxs-lookup"><span data-stu-id="2974d-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="2974d-105">이 페이지에서는 WSL 1과 WSL 2 preview의 사용자 환경 차이를 모두 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="2974d-106">유의 해야 하는 주요 변경 내용은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="2974d-107">더 빠른 파일 성능 속도를 위해 linux 앱이 Linux 루트 파일 시스템에서 액세스할 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="2974d-108">WSL 2 preview의 초기 빌드에서는 localhost를 사용 하는 대신 IP 주소를 사용 하 여 네트워크 응용 프로그램에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="2974d-109">다음은 볼 수 있는 다른 변경 내용에 대 한 전체 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="2974d-110">WSL 2는 VHD ( [가상 하드웨어 디스크](https://en.wikipedia.org/wiki/VHD_(file_format)) )를 사용 하 여 파일을 저장 하 고 최대 크기에 도달 하면 확장 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="2974d-111">시작할 때 WSL 2는 이제 작은 메모리 비율을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="2974d-112">초기 미리 보기 빌드에서 OS 간 파일 액세스 속도가 느려집니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="2974d-113">Linux 루트 파일 시스템에 Linux 파일 저장</span><span class="sxs-lookup"><span data-stu-id="2974d-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="2974d-114">파일 성능 혜택을 누릴 수 있도록 Linux 루트 파일 시스템 내부의 Linux 응용 프로그램에 자주 액세스 하는 파일을 배치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="2974d-115">이러한 파일은 더 빠른 파일 시스템 액세스를 위해 Linux 루트 파일 시스템 내에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="2974d-116">Windows 앱이 Linux 루트 파일 시스템에 액세스할 수도 있습니다 (예: 파일 탐색기).</span><span class="sxs-lookup"><span data-stu-id="2974d-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="2974d-117">실행 시도: Linux 배포판의 홈 디렉터리에 있는 `explorer.exe .` 하 고 어떤 일이 발생 하는지 확인 하면 훨씬 쉽게 전환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="2974d-118">네트워크 응용 프로그램 액세스</span><span class="sxs-lookup"><span data-stu-id="2974d-118">Accessing network applications</span></span>
<span data-ttu-id="2974d-119">WSL 2 preview의 초기 빌드에서는 호스트 컴퓨터의 IP 주소를 사용 하 여 Linux에서 Windows server에 액세스 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-119">In the initial builds of the WSL 2 preview, you will need to access any Windows server from Linux using the IP address of your host machine.</span></span>

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="2974d-120">Linux에서 Windows 응용 프로그램 액세스</span><span class="sxs-lookup"><span data-stu-id="2974d-120">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="2974d-121">Windows 네트워크 응용 프로그램에 액세스 하려면 호스트 컴퓨터의 IP 주소를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-121">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="2974d-122">이렇게 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-122">You can do so with these steps:</span></span>

- <span data-ttu-id="2974d-123">`cat /etc/resolv.conf` 명령을 실행 하 고 `nameserver`약관에 따라 IP 주소를 복사 하 여 호스트 컴퓨터의 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-123">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="2974d-124">복사한 IP 주소를 사용 하 여 Windows 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-124">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="2974d-125">아래 그림은 Windows에서 실행 되는 Windows에서 실행 되는 node.js 서버에 연결 하 여이에 대 한 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-125">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="2974d-127">Windows에서 Linux 응용 프로그램 액세스</span><span class="sxs-lookup"><span data-stu-id="2974d-127">Accessing Linux applications from Windows</span></span>

<span data-ttu-id="2974d-128">사용 중인 Windows 버전에 따라 가상 컴퓨터의 IP 주소를 검색 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-128">Depending on which version of Windows you're using, you might need to retrieve the IP address of the virtual machine.</span></span> <span data-ttu-id="2974d-129">빌드가 18945 이상인 경우 평상시와 같이 `localhost` 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-129">If your build is 18945 or higher, you can use `localhost` just like normal.</span></span> 

#### <a name="accessing-linux-on-builds-lower-than-18945httpsblogswindowscomwindowsexperience20190726announcing-windows-10-insider-preview-build-18945"></a><span data-ttu-id="2974d-130">[18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/) 보다 낮은 빌드에서 Linux 액세스</span><span class="sxs-lookup"><span data-stu-id="2974d-130">Accessing Linux on Builds lower than [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)</span></span>

<span data-ttu-id="2974d-131">WSL 배포판 서버를 사용 하는 경우 배포판를 켜는 가상 머신의 IP 주소를 찾아 해당 IP 주소를 사용 하 여 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-131">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="2974d-132">이렇게 하려면 다음 단계를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-132">You can do that by following these steps:</span></span>

- <span data-ttu-id="2974d-133">WSL 배포판 내에서 `ip addr` 명령을 실행 하 여 배포판의 IP 주소를 가져온 다음 `eth0` 인터페이스의 `inet` 값에서 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-133">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="2974d-134">다음과 같이 grep를 사용 하 여 명령의 출력을 필터링 하 여 보다 쉽게 찾을 수 있습니다. `ip addr | grep eth0`.</span><span class="sxs-lookup"><span data-stu-id="2974d-134">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="2974d-135">위에서 찾은 IP를 사용 하 여 Linux 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-135">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="2974d-136">아래 그림에서는 Edge 브라우저를 사용 하 여 node.js 서버에 연결 하는 방법의 예를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-136">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Windows에서 Linux 네트워크 응용 프로그램에 액세스](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a><span data-ttu-id="2974d-138">기타 네트워킹 고려 사항</span><span class="sxs-lookup"><span data-stu-id="2974d-138">Other networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="2974d-139">원격 IP 주소를 통해 연결</span><span class="sxs-lookup"><span data-stu-id="2974d-139">Connecting via remote IP addresses</span></span>

<span data-ttu-id="2974d-140">원격 IP 주소를 사용 하 여 응용 프로그램에 연결 하는 경우 LAN (Local Area Network)의 연결로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-140">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="2974d-141">즉, 응용 프로그램에서 LAN 연결을 허용할 수 있는지 확인 해야 합니다. 즉, `127.0.0.1`대신 `0.0.0.0`에 응용 프로그램을 바인딩해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-141">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="2974d-142">예를 들어 flask를 사용 하는 python에서는 `app.run(host='0.0.0.0')`명령을 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-142">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="2974d-143">이러한 변경을 수행 하는 경우 LAN 으로부터의 연결을 허용 하므로 보안을 염두에 두십시오.</span><span class="sxs-lookup"><span data-stu-id="2974d-143">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a><span data-ttu-id="2974d-144">LAN (local area network)에서 WSL2 배포판에 액세스</span><span class="sxs-lookup"><span data-stu-id="2974d-144">Accessing a WSL2 distro from your local area network (LAN)</span></span>

<span data-ttu-id="2974d-145">WSL1 배포판를 사용 하는 경우 컴퓨터를 LAN에서 액세스할 수 있도록 설정한 경우 WSL에서 실행 되는 응용 프로그램을 LAN 에서도 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-145">When using a WSL1 distro, if your computer was set up to be accessed by in your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span> <span data-ttu-id="2974d-146">WSL2에는 자체 IP 주소가 있는 가상화 된 이더넷 어댑터가 있기 때문에 WSL2의 기본 사례가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-146">This isn't the default case in WSL2, as WSL2 has a virtualized ethernet adapter with its own IP address.</span></span> <span data-ttu-id="2974d-147">현재이 워크플로를 사용 하도록 설정 하려면 일반 가상 컴퓨터와 동일한 단계를 진행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-147">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="2974d-148">이러한 환경을 개선 하는 방법을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-148">We are looking into ways to improve this experience!</span></span>

#### <a name="ipv6-access"></a><span data-ttu-id="2974d-149">IPv6 액세스</span><span class="sxs-lookup"><span data-stu-id="2974d-149">IPv6 access</span></span>

<span data-ttu-id="2974d-150">WSL2 배포판는 현재 i p v 6에만 도달할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-150">WSL2 distros currently cannot reach IPv6 only addresses.</span></span> <span data-ttu-id="2974d-151">이 기능을 추가 하기 위해 노력 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-151">We are working on adding this feature.</span></span>

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="2974d-152">WSL 2는 VHD를 사용 하 고 최대 크기에 도달 하는 경우 수행할 작업을 이해 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-152">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="2974d-153">WSL 2는 ext4 파일 시스템을 사용 하는 VHD 내에 모든 Linux 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-153">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="2974d-154">이 VHD는 저장소 요구에 맞게 자동으로 크기가 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-154">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="2974d-155">또한이 VHD의 초기 최대 크기는 256GB입니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-155">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="2974d-156">배포판 크기가 256GB 보다 큰 경우 디스크 공간이 부족 하다는 오류가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-156">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="2974d-157">VHD 크기를 확장 하 여 이러한 문제를 해결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-157">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="2974d-158">이 작업을 수행 하는 방법에 대 한 지침은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-158">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="2974d-159">`wsl --shutdown` 명령을 사용 하 여 모든 WSL 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-159">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="2974d-160">배포판 설치 패키지 이름 ' PackageFamilyName ' 찾기</span><span class="sxs-lookup"><span data-stu-id="2974d-160">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="2974d-161">Powershell 프롬프트에서 (' 배포판 '이 (가) 배포 이름인 경우)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-161">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="2974d-162">WSL 2 설치에서 사용 되는 VHD 파일 fullpath를 찾습니다 .이 파일은 ' pathToVHD '입니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-162">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="2974d-163">다음 명령을 완료 하 여 WSL 2 VHD 크기를 조정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-163">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="2974d-164">관리자 권한으로 명령 프롬프트 창을 열고 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-164">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="2974d-165">WSL 배포판 시작</span><span class="sxs-lookup"><span data-stu-id="2974d-165">Launch your WSL distro</span></span>
6. <span data-ttu-id="2974d-166">WSL에서 파일 시스템의 크기를 확장할 수 있음을 인식 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="2974d-166">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="2974d-167">WSL 배포판에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-167">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="2974d-168">이 항목의 이름을 복사 합니다. 예를 들어/Hv/sdxx (X는 다른 문자를 나타냄)와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-168">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="2974d-169">앞에서 복사한 값을 사용 해야 하며, `apt install resize2fs`을 사용 해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-169">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="2974d-170">참고: 일반적으로 Windows 도구 또는 편집기를 사용 하 여 AppData 폴더 내에 있는 WSL 관련 파일을 수정 하거나 이동 하거나 액세스 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-170">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="2974d-171">이렇게 하면 Linux 배포판 손상 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-171">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="2974d-172">WSL 2는 시작 시 일부 메모리를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-172">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="2974d-173">WSL 2는 실제 Linux 커널의 경량 유틸리티 VM을 사용 하 여 뛰어난 파일 시스템 성능 및 전체 시스템 호출 호환성을 제공 하는 동시에 WSL 1로 신속 하 고 신속 하 게 통합 되 고 응답성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-173">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="2974d-174">이 유틸리티 VM에는 작은 메모리 공간이 있으며 시작 시 가상 주소 지원 메모리를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-174">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="2974d-175">총 메모리의 작은 부분으로 시작 되도록 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-175">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="2974d-176">초기 미리 보기 빌드에서 OS 파일 속도가 느립니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-176">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="2974d-177">Linux 응용 프로그램에서 Windows 파일에 액세스 하거나 Windows 응용 프로그램에서 Linux 파일에 액세스 하는 경우 WSL 1과 비교 하 여 파일 속도가 느려지는 것을 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-177">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="2974d-178">이는 WSL 2의 아키텍처 변경의 결과 이며, WSL 팀이이 환경을 개선할 수 있는 방법에 대해 적극적으로 조사 하 고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2974d-178">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
