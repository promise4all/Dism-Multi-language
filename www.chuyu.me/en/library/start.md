> * Under Construction
* You can commit your translations [here] (https://github.com/Chuyu-Team/Dism-Multi-language/tree/master/www.chuyu.me/en) if you want to help us to translate the English documentations.

![Welcome to Dism++] (../images/logo.png "Welcome to Dism++")

## About Dism++ - ** We are in the frontline! **

Dism++ can be considered as a GUI frontend of DISM, but it is based on low-level Component Based Servicing (CBS) interface instead of DISM API or DISM Core API.


### Dism++ features
* Dism++ compatible with Windows Vista or later, without any Windows ADK DISM components requirements. If you use Microsoft's, it requires 3 versions of Windows ADK DISM components.
* Dism++ is the intersection of Dism, provides a complete graphical operation, almost all of Dism's features and a large number of features that Dism originally did not support. Manage Updates, Drivers, Features, Appx, Optional Features, Services, Compact/WIMboot, System Repair etc ... Let's go.
* Dism++ provides complete WIM support (including ESD capture, ESD to ISO, release of segmented ESD and direct ISO support). It is worth mentioning that ESD to ISO, Dism++ can decrypt directly in memory without modifying the hard disk data. This greatly satisfies the obsessive-compulsive disorder patients. `
* Dism++ provides open cleanup and optimization features, users can customize the Dism++ rules to create proprietary system tools.

[[BUG Feedback] (https://github.com/Chuyu-Team/Dism-Multi-language/issues)]
[[QQ Group 200783396] (http://shang.qq.com/wpa/qunwpa?idkey=07a04c095aee1e31f54b82ba98499a5b49aa10185f975946243ba68e0134a34e)]

### Donate to Dism++
The donation will be used to pay for the server, and if you are full of pride, you may still be able to pay the rent. In order to consider from a sustainable point of view, it is recommended that you sponsor once a year, each about 20RMB.

`Tips: sponsorship is not equal to paid support, this software for personal hobby amateur maintenance. BUG feedback and suggestions for improvement do not guarantee 100% prompt response and processing. Therefore, do not sponsor Dism++ solely for later service support. `

![WeiXin] (../images/weixin.png)! [Alipay] (../images/1487498940074.jpg)

## Minimum requirements of Dism++

Minimum: Windows NT 6.0 or later, 512 MB Physical Memory

Recommend: Windows NT 6.1 or later, an AMD64 processor, 8 GB Physical Memory and 8 GB Pagefile or higher

> * You can only run Dism++ on x86 and AMD64 processors. IA64, ARM and ARM64 images only support the offline mode.
* Dism++ does not support x86 images if it lacks WOW64 support in AMD64 Windows. (AMD64 Windows ADK PE is an example.)
* Features like CompactOS, WIMBoot and etc are unavailable in Windows Vista and Windows Server 2008.

## The file list of Dism++

Here are the all files about Dism++. You can delete files which you do not need. Lazy people ignore the following.

| File Name | Description
| -------- | -------
| Dism++ x64.exe | 64-bit system UI, on a 64-bit system, launches this program to render the UI. 32-bit system users may consider deleting this file.
| Dism++ x86.exe | The 32-bit system UI that automatically redirects to Dism++ x64.exe if you start this program on a 64-bit system. 64-bit system users may consider deleting this file.
| Config \ amd64 \ bcdboot.exe | Provide boot repair function, the original system comes with this file, delete has no effect. The original system users and 32-bit system users can delete this file.
| Config \ x86 \ bcdboot.exe | Provide boot repair function, the original system comes with this file, delete has no effect. The original system users and 64-bit system users can delete this file.
| Config \ amd64 \ CBSHost.dll | Dism++ API support module, 64-bit systems will not be able to use Dism++ after deletion. 32 users can delete this file.
| Config \ x86 \ CBSHost.dll | Dism++ API support module, 32-bit systems will not be able to use Dism++ after deletion, 64-bit systems will not be able to process 32-bit systems offline. 64-bit users who do not need offline processing of 32-bit systems may consider deleting.
| Config \ amd64 \ NCleaner.dll | 64-bit NCleaner cleanup engine, some advanced cleanup features will be disabled if missing, and 32 users can consider deleting this file.
| Config \ x86 \ NCleaner.dll | 32-bit NCleaner clean-up engine, some of the advanced cleanup features will be unavailable after missing this file, 64-bit users can consider deleting this file.
| Config \ amd64 \ wimgapi.dll | WIM file operation support module, Win10 users, 32-bit users or users who do not need any WIM-related features, then consider deleting.
| Config \ x86 \ wimgapi.dll | WIM file operation support module, Win10 users, 64-bit users, or users without any WIM related features.
| Config \ amd64 \ wofadk.sys <br> Config \ x86 \ wofadk.sys | Win10 users who provide support for Compact functions that do not require offline processing may wish to consider deleting this file. It is strongly recommended not to delete these files.
| Config \ Plugins | Dism++ plug-in support, users who do not need plug-ins can delete this file.
| Config \ Languages ​​| Dism++ language files to China, for example, only retain zh-Hans.zip can.
| Config \ Data.zip | This file holds the cleanup rules, ESD decryption KEY, and so on. This file is not allowed to be deleted.
| Config \ UpdateInfo.zip <br> Config \ UpdateInfoBeta.zip | Dism++ Update metadata to determine if a new version exists and to prevent users from downgrading to a new version. Recommended to retain, delete will be re-downloaded.
| Config \ default.ui.zip | This file saves Dism++'s UI. This file is not allowed to be deleted.
| Config \ wsusscn2.cab | Windows Update database file for scanning updates. Can consider deleting.
| Config \ include \ Dism++. H | This file is only available in beta. C Script supports header files. C Script scripts will not be available without this file.
| Config \ amd64 \ CScript.dll | This test only exists for the beta version. The 64-bit C Script Scripting Engine does not support the use of C Script scripts in the absence of this file. 32-bit users can consider deleting this file.
| Config \ x86 \ CScript.dll | This beta is available only in beta. The 32-bit C Script Scripting Engine will not work without this file, and 64-bit users can consider deleting this file.
