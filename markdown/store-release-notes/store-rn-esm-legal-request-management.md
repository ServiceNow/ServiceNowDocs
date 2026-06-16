---
title: Legal Request Management release notes
description: Version history for the Legal Request Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-request-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 16
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Legal Request Management release notes

Version history for the Legal Request Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.1.4 - June 2026**
    -   Changed:
        -   The platform\_ml\_read ACL on legal tables has been removed as part of a role cleanup, simplifying permission management.
        -   Enhanced UI for visual clarity in AI-assisted features.
    -   Fixed:
        -   Performance improvements were made while performing the 'Assign to me' actions on legal requests.
        -   Legal fulfiller users in the Legal Counsel Center can now see email client templates for Legal Request Management.
        -   Legal fulfiller users can now edit the due date on a legal request as expected.
        -   When creating a new task configuration, the values in the reference table are correctly displayed.
-   **Version 10.0.10 - May 2026**

    Fixed: Minor fixes.

-   **Version 10.0.6 - April 2026**
    -   Fixed:
        -   Installing the Legal Request Management plugin no longer changes the visibility and scope settings of the workspace view.
        -   The start date picker in Third Party Contract and Non disclosure agreement requests now correctly compare with the user’s local date and time, allowing users to select the next day’s date without receiving an error message.
-   **Version 10.0.3 - March 2026**
    -   New: Attorney Client Privilege enables legal fulfiller to designate legal requests as privileged and confidential. Attorney Client Privilege restricts access to authorized stakeholders, marks communications with confidentiality banners, and maintains a document audit trail to help you protect sensitive legal communications.
    -   Fixed:
        -   Unnecessary error message does not appear while submitting the contract request using the service portal.
        -   Folders are automatically created for SharePoint and Google Drive external storage integration even for non-admin users when a legal matter is initiated.
        -   Legal request notification emails now display the correct comment even when multiple comments are added in quick succession.
-   **Version 9.2.2 - January 2026**

    Fixed: Resolved RCA so that legal request details are visible to Gifts and Entertainment approver in Employee Center.

-   **Version 9.2.0 - December 2025**
    -   Changed: Security enhancements.
    -   Fixed:
        -   Resolved the External storage\(Google Drive\) permission issues related to collaborator on legal requests.
        -   Resolved the RCA issues.
        -   Resolved the langugae pack related issues while applying the Matter template.
        -   Resolved the user group listing issue during the Adhoc approval dialog when the fulfiller roles are inherited.
        -   Resolved misleading error message for attachment delete on legal request only in a certain case.
        -   Resolved the error during the transfer legal request by filtering out the inactive record producer records.
-   **Version 8.11.7 - October 2025**

    New: Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.

-   **Version 9.1.1 - September 2025**
    -   New: Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.
    -   Fixed:
        -   Users were unable to add a checklist on the intake form, and the "create new" button was not responding. This has been fixed.
        -   Addressed slow performance issues on workspace.
-   **Version 9.0.0 - August 2025**
    -   Fixed:
        -   The Interview Details section was incorrectly displayed even when the matter type was set to Data Collection. This issue has been fixed.
        -   The description field was not displayed by default available for the category table. This issue has been fixed.
        -   For a submitted request in Employee Center, the Request details tab was displayed twice. This issue has been fixed.
        -   When a user deletes an attachment from a Legal Request record, the worknote was updated indicating the attachment was deleted even when the deletion did not actually occur. This issue has been fixed.
        -   The signature type could not be modified when the request is in new, draft or work in progress. This issue has been fixed.
        -   The user and group filter was not working correctly for Initiate Approval. This issue has been fixed.
        -   Security issues.
-   **Version 8.11.3 - July 2025**
    -   Fixed:
        -   ACL issues
        -   Issue that caused a query range error to appear when navigating away from Matters - Unassigned, Matters - All, Matter tasks - All, and Artifacts - All list in the Legal Counsel Center after running the Writer audit script
