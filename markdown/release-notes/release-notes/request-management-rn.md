---
title: Request Management release notes
description: The ServiceNow Request Management application enables catalog items to be requested and fulfilled based on defined flows. Request Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Request Management release notes

The ServiceNow® Request Management application enables catalog items to be requested and fulfilled based on defined flows. Request Management was enhanced and updated in the Yokohama release.

## Request Management highlights for the Yokohama release

-   Improve customer satisfaction and operational efficiency with the sn\_service\_desk\_agent role, which is dedicated to the tier 1 service desk agents.
-   Restrict unauthorized access to the Request Management tables using deny ACLs.
-   Quickly determine whether a configuration item \(CI\) is available to be added to the **Configuration item** field in the Requested item form by searching the an alphabetized list of available CIs rather than having to first find the CI class list.

See [Request Management](https://www.servicenow.com/docs/access?context=c_RequestManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[User role for service desk agents](https://www.servicenow.com/docs/access?context=req-mgmnt-roles-instld-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Improve operational efficiency by providing level 1 or tier 1 service desk agents with access to change, incident, problem, and request records by assigning the sn\_service\_desk\_agent user role.

    **Note:**

    The sn\_service\_desk\_agent user role is available starting with Service Operations Workspace version 6.1.

-   **[Enhanced security model adoption for Request Management](https://www.servicenow.com/docs/access?context=request-management-architecture&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Prevent unauthorized access to request-related tables using deny ACLs. Non-authenticated user cannot perform any actions such as read, write, delete, create, or report view.

    This feature is available for new or zBoot customers with the installation of the ITSM Enhanced Security Features \(com.snc.itsm.enhanced\_security\) plugin. Existing or upgrade customers must test and evaluate in their sub-production instance before installing the plugin and implementing the security change in their production instance.


## Changed in this release

-   **[Sorting configuration items in requested item forms](https://www.servicenow.com/docs/access?context=create-request-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The list of configuration items \(CIs\) displayed for the **Configuration item** field in the Requested item form is now displayed and sorted based on the CI names in alphabetical order instead of sorting by CI class and then presenting the CI names in alphabetical order within a class. This change means you can determine whether a particular CI is available more quickly.


## Activation information

Request Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)

