---
title: Generate a Major Incident email content recommendation by using Now Assist for IT Service Management \(ITSM\)
description: Create a draft version of an email to communicate with stakeholders on a major incident using an email template. You can complete field values in the template using an AI-generated response. Use different GenAI variables in the template types for efficient communication with the requesters.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-03-24"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI]
breadcrumb: [Use, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Generate a Major Incident email content recommendation by using Now Assist for IT Service Management \(ITSM\)

Create a draft version of an email to communicate with stakeholders on a major incident using an email template. You can complete field values in the template using an AI-generated response. Use different GenAI variables in the template types for efficient communication with the requesters.

## Before you begin

**Note:** An admin must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) installed to enable the Major Incident Management email content recommendation skill. For more information on activating the plugin, see [Activate Incident Management - Major Incident Management](../../incident-management/task/activate-major-incident-management-plugin.md).

Role required: major\_incident\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace.**

2.  Using the List icon \(![List icon](../../../common/image/icon-list.png)\), open a major incident.

3.  Select the **Communicate** tab.

4.  Select **Compose** in any task where the channel is email.

    **Note:** The default template defined for the selected task displays in the **Email template** field. You can choose any template and any type of communication plan within the template for your communication.

    The following four types of communication plans are available by default:

    -   Ad hoc AI
    -   Business user AI
    -   End user AI
    -   Technical AI
    For more information, see these KB articles:

    -   [Email templates and Gen AI variables](https://www.servicenow.com/community/itsm-articles/email-templates-and-gen-ai-variables-for-mim-email-communication/ta-p/3242595)
    -   [Persona as an input for Gen AI email templates](https://www.servicenow.com/community/itsm-articles/major-incident-email-content-recommendation-persona-as-an-input/ta-p/3246356)
5.  Compose and send the email.

    1.  In the **To** field, enter one or more email addresses of the users you have to communicate with.

    2.  In the **Subject** field, enter a short reason for the communication.

    3.  In the body of the email, enter the message you want to communicate.

    4.  Select **Send**.


**Parent Topic:**[Using Now Assist for IT Service Management \(ITSM\)](../concept/using-now-assist-for-itsm.md)