-   **Version 8.11.1 - May 2025**
    -   Changed: Improved icons for Legal Service Delivery applications for improved space utilization in the intake forms.
    -   Fixed:
        -   For a legal request, the "Contract request" tab is not displayed. This issue has been fixed.
        -   In Core UI, when a legal request is transferred to another practice area, activity stream has comments that are duplicated.
        -   Customize the Legal Request form layout by removing Legal Request Variable Editor and save it. Open the form layout again, the request details and notes sections is also removed. This issue has been fixed
        -   Activity stream displayed irrelevant messages when an Non\_disclosure agreement was submitted with a contract document. This has been fixed.
        -   Security issues
-   **Version 8.9.0 - February 2025**
    -   Fixed:
        -   When a legal request is transferred to Contracts, the fulfiller is unable to edit the variable fields and submit the request. The Submit button is now not available for the fulfillers and the fulfiller can only select Send to requester when a legal request is transferred to Contracts.
        -   In Predictive Intelligence for Legal Service Delivery, failure to retrain a solution definition after editing. This has been fixed.
        -   UI issues
-   **Version 8.8.4 - December 2024**

    Fixed: The activity stream does not log the changes done to the Priority field of a Gifts &amp; entertainment request. This has been fixed.

-   **Version 8.7.2 - November 2024**
    -   Fixed:
        -   The View Request link in the email notifications for Legal Service Delivery directs the user to Legal Counsel Center Classic even when the new Legal Counsel Center is installed. It has been fixed now.
        -   The type field in the setup related for Content Review was not displaying any values. This is now fixed.
        -   Security fixes
        -   Performance improvements
-   **Version 8.5.3 - October 2024**

    Fixed: For Non-disclosure Agreement and Third-party contract review request, legal fulfiller is unable to upload a file when creating a new revision after working on change request.

-   **Version 8.6.0 - August 2024**
    -   Fixed:
        -   When you have installed Legal Request Management application only, you were not able to open legal request. This was because it has references to legal matter and matter template record.
        -   When you edit the description of a legal content review request, the changes made to the description were not displayed on the request when opened in Legal Service Portal.
        -   Cannot upload documents in a legal request when using iManage as an external storage.
        -   When adding a legal request to an existing matter, the add to existing matter pop-up doesn't list of available matters.
-   **Version 8.5.0 - May 2024**
    -   Changed: Updated UI labels.
    -   Fixed:
        -   When SharePoint is used as an external storage, an "Error uploading" error occurred when uploading an attachment to a legal request. This is now fixed.
        -   When transferring a third-party contract request to General Legal Request category, the Legal Request was successfully updated as Cancelled. However, the associated contract request remained in New state. This is now fixed.
        -   The field to select an existing matter in the Add to an existing matter pop-up was missing. This is now fixed.
        -   The Variables section in the Legal Request form in Legal Counsel Center was not displayed. This is now fixed.
        -   Third party contract revision upload to external storage failed when the default system language is set other than English. This is now fixed.
        -   Counsel Assist on Legal Counsel Center wasn't showing any information as the table configuration was not existing.
        -   Security fixes.
-   **Version 8.2.3 - March 2024**
    -   Fixed:
        -   Legal Counsel Center Workspace does not display variables.
        -   Failure to upload document when the default system language is set to any value other than English.
-   **Version 8.1.3 - November 2023**
    -   Fixed:
        -   Access to files and folders on iManage is provided while creating a legal matter and assigning it to a user group for Subpoena matters
        -   Values for Practice Area and Assignment group field are available
        -   A new document on a legal request with external storage can be attached
        -   File upload from the Legal Counsel Center to iManage is available
        -   Uploading of attachments can be done for SharePoint integrated requests in respective folders
        -   Updates to fields on the Legal Counsel Center \(Next Experience and Classic\) are saved when closing a request
