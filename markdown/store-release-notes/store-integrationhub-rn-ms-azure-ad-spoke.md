---
title: Microsoft Entra ID Spoke release notes
description: Version history for the Integration Hub Microsoft Entra ID Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-azure-ad-spoke.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Entra ID Spoke release notes

Version history for the Integration Hub Microsoft Entra ID Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.7.5 - June 2026**

    Fixed: Scripting defect

-   **Version 4.7.4 - March 2026**

    Fixed - Action: Look up Groups Stream

-   **Version 4.7.3 - December 2025**

    New: Action: Create Application Assignment, Look up Application Assignments Stream, Delete Application Assignment, and Look up People Stream by User

-   **Version 4.6.0 - September 2025**

    Fixed - Required ACL\(s\) and Role\(s\) for agents.

-   **Version 4.5.1 - August 2025**
    -   Fixed:
        -   AI Agents: Renaming and Output transformation strategy
        -   Azure AD Download User Job for Azure Gov Cloud
        -   User Onboarding flow
-   **Version 4.5.0 - March 2025**

    Minor release with new AI agents.

-   **Version 4.3.2 - February 2025**
    -   Pagination issue in Look up Service Principal Stream action is fixed.
    -   SSO Azure AD download applications job is fixed for Azure Gov Cloud env.
-   **Version 4.3.1 - November 2024**
    -   Changed: Look up Group Membership Stream now fetches assigned licenses as well.
    -   Fixed: Cosmetic label changes for Azure Active Directory to Entra ID.
-   **Version 4.3.0 - August 2024**

    New: Action: Look up Group Transitive Membership Stream

-   **Version 4.2.3 - March 2024**

    Fixed: Look up User action to support \# in the userPrincipalName.

-   **Version 4.2.2 - February 2024**

    Fixed: Auto-activation of shipped sample flows and subflows upon installing or upgrading the spoke.

-   **Version 4.2.1 - December 2023**
    -   Fixed: Be able to fetch groups whose name starts with a special character.
    -   Changed: Spoke name was changed from "Microsoft Azure Active Directory Spoke" to "Microsoft Entra ID Spoke"
-   **Version 4.2.0 - November 2023**

    Fixed: Create subscriptions if assignment required is set to no as well.

-   **Version 4.1.1 - September 2023**
    -   Fixed:
        -   Password generation error in Generate Random Password action
        -   Comma encoding in Azure user name
        -   The license requirements
-   **Version 4.1.0 - June 2023**

    New: Added actions: Add Owners to Group, Add Devices to Group, Delete Group, Look up Subscribed SKUs, and Look up Subscribed SKU.

