---
title: Create Folder Templates
description: Use Folder Templates to automatically create unique folders for different Major Security Incident types. The folder templates within the File Explorer Component are used to create a base folder structure for the security incident in the Microsoft SharePoint.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure File Explorer Component, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create Folder Templates

Use Folder Templates to automatically create unique folders for different Major Security Incident types. The folder templates within the File Explorer Component are used to create a base folder structure for the security incident in the Microsoft SharePoint.

## Before you begin

As an MSI Administrator, you define the initial folder structure necessary to allow collaboration across different incident responder groups and assign appropriate access privileges at a sub folder level. Multiple configurations can be created for different Major Security Incident types using a condition builder for specific Major Security Incident field values, which includes allowing access to different users and user groups at each sub folder level.

**Note:** These folder templates are used by all major security incidents that meet the conditions specified in the condition builder. It is recommended that you consider using incident field variables, such as the incident number or category, to create unique root folder names that distinguish one set of subfolders with common folder names for one major security incident from similar folders with these names that are part of a different major security incident.

The defined Folder Templates configuration is applied to the major security incident only when the condition is matched.

**Note:** A base system configuration \(without any sub folders\), is applied to all the security incidents. You may either edit this default configuration to include specific subfolders or create a new configuration based on a specified set of major security incident field values. For example, category = malicious code activity.

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **File Explorer** &gt; **Folder Templates**.

2.  Click **New** for Root Folder Configuration.

3.  On the form, fill the fields.

    |Field Name|Description|
    |----------|-----------|
    |**Name**|Name of the folder template.|
    |**File Repository Drive**| |
    |**Root Folder Name**|Name of the Root Folder which will appear in Microsoft SharePoint as well as the File Explorer and should probably include incident field variables such as the major security incident number and category so that one major security incident can be distinguished from another one.|
    |**Table**| |

4.  Define the security incident **Condition** values.

    ![Folder templates](../image/folder-templates-file-explorer.png)

5.  **Update** the record.

    The sub folders are created with the defined values.

6.  Click the desired **Sub folder**.

    If you don't create a sub folder with an appropriate name then the sub folders names are created as **Default** in the **Subfolder Configurations** section. ![Subfolders](../image/folder-templates-subfolders.png). The same folder structure will be created automatically in the Microsoft SharePoint using the same access privileges that are configured on the **Folder Templates** page.

    **Note:**

    -   **Root Folder Name** allows field variable names as input, provided they are valid fields in the selected table. The field name must be enclosed in curly braces and is substituted by the field value during the flow execution runtime. For example, the Security Incident SIR001001, if \{number\} variable is configured in the **Root Folder Name** field, then the number is replaced with SIR001001 during the runtime.
    -   **Root Folder Name** does not support any of these characters: " \* : &amp;lt; &amp;gt; ? / \\ \| and also, should not end with a period \(.\). If you use the above mentioned characters, they will be replaced automatically with a space character during the runtime.
    -   If the **Root Folder** and **Sub folder** name exceeds the defined limit \(256 characters\) then the folder name is truncated.
    Following is the run time execution of Create Folder Structure subflow:

    ![Flow designer subflows](../image/fe-related-flow-designer-execution.png)


**Parent Topic:**[Configure File Explorer Component](../concept/file-explorer.md)

