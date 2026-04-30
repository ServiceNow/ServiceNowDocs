---
title: Change Management release notes
description: The ServiceNow Change Management application provides a tool for managing the life cycle of all changes in your organization, enabling rapid changes without compromising stability and governance. Change Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Change Management release notes

The ServiceNow® Change Management application provides a tool for managing the life cycle of all changes in your organization, enabling rapid changes without compromising stability and governance. Change Management was enhanced and updated in the Yokohama release.

## Change Management highlights for the Yokohama release

-   Increase operational efficiency of tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Require specified field details to be updated before transitioning the state of a change request by converting existing optional fields to mandatory fields.
-   Restrict unauthorized access to Change Management tables using deny ACLs.

See [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=installed-with-cm-itsm-roles&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    With the sn\_service\_desk\_agent user role, increase operational efficiency by streamlining the process of asking about, gathering, and verifying information, as well as delivering quick resolutions. This role is designed for tier 1 service desk agents and is accessible when the ITSM Roles plugin \(com.snc.itsm.roles\) installed.

    The sn\_service\_desk\_agent role includes the following roles:

    -   sn\_incident\_write
    -   sn\_problem\_write
    -   sn\_change\_write
    -   sn\_request\_write
    -   tracked\_file\_reader
    Additionally, with the installation of the **ITSM Gen AI** \(**com.sn.itsm.gen.ai**\) plugin, the knowledge\_user and now\_assist\_panel\_user roles are integrated within the sn\_service\_desk\_agent role.

    The sn\_service\_desk\_agent user role can be used starting with Service Operations Workspace version 6.1.

-   **[Change model Type field](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    A new **Model** option has been added to the change model Type field to help users identify a change that is controlled by a change model. **Model** is the default if a Type has not been set for the change request of a certain change model.

-   **[No default Risk value for change requests](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    There is no longer a default value for the Risk field on the Change Request table. The Risk value is set to **-- None --** until the risk is evaluated for the change request. This change ensures that no risk value is pre-assigned, allowing for a more accurate assessment before advancing the change

-   **[Mandatory field transition condition](https://www.servicenow.com/docs/access?context=create-a-change-model&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Ensure mandatory fields are completed before advancing through states for a change request, as defined by the Change Model. This feature enables change managers to mandate the completion of required fields before states can progress according to the Change Model.

-   **[Deny-unless ACLs on core tables](https://www.servicenow.com/docs/access?context=features-itsm-enhanced-security-change&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Prevent unauthorized access to change\_request and change\_task tables using deny-unless ACLs. The deny-unless ACLs restrict access on these tables for a non-authenticated user to perform actions such as read, write, delete, or create.

    This feature is available for new or zBoot customers with the installation of the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin. Existing or upgrade customers must test and evaluate in their sub production instance before installing the plugin and implementing the security change in their production instance.


## Removed in this release

Change Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Activation information

Change Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

