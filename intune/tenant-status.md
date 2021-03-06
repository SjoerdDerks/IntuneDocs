---
# required metadata

title: Microsoft Intune Tenant Status page
titleSuffix: Microsoft Intune
description: Use the Intune Tenant Status page to view important tenant details without leaving the Intune portal
keywords:
author: brenduns
ms.author: brenduns
manager: dougeby
ms.date: 02/23/2019
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---
# Intune Tenant Status page
The Tenant Status page is a centralized hub where you can view current and important details about your tenant. Details include license availability and use, connector status, and important communications about the Intune service.  

To view the dashboard, in the Azure portal go to **Intune > Tenant Status**.  Tenant Status appears under the **Help and support group**.  

The page is divided into four areas:

## Tenant details
Tenant details provide at-a-glance information about your tenant. View details like your tenant name and location, your MDM Authority, and your tenants service release number. The service release number is a link that opens the *What’s new in Intune* article on Microsoft docs. In *What's new*, you can read about the latest features and updates to the Intune service.  

This section also provides basic information about your available licenses and how many are assigned to users. Licenses for devices aren't shown.

## Connector status
Connector status is a one-stop location to review the status of all available connectors for Intune.  

Connectors are:
- **Connections you configure to external services**. For example, the *Apple Volume Purchase Program* service or the *Windows Autopilot* service.  Status for this type of connector is based on the last successful synchronization time.
- **Certificates or credentials that are required to connect to an external unmanaged service**, like *Apple Push Notification Services* (APNS) certificates. Status for this type of connector is based on the expiry timestamp of the certificate or credential.  

By default, the display shows up to five connectors. You can select **See all connectors** to expand this list to view all available connectors, including connectors you haven't configured for use.  

Unhealthy connectors always display at the top of the list. Next are connectors with warnings, and then the list of healthy connectors. Connectors you haven't yet configured appear last.

When there's more than a single connector of any one type, the status is a summary for all of those same connectors. The least healthy status of any single connector is used as the health for the group.  

**Connector status:**
- **Unhealthy:**
    - The certificate or credential has expired
    - The last synchronization was three or more days ago
- **Warning:**
    - The certificate or credential will expire within seven days
    - The last synchronization was more than one day ago
- **Healthy:**
    - The certificate or credential won't expire within the next seven days
    - The last synchronization was less than one day ago  

When you select a connector from the list, the portal presents the portal page that is relevant to creating or configuring that connector.  For example, when you select the **VPP Expiry Date** connector, the **iOS Volume-Purchased Program Tokens** page opens where you can view more details about that connector. You can then create a new configuration or edit and fix issues with an existing one.  

## Intune service health  
You can view details for active incidents and advisories without having to navigate to the Microsoft 365 Service Health Dashboard or the Message Center, both located in the Microsoft 365 admin center at https://portal.office.com. Only incidents where impact has been noted to affect your tenant are shown.  

When you select an incident, the incident details are presented directly in the Tenant Status page. To view past advisories and incidents, select **See past Incidents/Advisories**. The Microsoft 365 admin center opens and you can then view advisories and incidents from the last 30 days for your tenant.  

To view information for *Intune Service Health*, your account must have the **Global Administrator** or **Service Administrator** role in Azure Active Directory or the Office Admin portal. To assign these permissions, sign in to the [Microsoft 365 admin center](https://portal.officeppe.com/AdminPortal/Home#/homepage) with Global Administrator permissions. Select **Users > Active Users**, and then select the account that requires access. Select **Edit** for Roles, select *Service Administrator* or *Global Administrator*, and then **Save** your edit to assign the permissions.  

You can only set up your communication preferences for Intune Service Health through the Microsoft 365 admin center.

## Intune news  
View informational communications from the Intune service team without having to navigate to the Office Message Center. Communications include messages about changes that have recently happened to the Intune service, or that are on the way for your tenant.  

By default, the last 10 active messages display. To view older messages, select **See past Messages** to open the *Message center* in the Microsoft 365 admin center portal.  

To view information for Intune News, your account must have the **Global Administrator** or **Service Administrator** role in Azure Active Directory, or the **Message Center reader** role in the Office Admin portal.  To assign this permission, sign in to the [Microsoft 365 admin center](https://portal.officeppe.com/AdminPortal/Home#/homepage) with administrator permissions. Select **Users > Active Users**, and then select the account that requires access. Select **Edit** for *Roles*, select *Teams Communications Administrator*, and then **Save** your edit to assign the permissions.  

You can only set up your communication preferences for Intune News through the Microsoft 365 admin center.