-   **Version 4.0.0 - May 2023**
    -   New:
        -   Attribute API Version in the default alias for spoke i.e. AzureAD under Connections &amp; Credential Aliases
        -   Equivalent or better actions for those deprecated \(refer Removed section below\):
            -   Application Management:Look up App Roles Assignments Stream \(look\_up\_app\_roles\_assignments\_stream\), Revoke User Application Access \(revoke\_user\_application\_access\_v2\)
            -   Group Management:Add Users to Group \(add\_users\_to\_group\),Add Owner to Group \(add\_owner\_to\_group\_v2\),Add User to Group \(add\_user\_to\_group\_v2\),Create Office 365 Group \(create\_office\_365\_group\_v2\),Create Security Group \(create\_security\_group\_v2\),Look up Group \(look\_up\_group\),Remove Owner from Group \(remove\_owner\_from\_group\_v2\),Remove User from Group \(remove\_user\_from\_group\_v2\),Update Office 365 Group \(update\_office\_365\_group\_v2\)
            -   License Management:Assign User License \(assign\_user\_license\_v2\),Remove User License \(remove\_user\_license\_v2\)
            -   Organization Management: Look up Tenant \(look\_up\_tenant\)
            -   Password Management:Change Password \(change\_password\),Generate Random Password \(generate\_random\_password\_v2\),Look up Password Expiration \(look\_up\_password\_expiration\),Reset Password \(reset\_password\_v2\)
            -   User Management:Create User \(create\_user\_v2\),Delete User \(delete\_user\_v2\),Disable User \(disable\_user\_v2\),Enable User \(enable\_user\_v2\),Fetch Latest Delta Token for Users \(fetch\_latest\_delta\_token\_for\_users\_v2\),Is User Enabled \(is\_user\_enabled\),Is User in Group \(is\_user\_in\_group\_v2\),Does User owns Group \(does\_user\_owns\_group\),Look up User \(look\_up\_user\),Update User \(update\_user\_v2\)
        -   Action: Revoke User SignIn Sessions
    -   Changed:
        -   Actions: Renamed certain actions, renamed category for certain actions, added page size parameter for Stream actions, renamed certain inputs and outputs, used Attribute API Version in the REST step for the actions
            -   Look up Application List - Look up Applications Stream
            -   Add Device to Group
            -   Is Device in Group
            -   Remove Device from Group
            -   Look up Devices Stream
            -   Get Group List - Look up Groups Stream by Directory
            -   Look up Group Members Stream
            -   Look up Group Membership List - Look up Group Membership Stream by Directory
            -   Look up Groups Stream
            -   Look up Group Membership Stream
            -   Look up Assigned-To Service Principal - Look up App Role Assigned to Service Principal Stream
            -   Look up Service Principals
            -   Look Up Incremental Changes for Users - Look up Incremental Changes for Users Stream
            -   Look up User List - Look up Users Stream by Directory
            -   Look up Users Stream - Look up Users Stream
            -   Look up Sign Ins - Look up Sign Ins Stream
        -   Flows:User Onboarding,User Offboarding to use newer actions
        -   Sub-Flows:Add User to Group to use newer actions
        -   Added retry policy for all actions
        -   Added updated error handling for newly created actions
    -   Removed:
        -   Deprecated Actions \(by setting active=false\)
            -   Application Management: Look up App Roles Assignments \(look\_up\_app\_roles\_assignments\), Revoke User Application Access \(revoke\_user\_application\_access\)
            -   Group Management:Add Multiple Users To Group \(add\_multiple\_users\_to\_group\),Add Owner To Group \(add\_owner\_to\_group\),Add User To Group \(add\_user\_to\_group\),Create Office 365 Group \(create\_office\_365\_group\),Create Security Group \(create\_security\_group\),Look Up Group Details \(look\_up\_group\_details\),Remove Owner From Group \(remove\_owner\_from\_group\),Remove User From Group \(remove\_user\_from\_group\),Update Office 365 Group \(update\_office\_365\_group\),Look Up Group ID \(look\_up\_group\_id\)
            -   License Management: Assign User License \(assign\_user\_license\), Remove User License \(remove\_user\_license\)
            -   Organization Management: Look up Tenant \(lookup\_tenant\)
            -   Password Management: Change User Password \(change\_user\_password\), Generate Random Password \(generate\_random\_password\), Look up User Password Expiration Details \(look\_up\_user\_password\_expiration\_details\), Reset User Password \(reset\_password\)
            -   User Management:Create User \(create\_user\),Delete User \(delete\_user\),Disable User \(disable\_user\),Enable User \(enable\_user\),Fetch Latest Delta Token for Users \(fetch\_latest\_delta\_token\_for\_users\),Is User Enabled \(is\_user\_account\_locked\),Is User In Group \(is\_user\_in\_group\),Is User Owns Group \(is\_user\_owns\_group\),Look Up User Details \(look\_up\_user\_details\),Update User \(update\_user\),Look Up User ID \(look\_up\_user\_id\)
-   **Version 3.7.1 - January 2023**

    Fixed: Installation performance, hints for Auth URL and Revoke Token URL.

-   **Version 3.7.0 - September 2022**
    -   New: Added following actions for device management
        -   Add Device to Group
        -   Remove Device from Group
        -   Look up Devices Stream
        -   Is Device in Group
    -   Changed - Spoke name changed from Microsoft Azure AD to Microsoft Azure Active Directory
-   **Version 3.6.0 - May 2022**

    Patch release of Microsoft Azure AD for IntegrationHub.

-   **Version 3.5.0 - February 2022**

    New: Patch release of Microsoft Azure AD for IntegrationHub. This version includes bug fixes and a new action Generate Random Password.

-   **Version 3.3.1 - November 2021**
    -   Fixed:
        -   Fix for the Look up Group ID action when the display name input includes a special character.
        -   Security fixes
-   **Version 3.3.0 - October 2021**

    New: This version includes two new actions - Look up User Password Expiration Details, Add Multiple Users To Group, and related fixes.

-   **Version 3.2.0 - September 2021**
    -   Changed:
        -   Changes to naming convention and descriptions of below actions:
            -   List Service Principals - Look up Service Principal
            -   List Assigned-To Service Principal - Look up Assigned-To Service Principal
            -   Get Group List - Look up Group List
            -   List Sign Ins - Look up Sign Ins
            -   Get Application List - Look up Application List
            -   Get Group Membership List - Look up Group Membership List
            -   Get User List - Look up User List
        -   Description updated for:
            -   Look up Group List
            -   Look up Application List
            -   Look up Group Membership List
    -   Fixed: A fix for uninstall of spoke in Quebec Patch 5.
-   **Version 3.1.0 - August 2021**

    Minor release of the Microsoft Azure AD Spoke. This version includes two new actions - Look up User Stream, Look up Groups Stream and some fixes.

-   **Version 3.0.0 - July 2021**

    Microsoft Azure AD spoke provides actions to automate Microsoft Azure Active Directory tasks for user management, authentication, and group membership.


