---
title: Create cases in Security Case Management
description: Cases are used to track information about a campaign or state actor threatening your organization. After a case is created, you can add artifacts that allow you to review and analyze all related information within a single case record.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create cases in Security Case Management

Cases are used to track information about a campaign or state actor threatening your organization. After a case is created, you can add artifacts that allow you to review and analyze all related information within a single case record.

## Before you begin

Role required: sn\_ti.case\_use

r

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Case Management** &gt; **All Cases**.

    The Security Cases list opens.

2.  Click **New**.

    The Security Cases screen opens.

    ![New security case](../image/new-sec-case.png)

3.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Case Number|\[Read only\] The case number.|
    |Case Name|Enter a descriptive name for the case.|
    |Case Type|Select the type of case being investigated.|
    |Rating|Select the importance of this case \(from Critical to Low\).|
    |Last Updated|\[Read only\] The date and time the case was last updated.|
    |Short Description|A brief description of the case.|

4.  Click the **Additional Case Details** tab.

    ![Additional details fields](../image/additional-details-tab.png)

5.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Created by|\[Read only\] The name of the user who created this case.|
    |State|The current state of the case. At case creation, the State defaults to Draft.|
    |Assigned to|Click the lookup icon and assign the case to an analyst.|
    |Work notes list|Click the lock icon and add internal users who can view work notes.|
    |Additional comments|As needed, enter notes on the case that will be visible to the customer.|
    |Work Notes|If needed, type a work note for the case.|

6.  Click **Submit**.

    After the record has been saved, you can click the **Case Artifacts** tab and [add artifacts to the case](add-records-to-cases.md).


-   **[Add artifacts to a case](add-records-to-cases.md)**  
After you have created a case, you can add artifacts, such as security incidents, CIs, and indicators of compromise, to the case. These artifacts act as clues in solving the case.
-   **[Associate MITRE-ATT&amp;CK information with security case](associate-mitre-att-ck-information-with-security-case-management.md)**  
Associate MITRE-ATT&amp;CK tactics and techniques to a security case for better security case management and threat analysis at a granular level.

**Parent Topic:**[Security Case Management](../concept/case-mgmt.md)

