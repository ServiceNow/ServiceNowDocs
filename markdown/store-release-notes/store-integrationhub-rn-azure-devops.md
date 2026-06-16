---
title: Microsoft Azure DevOps Boards spoke release notes
description: Version history for the Integration Hub Microsoft Azure DevOps Boards spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-azure-devops.html
release: store
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure DevOps Boards spoke release notes

Version history for the Integration Hub Microsoft Azure DevOps Boards spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.1.0 - September 2025**

    Fixed - Required ACL\(s\) / Role\(s\) for agents

-   **Version 3.0.2 - August 2025**

    Fixed - AI Agents - Output response includes anchor tags that are now rendered as clickable link

-   **Version 3.0.1 - July 2025**

    Fixed: Event source, Triggers set to Published state.

-   **Version 2.0.1 - June 2025**

    Fixed: Actions: Look Up Projects Stream, Look Up Work Item Revisions Stream.

-   **Version 3.0.0 - May 2025**

    New: Added triggers for work item management.

-   **Version 2.0.0 - February 2025**
    -   New:
        -   Authentication template to setup the spoke with OAuth 2.0
        -   API Version set as v7.1
        -   Added new Actions with new design pattern: use connection and credential alias, enabled retry policy, improved error handling and complex object outputs
            -   Core Process Management
                -   Create Iteration \(create\_iteration\_v2\)
                -   Delete Iteration \(delete\_iteraiton\_v2\)
                -   Delete Team Iteration \(delete\_team\_iteration\)
                -   Look up Area by Path \(look\_up\_area\_by\_path\_v2\)
                -   Look up Area Path of a Team \(look\_up\_area\_path\_of\_a\_team\)
                -   Look up Area Paths \(look\_up\_area\_paths\)
                -   Look up Creatable Fields \(look\_up\_creatable\_fields\)
                -   Look up Editable Fields \(look\_up\_editable\_fields\)
                -   Look up Iteration by Path \(look\_up\_iteration\_paths\)
                -   Look up Iteration Paths of a Team \(look\_up\_iteration\_paths\_of\_a\_team\)
                -   Look up Processes \(look\_up\_processes\)
                -   Look up Queries by Wiql \(look\_up\_queries\_by\_wiql\)
                -   Look up Team Settings \(look\_up\_team\_settings\)
                -   Look up Teams \(look\_up\_teams\)
                -   Look up Work Item Data by ID \(look\_up\_work\_item\_data\_by\_id\)
                -   Look up Work Item Relations by ID \(look\_up\_work\_item\_relations\_by\_id\)
                -   Look up Work Item Type Fields by Process \(look\_up\_work\_item\_type\_fields\_by\_process\)
                -   Look up Work Item Types \(look\_up\_work\_item\_types\)
                -   Look up Work Item Types by Process \(look\_up\_work\_item\_types\_by\_process\)
                -   Look up Work Items \(look\_up\_work\_items\_v2\)
                -   Post Iteration to Team \(post\_iteration\_to\_iteam\_v2\)
                -   Update Iteration \(update\_iteration\_v2\)
                -   Look up Projects Stream \(look\_up\_projects\_stream\)
                -   Look up Work Item Links Stream \(look\_up\_work\_item\_links\_stream\)
                -   Look up Work Item Revisions Stream \(look\_up\_work\_item\_revisions\_stream\)
            -   Work Item Management
                -   Add Attachment \(add\_attachment\)
                -   Create Link between Work Items \(create\_link\_between\_work\_items\_v2\)
                -   Create Service Hook \(create\_service\_hook\)
                -   Create Work Item \(create\_work\_item\)
                -   Delete Link between Work Items \(delete\_link\_between\_work\_items\)
                -   Delete Work Item \(delete\_work\_item\)
                -   Update Work Item \(update\_work\_item\)
                -   Update Work Item Project Details \(update\_work\_item\_project\_details\)
    -   Removed:
        -   Deprecated Actions:
            -   Core Process Management
                -   Create Iteration \(create\_iteration\)
                -   Delete Iteration \(delete\_iteration\)
                -   Delink Iterations From A Team \(delink\_iteration\_from\_a\_team\)
                -   Get Area Paths of a Team \(get\_area\_paths\_of\_a\_team\)
                -   Get Areas Path \(get\_areas\_path\)
                -   Get Backlog and Default Iterations \(get\_default\_iteration\_of\_a\_team\)
                -   Get Creatable Fields \(get\_creatable\_fields\)
                -   Get Editable Fields \(get\_editable\_fields\)
                -   Get Iteration by Path \(get\_iteration\_by\_path\)
                -   Get Iteration Paths of a Team \(get\_itration\_paths\_of\_a\_team\)
                -   Get Processes \(get\_processes\)
                -   Get Projects \(get\_projects\_in\_ado\)
                -   Get Projects \(Metadata\) \(get\_projects\)
                -   Get Teams \(get\_teams\)
                -   Get Work Item Data By ID \(get\_work\_item\_data\_by\_id\)
                -   Get Work Item Relations \(get\_work\_item\_relations\)
                -   Get Work Item Type Fields By Process \(get\_work\_item\_type\_fields\_in\_a\_process\)
                -   Get Work Item Types \(get\_work\_item\_types\)
                -   Get Work Item Types By Process \(get\_work\_item\_types\_in\_a\_process\)
                -   Look up Area By Path \(look\_up\_area\_by\_path\)
                -   Look up Work Items \(look\_up\_work\_items\)
                -   Post Iteration to Team \(post\_iteration\_to\_team\)
                -   Query by Wiql \(query\_by\_wiql\)
                -   Reporting Work Item Revisions \(reporting\_work\_item\_revisions\)
                -   Reporting Work Item Links \(reporting\_work\_items\_links\)
                -   Update Iteration \(update\_iteration\)
            -   Work Item Management
                -   Add Attachment \(add\_attachment\_ado\)
                -   Create Child Link \(create\_link\_between\_work\_items\)
                -   Create Work Item \(create\_work\_item\_in\_azure\_devops\)
                -   Delete Work Item \(delete\_work\_item\_in\_azure\_devops\)
                -   Delink Work Items \(delete\_child\_linkeage\)
                -   Move To Project \(move\_project\)
                -   Register Service Hook \(register\_to\_azure\_devops\_service\_hook\)
                -   Update Work Item \(edit\_work\_item\_in\_azure\_devops\)
