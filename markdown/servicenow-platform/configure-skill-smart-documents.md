---
title: Configure the smart documents skill
description: The smart documents skill is activated by default on all the tables. Configure it to customize access control, specify which tables use it, or adjust display preferences to get document insights through conversational interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configure-skill-smart-documents.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist in Document Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the smart documents skill

The smart documents skill is activated by default on all the tables. Configure it to customize access control, specify which tables use it, or adjust display preferences to get document insights through conversational interactions.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

**Note:** From Zurich Patch 11 and Australia Patch 4 onwards, Smart documents skill is enabled by default for all tables. Disable it if not required on any table.

For earlier versions, see [Activate the smart documents skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/activate-smart-documents.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the workflow list, select **Platform**.

3.  In the Now Assist skills for Platform, locate the **Smart Documents** skill.

    **Note:** The smart documents skill is enabled by default. You can configure it to specify which tables should have the feature, manage user access, or customize display settings.

4.  Select options icon \[Omitted image "icon-um-more-options-vertical.png"\] Alt text: Options icon.

5.  Select **Edit**.

6.  In the Define Availability section, specify the tables where you want the smart documents skill to be enabled.

    **Note:** If you leave this section empty, the skill remains enabled on all tables. If you specify particular tables, the skill will be enabled only on those tables.

7.  Select **Save and continue** to go to the next step in the guided setup.

    A guided setup leads you through the configuration of the general details, input, prompt, availability, display, review, and activation of the customized skill.

8.  In the Define access section, determine the roles that have access to this skill.

9.  Select **Save and continue** to go to the next step in the guided setup.

10. In the Select Display section, choose where to display the Smart Documents.

11. Select **Save and continue**.

12. Review your selection and select **Done**.

    Your changes are applied. The smart documents skill is now enabled only on the tables you specified or on all the tables if left empty. The Ask Now Assist button displays according to your display preferences and role-based access settings.


