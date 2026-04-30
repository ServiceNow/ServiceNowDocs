---
title: Now Assist for Operational Technology Manager \(OTM\) release notes
description: The ServiceNow Now Assist for Operational Technology Manager \(OTM\) application helps streamline processes in the Industrial Workspace related to your Operational Technology \(OT\) device data. Now Assist for Operational Technology Manager \(OTM\) is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-05"
reading_time_minutes: 3
---

# Now Assist for Operational Technology Manager \(OTM\) release notes

The ServiceNow® Now Assist for Operational Technology Manager \(OTM\) application helps streamline processes in the Industrial Workspace related to your Operational Technology \(OT\) device data. Now Assist for Operational Technology Manager \(OTM\) is a new application in the Zurich release.

## Now Assist for Operational Technology Manager \(OTM\) highlights for the Zurich release

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Find OT Configuration Management Database \(CMDB\) records more quickly by using the OT CMDB search function.
-   Simplify the upload, validation, and import of your OT device data by using the Import OT device spreadsheet into OT CMDB agentic workflow.

See [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

**Important:** Now Assist for Operational Technology Manager \(OTM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Operational Technology Manager \(OTM\) features

-   **[Search for related records in an OT CMDB table](https://www.servicenow.com/docs/access?context=search-related-records-ot-cmdb-tables-now-assist-otm&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the OT CMDB search function to find an OT configuration item \(CI\) and OT device information in an OT CMDB table.

-   **[Upload, validate, and import your OT device inventory spreadsheet using the Import OT device spreadsheet into OT CMDB agentic workflow](https://www.servicenow.com/docs/access?context=upload-import-validate-ot-device-inventory-spreadsheet&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the Import OT device spreadsheet into OT CMDB agentic workflow to begin the process for uploading, validating, and importing your OT device inventory into ServiceNow.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    [Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).


## Activation information

Now Assist for Operational Technology Manager \(OTM\) is a ServiceNow AI Platform feature that is available with activation of the Operational Technology Manager \(com.sn\_ot\_foundation\). For details, see [Install Operational Technology Manager](https://www.servicenow.com/docs/access?context=install-operational-technology-manager&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    Now Assist for Operational Technology Manager \(OTM\) \(com.sn\_otm\_gen\_ai\): Contains the features, AI agents, and agentic workflows for Now Assist for OTM.


## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Using Now Assist for OTM with the Operational Technology Manager, you can efficiently manage your OT device data.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