-   **Version 1.8.8 - October 2024**

    Fixed a bug.

-   **Version 1.8.7 - March 2024**

    Fixed: Issue related to formatting of the description field.

-   **Version 1.8.6 - December 2023**

    Fixed: Script utils AzureDevopsUtils makePayloadForLinkingWorkItems\(\) function now checks for connection to be active.

-   **Version 1.8.5 - October 2023**

    Fixed: Get Teams, Register Service Hook actions - API Version.

-   **Version 1.8.4 - September 2023**
    -   Fixed:
        -   Get Iterations Path action
        -   Get Projects action
-   **Version 1.8.3 - June 2023**

    Fix related to setting project size in Get Projects metadata action and error in Get Processes action.

-   **Version 1.8.1 - March 2023**
    -   Changed: Spoke name.
    -   Fixed: Issue related with formatting observed in 'Create Work Item' and 'Update Work item' actions.
-   **Version 1.8.0 - December 2022**
    -   New: Authentication template for spoke setup from the connections dashboard
    -   Fixed: Improve installation performance of spoke.
-   **Version 1.7.1 - September 2022**

    Fixed: Improve installation performance of spoke

-   **Version 1.7.0 - May 2022**

    New: Minor release of Azure DevOps Boards Spoke. This version adds three new actions - Look up Area by Path, Query by WIQL, Look up Work Items.

-   **Version 1.6.4 - August 2021**

    Azure DevOps Boards 1.6.4 is a patch release with minor patch fixes

-   **Version 1.6.3 - April 2021**

    Azure DevOps Boards 1.6.3 is a patch release with minor patch fixes

-   **Version 1.6.2 - February 2021**

    Azure DevOps Boards 1.6.2 is a patch release with fixes to key-value pair separation \(in Create Work Item\) and a fix for dynamic templates \('=' in a value was breaking inputs\).

-   **Version 1.6.1 - July 2020**

    New: This release of the Azure DevOps Boards spoke includes actions to get work item types and fields by process id, and to get all processes of a given organization.

-   **Version 1.5.6 - May 2020**

    New: Support for retrieving work items using Azure DevOps Boards Reporting API.

-   **Version 1.5.5 - April 2020**

    New: Support for Azure DevOps Boards Iterations

-   **Version 1.0.5 - December 2019**

    Provides actions to automate work item and metadata retrieval management in Azure DevOps Boards.


