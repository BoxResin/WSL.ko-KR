---
title: WSL 배포를 위한 사용자 계정 만들기 및 업데이트
description: Linux용 Windows 하위 시스템의 사용자 계정 및 권한 관리에 대한 참조입니다.
keywords: BashOnWindows, Bash, WSL, Windows, Linux용 Windows 하위 시스템, Windows 하위 시스템, Ubuntu, 사용자 계정
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: e5fb773dd44abab7bcf289340da00f59528b88f7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/03/2020
ms.locfileid: "76973683"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="55e36-104">WSL 배포를 위한 사용자 계정 만들기 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="55e36-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="55e36-105">WSL을 사용하도록 설정하고 Microsoft Store에서 Linux 배포를 설치하면, 새로 설치된 Linux 배포를 열 때 완료해야 하는 첫 번째 단계는 **사용자 이름** 및 **암호**를 포함하여 계정을 만드는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="55e36-106">이 **사용자 이름** 및 **암호**는 Linux 배포에만 적용되며, Windows 사용자 이름에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="55e36-107">이 **사용자 이름** 및 **암호**를 만들면 해당 계정이 배포의 기본 사용자가 되고 시작 시 자동으로 로그인됩니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="55e36-108">이 계정은 `sudo`(슈퍼 사용자 작업) 관리 명령을 실행할 수 있는 Linux 관리자로 간주됩니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="55e36-109">Linux용 Windows 하위 시스템에서 실행되는 각 Linux 배포에는 고유한 Linux 사용자 계정과 암호가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="55e36-110">배포를 추가하거나, 다시 설치하거나, 다시 설정할 때마다 Linux 사용자 계정을 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="55e36-111">Linux 암호 재설정</span><span class="sxs-lookup"><span data-stu-id="55e36-111">Reset your Linux password</span></span>

<span data-ttu-id="55e36-112">암호를 변경하려면 Linux 배포(예: Ubuntu)를 열고 `passwd` 명령을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="55e36-113">현재 암호를 입력하고 새 암호를 입력하라는 메시지가 표시된 다음, 새 암호를 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="55e36-114">암호 잊음</span><span class="sxs-lookup"><span data-stu-id="55e36-114">Forgot your password</span></span>

<span data-ttu-id="55e36-115">Linux 배포용 암호를 잊은 경우 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="55e36-116">PowerShell을 열고, `wsl -u root` 명령을 사용하여 기본 WSL 배포의 루트를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

> <span data-ttu-id="55e36-117">기본값이 아닌 배포에서 잊어버린 암호를 업데이트해야 하는 경우 `Debian`을 대상 배포의 이름으로 바꾼 `wsl -d Debian -u root` 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-117">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="55e36-118">WSL 배포가 PowerShell 내의 루트 수준에서 열리면 `passwd` 명령을 사용하여 암호를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="55e36-119">새 UNIX 암호를 입력한 다음, 해당 암호를 확인하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="55e36-120">암호가 성공적으로 업데이트되었다는 메시지가 표시되면 `exit` 명령을 사용하여 PowerShell 내에서 WSL을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="55e36-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="55e36-121">1703(크리에이터스 업데이트) 또는 1709(Fall Creators Update)와 같은 초기 버전의 Windows 운영 체제를 실행하는 경우 [이 사용자 계정 업데이트 문서의 보관 버전](./user-support-archived.md)을 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="55e36-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
