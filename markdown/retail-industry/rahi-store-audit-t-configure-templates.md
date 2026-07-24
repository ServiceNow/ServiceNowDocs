---
title: Configure audit plan templates
description: As an Admin, modify the default Task Plan Template Configuration and Template Item Configurations, or create additional configurations to support new audit programs after the application is deployed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-t-configure-templates.html
release: australia
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 2
keywords: [configure audit templates, task plan template configuration, template item configuration, assignment rules, admin]
breadcrumb: [Configure, Retail]
---

# Configure audit plan templates

As an Admin, modify the default Task Plan Template Configuration and Template Item Configurations, or create additional configurations to support new audit programs after the application is deployed.

## Before you begin

-   The Retail Store Audit Operations application is installed on the instance.
-   Role required: `sn_rtl_store_audit.admin`

## About this task

The application ships a default Store Audit Plan Configuration \(`sn_task_plan_config`\) and associated Template Item Configurations as out-of-the-box seed data. You can modify this default setup or create additional configurations as audit programs evolve. All configurable values—default states, number prefixes—are stored in System Properties under the `sn_rtl_store_audit` scope.

## Procedure

1.  To modify an existing template configuration:
2.  Log in to the ServiceNow instance with Admin credentials.

3.  In the application navigator, navigate to the `sn_rtl_store_audit` application scope and open **Task Plan Template Configurations**.

4.  Select the configuration you want to modify, for example the default Store Audit Plan Configuration.

5.  Update the configuration fields as required—name, description, or the `playbook_record_generator` field reference.

6.  Click **Save**.

7.  To create a new template configuration:
8.  Navigate to **Task Plan Template Configurations** in the application navigator and click **New**.

9.  Complete the required fields: **Name**, Task Plan Config type, and the `playbook_record_generator` reference.

10. In the Template Item Configurations related list, click **New** and define the Store Case and Audit Task template item levels.

11. Click **Save**.

    The new configuration is available to Plan Authors when they use the Record Generator to create an audit plan.

12. To modify assignment rules:
13. Navigate to **Assignment Rules** \(`sysrule_assignment`\) in the platform.

14. Locate the out-of-the-box rules: **Assign Store Audit Case to Retail auditors** and **Assign Audit Task to Retail auditors**.

15. Open the rule you want to modify and update the conditions, assignment group, or priority order as required.

16. Click **Save**.

    The updated rule takes effect on the next matching record creation.


## Result

Template configurations and assignment rules are updated. Plan Authors can immediately use any new or modified configurations when authoring audit plans. Assignment rule changes apply to all subsequently generated records.

**Related topics**  


[Audit plan and playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-plan-playbook.md)

[Components installed with Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-reference.md)

