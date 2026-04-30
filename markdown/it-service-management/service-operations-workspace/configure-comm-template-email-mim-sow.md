---
title: Configure a communication template for email in Major Incident Management
description: Configure a communication templates for email in Major Incident Management to help reduce the efforts and time spent in creating and composing communication emails.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up communication templates and plans in Major Incident Management, Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure a communication template for email in Major Incident Management

Configure a communication templates for email in Major Incident Management to help reduce the efforts and time spent in creating and composing communication emails.

## Before you begin

The Major Incident Management plugin must be activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select **Configure** for Major Incident Management.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management.

3.  In the **Communication Template** section, select **Configure email** to display a list of available communication email templates.

4.  Select **New**.

5.  On the form, fill in the details.

<table id="table_hxq_dfw_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the email template.

</td></tr><tr><td>

Table

</td><td>

Table where the email template is applicable.

 **Note:** By default, the value is the Incident Communication Task \[incident\_alert\_task\] table.

</td></tr><tr><td>

Application

</td><td>

Application scope of the email template. The email template is available for all applications or for scoped applications.

</td></tr><tr><td>

Execution order

</td><td>

The sequence that the templates are applied. The template with lowest execution order is applied first. For example, a template with execution order = 100 is applied first then a template with execution order = 200.

</td></tr><tr><td>

Condition

</td><td>

Condition builder that sets the conditions that must be met to apply the email template when composing email communications.

</td></tr><tr><td class="sub-head" colspan="2">

Content

</td></tr><tr><td>

Subject

</td><td>

Subject line of the email.

</td></tr><tr><td>

Content Type

</td><td>

Content type of the email. Possible values:-   **HTML**: Enables you to add links, multimedia, and other HTML content to the email.
-   **Plain Text**: Enables you to add only text and other text-related features, such as bold and italics.


</td></tr><tr><td>

Body

</td><td>

Content for the body of the email.

 **Note:** Based on the option chosen in the **Content Type** field, the **Body** field enables you to add text or HTML-related content.

</td></tr><tr><td>

Select Variables

</td><td>

Add field variables to the **Body**.

</td></tr><tr><td class="sub-head" colspan="2">

Recipients

</td></tr><tr><td>

To

</td><td>

Users or recipient list to be added in the **To** section of the email.

</td></tr><tr><td>

Cc

</td><td>

Users or recipient list to be added in the **Cc** section of the email.

</td></tr><tr><td>

Bcc

</td><td>

Users or recipient list to be added in the **Bcc** section of the email.

</td></tr><tr><td class="sub-head" colspan="2">

Sender configuration

</td></tr><tr><td>

From Generation Type

</td><td>

Generation type of the email sent. This value provides information about the email sender displayed on the **From** section of the email. Possible values:-   **SMTP Email Account**: Email is generated and sent using the SMTP email account of the sender.The **From** section of the email sent displays the SMTP email account of the sender.
-   **Select from List**: The **From** section of the email sent displays the list of email addresses specified in the **Email Client from Address** field.
-   **Script**: Email is generated and sent using the script specified in the **Script For From** field. The From section of the email sent displays the sender name based on the script.
-   **Text**: The From section of the email displays the value specified in the **From** field.
-   **None**: The **From** section of the email sent displays no value.


</td></tr><tr><td>

Email Client from Address

</td><td>

Email address that is displayed on the **From** section of the email. You can add multiple email addresses.

 **Note:** This field is visible only if **From Generation Type** is set to **Select from List**.

</td></tr><tr><td>

Script For From

</td><td>

Script that is responsible for creating and sending the email.

 **Note:** This field is visible only if **From Generation Type** is set to **Select from List**.

</td></tr><tr><td>

From

</td><td>

Name or user that is displayed on the **From** section of the email.

 **Note:** This field is visible only if **From Generation Type** is set to **Select from List**.

</td></tr></tbody>
</table>6.  Select **Submit**.


