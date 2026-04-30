---
title: Microsoft Exchange Online integration
description: For the Microsoft Exchange Online integration application by ServiceNow, the ServiceNow AI Platform Security Incident Response \(SIR\) product is integrated with the Microsoft Exchange Online service, one of the cloud-based services in the Microsoft Office 365 suite of products. Your Security Operation Center \(SOC\) analyst can search your corporate email environment for security-related threats and remove and remediate phishing emails with email search and delete capabilities.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Exchange Online integration

For the Microsoft Exchange Online integration application by ServiceNow, the ServiceNow AI Platform® Security Incident Response \(SIR\) product is integrated with the Microsoft Exchange Online service, one of the cloud-based services in the Microsoft Office 365 suite of products. Your Security Operation Center \(SOC\) analyst can search your corporate email environment for security-related threats and remove and remediate phishing emails with email search and delete capabilities.

## Overview of Microsoft Exchange Online integration

As the security incident analyst, you execute the integration from the security analyst interface, and the workflow returns email message details that match search criteria. Email searches are based on criteria that include subject lines as well as sender and recipient email addresses. After the email search is complete, you can delete suspicious emails from the Microsoft Exchange Online service, and, an optional approval process can be configured to request approval prior to deleting emails.

This email search and delete integration can be used with a broader phishing response incident workflow or runbook. After a corporate user or employee receives a suspicious email and reports it to the company's phishing response team or inbox, the reported email is forwarded to the ServiceNow AI Platform and categorized as a security incident. After you have verified that an email is a phishing attack, as the analyst responsible for investigating phishing incidents, you can initiate an email search to determine if other corporate users have received this phishing email. The search allows you to locate related emails from the same phishing campaign and identify other potential victims who may have received the email, read it, and also potentially clicked a malicious URL or opened an attachment.

## Key features

The integration includes the following key features:

-   Configure search criteria for phishing threats in Security Incident Response based on combinations of the sender, recipient, and subject fields on email messages.
-   For large and lengthy email searches, the security incident analyst is notified via email when the search has successfully completed, along with the number of matched messages.
-   Status for individual messages informs you if recipients have read or deleted suspicious emails.
-   If configured, optional approval processes ensure that suspicious emails are not deleted without prior approval.
-   A complete audit trail for delete requests that includes the number of deleted emails is logged in the work notes of security incidents.
-   If tagging is configured, security tags record when email search and delete workflows are initiated and successfully completed on security incidents.

## Supported Microsoft Exchange Online versions

This integration supports Microsoft Exchange Online services, which are part of the Microsoft Office 365 suite. The integration does not support hosted Microsoft Exchange environments. Microsoft runs Microsoft Exchange Online services on the Exchange 2016 version.

## Prerequisites

The com.snc.si\_dep plugin is required for any ServiceNow AI Platform version. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before installing and activating the other Security Operations applications.

The following Security Operations applications must be installed and activated from the ServiceNow Store. Install and then activate one application at a time in the order listed below to ensure a smooth installation:

1.  Security Integration Framework
2.  Security Support Common
3.  Security Support Orchestration
4.  Security Incident Response

1.  [Set up your Microsoft Azure account](../task/ms-azure-account.md)  
Complete the following setup tasks in your Microsoft Azure portal prior to installing the ServiceNow application for this integration. This account permits access to the Microsoft Exchange Online tenant for email message details.
2.  [Install Microsoft Exchange Online application](../task/install-and-configure-ms-exchange-online.md)  
Before you run the integration on your instance, install the Microsoft Exchange Online application for the integration from the ServiceNow Store.
3.  [Configure the Microsoft Exchange Online integration](../task/msx_configure.md)  
After you’ve installed the application from the ServiceNow Store, configure it to connect to your ServiceNow AI Platform instance. This activation activates the search and delete workflows.
4.  [Define email search criteria and request a search on the Microsoft Exchange Online service](../task/verify-expected-results-ms-exchange-online.md)  
As a user with the sn\_si.analyst role, define search criteria and submit an email search request based on incident details on a security incident record.
5.  [Request delete approval for emails on Microsoft Exchange online service](../task/ms-delete-email.md)  
After an email search is successfully completed and matching messages are identified, you can permanently delete all the suspicious emails from the Microsoft exchange online service that are related to the security incident and phishing campaign.
6.  [Approve delete email requests for the Microsoft Exchange Online integration](../task/ms-approve-delete.md)  
If the approval option is enabled in your ServiceNow AI Platform instance, requests to delete emails are sent to each member of the approval group via email. You select the approval group during the configuration step. Approvals provide your organization with an additional level of control over the deletion of emails.
7.  [Recover deleted emails on the Microsoft Exchange Online service](../task/ms-recover-deleted-emails.md)  
\(Optional\) As a Microsoft Exchange Administrator, you can recover deleted emails if your incident remediation requires that you to recover the emails deleted by the workflow of this integration.
8.  [Edit security tags for the Microsoft Exchange Online integration](../task/ms-edit-tags.md)  
You can edit the names and colors of the security tags in your ServiceNow AI Platform® instance for the Microsoft Exchange Online integration. These security tags help you quickly identify when email search either completes or fails. They also identify when requests to delete emails are initiated and when the email items are successfully deleted.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