-   **Version 8.0.10 - September 2023**
    -   Fixed:
        -   iManage:
            -   File upload failing from the Legal Counsel Center
            -   Error in processing document access is not processing other permissions requests
            -   Permissions are not getting synced to iManage
            -   When creating a legal matter and assigning it to a user group, the users do not get access to the files and folders on iManage for Subpoena matter
        -   Error when the legal configurer is trying to remove the template from the intake form
        -   Unable to attach new document on Legal request with external storage
-   **Version 8.0.5 - August 2023**

    New: Configure iManage as an external storage system integration to store documents attached to legal requests and matters.

-   **Version 7.1.11 - June 2023**
    -   Fixed:
        -   New Record Producers are not automatically displayed in the ESC portal when new customers install Legal Content Review and Legal Simple Privacy.
        -   When the Simple Contracts application is not installed, the Legal Request Ticket Page tabs are not visible.
        -   ACL Bypass via "transfer\_request" UI Page in Legal Simple Contracts.
-   **Version 7.1.6 - May 2023**
    -   New: An incorrect legal request can be transferred to a different practice area or category by the fulfillers when the request is in a new or assigned state
    -   Changed:
        -   The legal privacy assessment request functionality has been moved from Legal Request Management to the new application Legal Simple Privacy &gt; \(sn\_lg\_privacy\)
        -   The legal content review request functionality is moved from Legal Request Management to the new application Legal Content Review \(sn\_lg\_cont\_review\)
-   **Version 7.0.3 - February 2023**
    -   Changed: A Legal Request can be Closed or Cancelled with Matters still in Work in Progress state.
    -   Fixed: Fixed an issue that displayed a message to close all matters while close completing the requests when there are no matters associated to the request.
    -   Removed: Removed the Approval To-dos widgets as they are not required in the system.
-   **Version 6.2.12 - January 2023**
    -   Changed: Updated permissions for users with the report\_viewer role to view a few reports in the Legal Executive dashboard and Legal Counsel Center landing page.
    -   Fixed:
        -   Fixed an issue in Legal Counsel Center where the email details were not showing up in the Activities stream.
        -   Fixed an issue where a legal request created from a new intake form did not display the intake form's configured items.
        -   Fixed a cross-scope error that appeared while opening the Response Template Configurations module under Legal Administration.
-   **Version 6.2.5 - November 2022**
    -   New:
        -   Attachments deleted from a legal request are recorded as comments in the Activities.
        -   Added the Edit in Catalog Builder button on the Record Producer form to enable editing of the record producer in Catalog Builder.
        -   Added Configurations based on the new Approval Hub in the Employee Center to include approvals for legal requests and documents and attachments in legal requests.
        -   Enabled AI Search in the Legal Service Portal.
        -   Added Response Templates so that legal fulfillers can use reusable text in the work notes, comments, emails, or chats to communicate with stakeholders while working on legal requests.
    -   Changed:
        -   Access to attachments in the legal requests is removed for the admins.
        -   Access to all email notifications related to legal requests or legal matters is removed for the admins.
        -   Updated icons for the base system record producers.
        -   There is a 15-minute increase in upgrade time due to table modifications for customers.
-   **Version 6.1.2 - September 2022**

    Fixed: Fixed an issue where signed legal contracts were not uploading to the configured external storage.

-   **Version 6.1.1 - August 2022**
    -   New:
    -   -   Integration of legal requests with Universal Request to provide a seamless experience for fulfilling requests across the organization.
-   Added an email notification sent to the legal fulfillers when the ad hoc approvals are approved or rejected by the approver. If there are collaborators in the legal request, they are CC'd in the email.
-   Added Legal Integration properties to configure integrations for Legal Service Delivery apps.
    -   Changed:
        -   Increased the file size limit of OneDrive external storage to upload attachments.
        -   Updated the Conflict of Interest and Stock Preclearance legal request types so that, when the requests are closed, the Closed by field is filled with a user ID as follows:
            -   Approver's ID when the legal request is approved or rejected.
            -   Legal fulfiller's ID when the legal request is canceled by the fulfiller.
            -   Practice area lead's ID when the legal request is auto-approved.
        -   Updated conditions to include Universal Request-related exceptions when sending email notifications to requesters.
        -   Updated the email notification to send it to both the previous and new assignees on a legal request when the Assigned to field is updated with a new user.
