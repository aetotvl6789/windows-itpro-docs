---
title: Tabs on the SUA Tool Interface (Windows 10)
description: The tabs in the Standard User Analyzer (SUA) tool show the User Account Control (UAC) issues for the applications that you analyze.
ms.assetid: 0d705321-1d85-4217-bf2c-0ca231ca303b
ms.reviewer: 
manager: laurawi
ms.author: greglin
ms.prod: w10
ms.mktglfcycl: plan
ms.pagetype: appcompat
ms.sitesec: library
audience: itpro
author: greg-lindsay
ms.date: 04/19/2017
ms.topic: article
---

# Tabs on the SUA Tool Interface


**Applies to**

-   Windows 10
-   Windows 8.1
-   Windows 8
-   Windows 7
-   Windows Server 2012
-   Windows Server 2008 R2

The tabs in the Standard User Analyzer (SUA) tool show the User Account Control (UAC) issues for the applications that you analyze.

The following table provides a description of each tab on the user interface for the SUA tool.

|Tab name|Description|
|--- |--- |
|App Info|Provides the following information for the selected application:<li>Debugging information<li>Error, warning, and informational messages (if they are enabled)<li>Options for running the application|
|File|Provides information about access to the file system.<p>For example, this tab might show an attempt to write to a file that only administrators can typically access.|
|Registry|Provides information about access to the system registry.<p>For example, this tab might show an attempt to write to a registry key that only administrators can typically access.|
|INI|Provides information about WriteProfile API issues.<p>For example, in the Calculator tool (Calc.exe) in Windows® XP, when you change the view from **Standard** to **Scientific**, Calc.exe calls the WriteProfile API to write to the Windows\Win.ini file. The Win.ini file is writable only for administrators.|
|Token|Provides information about access-token checking.<p>For example, this tab might show an explicit check for the Builtin\Administrators security identifier (SID) in the user's access token. This operation may not work for a standard user.|
|Privilege|Provides information about permissions.<p>For example, this tab might show an attempt to explicitly enable permissions that do not work for a standard user.|
|Name Space|Provides information about creation of system objects.<p>For example, this tab might show an attempt to create a new system object, such as an event or a memory map, in a restricted namespace. Applications that attempt this kind of operation do not function for a standard user.|
|Other Objects|Provides information related to applications accessing objects other than files and registry keys.|
|Process|Provides information about process elevation.<p>For example, this tab might show the use of the CreateProcess API to open an executable (.exe) file that, in turn, requires process elevation that will not function for a standard user.|

