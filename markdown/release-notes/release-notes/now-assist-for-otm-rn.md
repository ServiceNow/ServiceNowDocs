---
title: Now Assist for Operational Technology Manager \(OTM\) release notes
description: The ServiceNow Now Assist for Operational Technology Manager \(OTM\) application helps streamline processes in the Industrial Workspace related to your Operational Technology \(OT\) device data. Now Assist for Operational Technology Manager \(OTM\) is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-06-23"
reading_time_minutes: 4
---

# Now Assist for Operational Technology Manager \(OTM\) release notes

The ServiceNow® Now Assist for Operational Technology Manager \(OTM\) application helps streamline processes in the Industrial Workspace related to your Operational Technology \(OT\) device data. Now Assist for Operational Technology Manager \(OTM\) is a new application in the Zurich release.

## Now Assist for Operational Technology Manager \(OTM\) highlights for the Zurich release

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)

-   The Now LLM Service is no longer the default model provider for new or inactive AI assets.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Find OT Configuration Management Database \(CMDB\) records more quickly by using the OT CMDB search function.
-   Simplify the upload, validation, and import of your OT device data by using the Import OT device spreadsheet into OT CMDB agentic workflow.

See [Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-otm-landing.md) for more information.

**Important:** Now Assist for Operational Technology Manager \(OTM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Operational Technology Manager \(OTM\) features

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Search for related records in an OT CMDB table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/search-related-records-ot-cmdb-tables-now-assist-otm.md)**

    Use the OT CMDB search function to find an OT configuration item \(CI\) and OT device information in an OT CMDB table.

-   **[Upload, validate, and import your OT device inventory spreadsheet using the Import OT device spreadsheet into OT CMDB agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/upload-import-validate-ot-device-inventory-spreadsheet.md)**

    Use the Import OT device spreadsheet into OT CMDB agentic workflow to begin the process for uploading, validating, and importing your OT device inventory into ServiceNow.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    [Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/define-sec-controls-aw.md).


## Activation information

Now Assist for Operational Technology Manager \(OTM\) is a ServiceNow AI Platform feature that is available with activation of the Operational Technology Manager \(com.sn\_ot\_foundation\). For details, see [Install Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/install-operational-technology-manager.md).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    Now Assist for Operational Technology Manager \(OTM\) \(com.sn\_otm\_gen\_ai\): Contains the features, AI agents, and agentic workflows for Now Assist for OTM.


## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/operational-technology-manager.md)**

    Using Now Assist for OTM with the Operational Technology Manager, you can efficiently manage your OT device data.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/operational-technology-rn-landing.md)