-   **Version 5.0.5 - May 2022**
    -   New:
        -   Added a new 'Practice area leads' related list in the Practice Area form to add or remove practice area leads for a legal request.
        -   Assignment group change in a legal request:
            -   Added the option to change the assignment group in a legal request.
            -   Added a new option called 'Editable Assignment group in Request' in the Options of the Intake Form.
        -   Collaborating on a legal request:
            -   Added a new field 'Collaborator' in the Legal Request form's Details tab to enable the legal fulfiller to add more users to collaborate on the legal request. The collaborators will have full access to the request as the legal fulfiller except for changing assignment group, assignment group permission, and assigned user.
            -   Added a new module called 'Collaborations' under Legal Requests, which displays a list of all legal requests in which the logged-in user is added as a collaborator.
            -   Added a new email notification that will be sent to a user who has been added as a collaborator in a legal request.
        -   External storage for attachments in a legal request:

            -   Added a new option called 'Enable External Storage for attachment' in the Options of the Intake Form.
            -   Added a new 'Documents' tab in the Legal Request form to enable adding and deleting documents to a legal request, requesting access for users.
            -   Added a new 'Document Access' tab in the Legal Request form that is visible to the assigned user, practice area lead, and group manager. The fulfiller can revoke access for any user.
            -   Added a scheduled job that syncs permissions for users to allow them access to documents of a legal request saved in external storage folders.
            -   Added a scheduled job for admins to upload failed documents again after fixing any issues.
            -   Added option to request ad hoc approval for a document.
    -   Changed:
        -   Updated legal request email notifications to include in the CC field, the collaborators added to a legal request.
        -   Updated the Standard Ticket page to show the collaborator-related changes in the legal request in the Activity stream.
        -   Updated granular delegation functionality to meet the user criteria of the delegation rule while adding duties for a delegate.
        -   Removed: Removed the Practice area lead field from the Practice Area form.
-   **Version 4.2.2 - February 2022**
    -   New:
        -   Legal Executive dashboard, which is installed via Performance Analytics Content Pack for Legal Service Delivery app, enables general counsel and practice area leads to get insight, analyze trends, and drill down into the details of legal requests.
        -   Delegation of legal duties relating to legal requests, legal matters, legal matter tasks, and approvals to another user by legal fulfillers during period of absence.
        -   Granular delegation to choose specific services for the delegation. This needs instalallation and setting the Granular Delegation app.
    -   Changed:
        -   Legal: Request Management has been renamed Legal Request Management
        -   Legal Dashboard module in the Application Navigator is renamed Legal Dashboards if you install the Performance Analytics Content Pack for Legal Service Delivery app.
    -   Removed: Remove the assignment\_group column from Practice Area table
