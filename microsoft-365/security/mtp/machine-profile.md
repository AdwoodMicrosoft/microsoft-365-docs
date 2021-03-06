---
title: Machine profile in Microsoft 365 security portal
description: View risk and exposure levels for a device in your organization. Analyze past and present threats, and protect the machine with the latest updates.
keywords: security, malware, Microsoft 365, M365, Microsoft Threat Protection, MTP, security center, Microsoft Defender ATP, Office 365 ATP, Azure ATP, machine page, machine list, machine profile
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: v-maave
author: martyav
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance  
ms.topic: article
search.appverid: met150
---

# Machine profile page

The Microsoft 365 security portal provides you with Machine profile pages, so you can assess the health and status of devices on your network. Each Machine profile page contains a wealth of information about the device.

You can review in-depth information about what software it is running, any past and present security events or alerts, and find links to relevant software patches.

You can also use the Machine profile to perform common security-related tasks, and quickly review basic details about the device.

## Navigating the Machine profile page

The machine profile page is broken up into three sections.

![Image of machine profile page with (1) Tab area (2) Sidebar and (3) Actions highlighted in red](../../media/mtp-machine-profile/mtp-machine-profile-all.png)

The main content area (1) contains seven tabs that you can toggle through to view different kinds of information about the machine.

The sidebar (2) lists basic details about the machine.

There are also response actions available in a header (3) before the sidebar and main content sections. You can use the actions in this header to perform common security-related tasks.

## Tabs section

The Machine profile tabs allow you to toggle through an overview of security details about the machine, and tables containing a list of alerts, a timeline, a list of security recommendations, a software inventory, a list of discovered vulnerabilities, and missing KBs (security updates).

### Overview tab

The default tab is **Overview**. It provides a quick look at the most important security fact about the device.

![Image of overview tab for Machine profile](../../media/mtp-machine-profile/overview.png)

Here, you can find a chart of the device's risk level and active alerts, any currently logged on users, a brief list of most and least frequent users, and security assessments that detail the device's exposure level, security recommendations, affected software, and discovered vulnerabilities.

### Alerts tab

The **Alerts** tab contains a list of alerts that have been reported on the device.

![Image of alerts tab for Machine profile](../../media/mtp-machine-profile/alerts.png)

You can customize the number of items displayed, as well as which columns are displayed for each item. The default behavior is to list 30 items per page, and have 11 columns toggled on to display.

The columns in this tab include information on the severity of the threat that triggered the alert, as well as status, investigation state, and who if anyone the alert has been assigned to.

The *impacted entities* column refers to the machine (entity) whose profile you are currently viewing, plus any other machines in your network that are affected.

Selecting an item from this list will open a link to the selected alert.

This list can be filtered by severity, status, or assignee.

### Timeline tab

The **Timeline** tab includes a interactive, chronological chart of events raised on the device. By moving the highlighted area of the chart, you can view events over different ranges of time. You can also type in a custom range of dates.

Below the chart is a list of events for the selected range of dates.

![Image of timeline tab for Machine profile](../../media/mtp-machine-profile/timeline.png)

The number of items displayed and the columns on the list can both be customized. The default columns list the event time, active user, action type, entities (processes), and additional information about the event.

Selecting an item from the list will open a flyout displaying an Event entities graph, showing the parent and child processes that triggered the event.

This list can be filtered by the specific kind of event; for example, Registry events or Smart Screen Events.

### Security recommendations tab

The **Security recommendations** tab lists actions you can take to protect the device. Selecting an item on this list will open a flyout where you can get instructions on how to apply the recommendation.

![Image of security recommendations tab for Machine profile](../../media/mtp-machine-profile/security-recs.png)

As with the previous tabs, the number of items displayed per page and which columns are visible can be customized.

The default view includes columns that detail the security weaknesses addressed, the associated threat, the related component or software affected by the threat, and more. Items can be filtered by the recommendation's status.

### Software inventory

The **Software inventory** tab lists software installed on the device.

![Image of software inventory tab for Machine profile](../../media/mtp-machine-profile/software-inventory.png)

The default view displays the software vendor, installed version number, number of known software weaknesses, threat insights, product code, and tags. The number of items displayed and which columns are displayed can both be customized.

Selecting an item from this list opens a flyout containing more details about the selected software, as well as the path and timestamp for the last time the software was found.

This list can be filtered by product code.

### Discovered vulnerabilities tab

The **Discovered vulnerabilities** tab lists any Common Vulnerabilities and Exploits (CVEs) that may affect the device.

![Image of discovered vulnerabilities tab for Machine profile](../../media/mtp-machine-profile/discovered-vulnerabilities.png)

The default view lists the severity of the CVE, the Common Vulnerability Score (CVS), the software related to the CVE, when the CVE was published, when the CVE was last updated, and threats associated with the CVE.

As with the previous tabs, the number of items displayed and which columns are visible can be customized.

Selecting an item from this list will open a flyout that describes the CVE.

### Missing KBs

The **Missing KBs** tab lists any Microsoft Updates that have yet to be applied to the machine. The "KBs" in question are [Knowledge Base articles](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) which describe these updates; for example, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).

![Image of missing kbs tab for Machine profile](../../media/mtp-machine-profile/missing-kbs.PNG)

The default view lists the bulletin containing the updates, OS version, products affected, CVEs addressed, the KB number, and tags.

The number of items displayed per page and which columns are displayed can be customized.

Selecting an item will open a flyout that links to the update.

## Sidebar

Beside the main content area of the Machine profile page is the sidebar.

![Image of sidebar tab for Machine profile](../../media/mtp-machine-profile/sidebar.png)

The sidebar provides some important basic information in small subsections which can be toggled open or closed:

* **Tags** - Any tags associated with the device
* **Security info** - Open incidents, active alerts, exposure level and risk level
* **Device details** - Domain, OS, Asset group, health state, data sensitivity, and IP addresses
* **Network activity** - Timestamps for the first time and last time the device was seen on the network

This section also includes the name and exposure level of the device, and an icon to indicate if it is currently active on the network.

## Response actions

Response actions offer a quick way to defend against and analyze threats.

![Image of sidebar tab for Machine profile](../../media/mtp-machine-profile/actions.PNG)

The response actions available to you here include:

* **Manage tags** - Updates custom tags you have applied to this device.
* **Isolate machine** - Isolates the machine from your organization's network while keeping it connected to Microsoft Defender Advanced Threat Protection. You can choose to allow Outlook, Teams, and Skype for Business to run while the machine is isolated, for communication purposes.
* **Restrict app execution** - Prevents applications that are not signed by Microsoft from running
* **Run antivirus scan** - Updates Windows Defender Antivirus definitions and immediately runs an antivirus scan. Choose between Quick scan or Full scan.
* **Collect investigation package** - Gathers information about the machine. When the investigation is completed, you can download it.
* **Initiate Live Response session** - Loads a remote shell on the machine for [in-depth security investigations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response).
* **Initiate automated investigation** - Automatically [investigates and remediates threats](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air). Although you can manually trigger automated investigations to run from this page, [certain alert policies](https://docs.microsoft.com/microsoft-365/compliance/alert-policies?view=o365-worldwide#default-alert-policies) trigger automatic investigations on their own.
* **Action center** - View the status of submitted actions. Only available if another action has already been selected.

## Related topics

* [Microsoft Threat Protection overview](microsoft-threat-protection.md)
* [Turn on Microsoft Threat Protection](mtp-enable.md)
* [Investigate entities on machines using live response](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response)
* [Automated investigation and response (AIR) in Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air)
