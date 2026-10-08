---
title: Configure skills for potential gaps
description: The knowledge gaps feature identifies missing knowledge articles. Activate the Knowledge Gaps skill in the ServiceNow Otto AI Admin console before working with gaps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-in-knowledge-management/configure-na-km.html
release: zurich
product: Now Assist in Knowledge Management
classification: now-assist-in-knowledge-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure ServiceNow Otto in Knowledge Management, ServiceNow Otto in Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure skills for potential gaps

The knowledge gaps feature identifies missing knowledge articles. Activate the Knowledge Gaps skill in the ServiceNow Otto AI Admin console before working with gaps.

## Before you begin

Role required: knowledge\_admin and knowledge\_manager

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Locate and select **Platform** under **AI skills for knowledge**, and then select **Knowledge**, to open the AI skills for knowledge view.

3.  Locate the relevant **Knowledge gaps** skill card.

    You can enable or disable the following skills:

    -   You can activate or deactivate the **Knowledge gaps identification \(ITSM\)** skill.
    -   You can activate or deactivate the **Knowledge gaps identification \(CSM\)** skill.
    -   You can activate or deactivate the **Knowledge gaps identification \(HR\)** skill.
4.  Select **Activate** to navigate to the skill configuration page.

5.  In the **Choose input** section, select **Switch scope** using the toggle button, and specify the following fields:

<table id="table_erk_jmw_gfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

The table on which the skill is configured. This is a read-only field with a default value. It is not editable.

</td></tr><tr><td>

Fields

</td><td>

Specifies the fields which will be used to identify knowledge gaps. This is a read-only field with a default value. It is not editable.

</td></tr><tr><td>

Filter

</td><td>

Select **Edit conditions** and build filters by adding article related conditions such as article status, and the duration of this status.This is a configurable condition builder.

</td></tr><tr><td>

Gaps generation frequency

</td><td>

Set the frequency at which the job for identifying the gaps in the articles is run. **Note:**

-   The skill must be reset every time the frequency is set.
-   When you select the **Run once** option and activate the skill, the application runs the job immediately after its activation. Selecting any other option, runs the job soon after its activation and, as per the selected frequency in the subsequent runs.


</td></tr></tbody>
</table>6.  Select **Save and continue**.

7.  Review your inputs in the Review and activate section and select **Done**.


## Result

The skill is activated and gap recommendations appear on the home page. The skill activation does not happen instantly. The configuration inputs have to pass through a Group Action Framework to create the specified cluster of jobs. For more information see, [Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/group-action-framework.md).

**Parent Topic:**[Configuring ServiceNow Otto in Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-in-knowledge-management/configuring-now-assist-km.md)

**Related topics**  


[Knowledge Center Home Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/kc-home-page.md)

[Manage potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/address-knowledge-gaps.md)

[Group Action Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/group-action-framework.md)