-   **Version 4.1.9 - December 2021**
    -   New:
        -   Added new email notifications for various legal request actions
        -   Added the following new practice area tables that extend the Legal Request table:
            -   Crime \[sn\_lg\_ops\_crime\]: Crime practice area related to financial crimes like sanctions, bribery, fraud, etc.
            -   Real Estate \[sn\_lg\_ops\_real\_estate\]: Real Estate practice related to commercial real estates, contracts, etc.
            -   Health, Safety and Environment \[sn\_lg\_ops\_health\_safety\_and\_environment\]: Health, Safety and Environment practice related to occupational health and safety.
        -   Added the Assignment group permission field to set permissions for assignment group members to read, write, or have no access to a legal request.
        -   Added the Approvals tab in the Standard Ticket page, enabling requesters to see the approvals associated with their legal requests. View the relevant information in Employee Center under My To-Do's to make an approval decision​.
        -   Added the Legal Disposition \[sn\_lg\_ops\_legal\_disposition\] table to store dispositions for a legal request and can be added to the Legal Request form as a related list.
        -   Added the Active check box in the Subcategory form.
        -   Enabled approvals related to legal requests and their attachments on the Employee Center portal.
        -   Configure multiple electronic signature and external storage providers and use them based on different conditions.
    -   Changed:
        -   Legal integrations to add external storage and electronic signature providers has been updated to support multiple electronic signature and external storage providers at the same time.
        -   The external storage workflow for storing legal documents have been renamed and updated:
            -   Legal External Storage Core - Box
            -   Legal External Storage Core - Google Drive
            -   Legal External Storage Core - OneDrive
        -   Updated external storage subflows to be used with any other flows to store any legal documents in an external storage system.
        -   The core electronic signature workflows for e-signing of legal documents have been renamed and updated:
            -   Electronic Signature Core - DocuSign
            -   Electronic Signature Core – AdobeSign
        -   The core electronic signature workflows for e-signing of Non-disclosure Agreement \(NDA\) documents have been renamed and updated:
            -   NDA Signature Flows
            -   NDA Electronic Signature \(Dynamic Flow\)
            -   NDA Electronic Signature - DocuSign
            -   NDA Electronic Signature - AdobeSign
    -   Removed:
        -   Removed the Edit button in the Subcategories related list on the Intake Form.
        -   All existing electronic signature and external storage workflows have been removed and replaced with the new modular workflows.
        -   The Legal External Apps \[sn\_lg\_ops\_external\_configuration\] table has been deprecated to replace the new tables for Legal Integration - External Storage \[sn\_lg\_ops\_integration\_external\_storage\] and Electronic Signature \[sn\_lg\_ops\_integration\_esignature\]. These tables extend the Legal Integration \[sn\_lg\_ops\_integration\_core\] table.
    -   Fixed: Fixed an issue where the legal requests created on behalf of the logged-in user were not showing up in the Self Service &gt; My Requests list.
-   **Version 4.0.6 - September 2021**
    -   New:
        -   Request legal services related to digital forensics from Employee Center portal.
        -   Requesters can reopen a request if they re not satisfied with the resolution given by the legal team.
        -   The Legal Matters tab on the Standard Ticket page added to view legal matters associated with a legal request.
        -   Ability to send and receive emails while working on legal requests from within the Legal Counsel Center.
        -   Predefined options for configuring the intake forms, such as reopening a legal request or a legal matter, ad hoc approvals. These predefined options enable you to change the default behavior of legal requests and legal matters based on your business needs.
    -   Changed:
        -   Attachments in a legal request cannot be removed until they have an ad hoc approval record in the Requested state. To remove such attachments, either cancel the ad hoc approval request or obtain the approval first.
        -   When you remove an attachment associated with a legal request, it also deletes the associated ad hoc approval records.
    -   Removed: The **Condition** field has been removed from the External Apps Configuration form.
-   **Version 3.6.2 - June 2021**
    -   New:
        -   Adhoc approval for a legal request or its attachments from a user or a user group
        -   Email notifications enabled for all the practice area tables for legal requests
-   **Version 3.5.4 - April 2021**
    -   New:
        -   On cancellation of a legal request, the associated Flow Designer flow is aborted and any pending approvals for the request are cancelled.
        -   Accessibility improvements made for widgets used in Request and Matter in the Legal Service Portal, and they are now WCAG2.1 AA compliant.
        -   An email notification is sent to the requester and users in the Watchlist when a comment is posted in a legal request.
    -   Fixed: The issue with the Short Description field on the Legal Request form not being editable.
-   **Version 3.4.2 - March 2021**
    -   New:
        -   Configurable intake forms for different types of legal requests
        -   Automated routing based on defined rules and SLA's
        -   Legal Knowledge Base
        -   Reports and dashboards
        -   Plug-in support with Employee Service Center

