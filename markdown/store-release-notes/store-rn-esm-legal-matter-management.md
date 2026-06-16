---
title: Legal Matter Management release notes
description: Version history for the Legal Matter Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-esm-legal-matter-management.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 9
breadcrumb: [ServiceNow Store - Legal Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Legal Matter Management release notes

Version history for the Legal Matter Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.1.4 - June 2026**
    -   Changed: Security enhancements
    -   Fixed:
        -   Matter artifact document approval information is now correctly displayed in the Employee Center My Tasks page.
        -   Performance improvements made on 'Legal Matter Tasks' list view on Legal Counsel Center.
-   **Version 10.0.1 - March 2026**

    New: Attorney Client Privilege enables legal matter owner to designate legal matters as privileged and confidential. Attorney Client Privilege restricts access to authorized stakeholders, marks communications with confidentiality banners, and maintains a document audit trail to help you protect sensitive legal communications.

-   **Version 9.2.4 - January 2026**

    Fixed: Resolved RCA issues.

-   **Version 9.2.2 - December 2025**
    -   Changed: Security enhancements.
    -   Fixed:
        -   The “Interview details” section no longer appears on legal matter tasks when the type is set to “Data collection.”
        -   The “Delete the attachment” messages do not appear unnecessarily in the activity stream for legal hold matters when the assignment group permissions are changed to read access.
        -   Coding errors in the LegalEventSecurityUtilsBase script include have been corrected, ensuring proper milestone association in Legal Matter Management.
        -   The email template now populates correctly in the right pane for legal matters, allowing users to view and copy template contents as expected.
        -   The "Re-trigger external integration" action is now accessible to users with the legal fulfiller role.
        -   Outside counsel request submission related issue has been fixed.
-   **Version 9.1.0 - September 2025**
    -   Changed: Additional ACLs have been applied to the sn\_lg\_matter\_m2m\_request\_matter and sn\_lg\_matter\_m2m\_matter\_task\_artifact\_list tables.
    -   Fixed: The issue related to restricted controlled access in the Legal Schedule has been resolved.
-   **Version 9.0.1 - August 2025**

    New: Introduced support for Legal Hold workflow \(new legal practice app\).

-   **Version 8.9.3 - July 2025**
    -   Fixed:
        -   ACL issues
        -   Issue that caused a query range error to appear when navigating away from Matters - Unassigned, Matters - All, Matter tasks - All, and Artifacts - All list in the Legal Counsel Center after running the Writer audit script
-   **Version 8.9.1 - May 2025**
    -   New: When an external matter is closed or reopened in Legal Tracker, the corresponding legal matter status is updated in Legal Matter Management. The change in the state is recorded in the Activity stream.
    -   Changed: Improved Subpoena icon for improved space utilization in the intake form.
    -   Fixed: When you close a legal matter after editing the short description, the changes are not saved. This has been fixed.
-   **Version 8.7.0 - February 2025**

    Fixed: Edits made to a matter were not saved when "Close Complete" was selected without saving the matter. This has been fixed.

-   **Version 8.5.0 - November 2024**

    Fixed: The View Legal Matter button in email notifications now opens the matter in the next experience Legal Counsel Center. Previously, it was routing the users to Legal Service Portal.

-   **Version 8.4.1 - August 2024**
    -   Changed: The default matter templates were updated to remove the workflow column. You are advised to review matter templates and ensure that these workflows or any of the custom ones that you have created are removed.
    -   Fixed:
        -   Collaborators were not able to attach documents to matter artifacts.
        -   Variable section not displayed for Digital forensics, Matters and Sales request
    -   Removed:
        -   The default matter template was updated to remove the following workflows:
            -   Legal Privacy Matter for Privacy Review Questionnaire
            -   Legal Matter for Subpoena
-   **Version 8.3.1 - May 2024**
    -   Fixed:
        -   Involved party field was not displayed on Legal Matter Task form.
        -   Integration with Legal Tracker functionality wasn't working for matters belonging to Privacy Assessment requests.
        -   The Variables section for Subpoena &amp; Digital Forensics related matters was not displayed in Legal Counsel Center.
        -   Comments added while cancelling a legal matter task were not captured in the activity stream.
        -   Security fixes.
-   **Version 8.1.5 - January 2024**

    Security fixes.

-   **Version 8.1.4 - November 2023**
    -   New:
        -   Integration with Legal Tracker for engagement with outside counsels and to track spend.
        -   The legal matter form now supports Outside Counsels and External Matters' related lists, which enable the legal fulfillers to submit outside counsel engagements for Invention Disclosure and Legal Tracker integration and to view external matter details and track spends. These related lists will be displayed when you have enabled Invention Disclosure or Legal Tracker integration related features.
    -   Fixed:
        -   Added access controls to restrict access for legal fulfillers to approve records for legal requests.
        -   The attachment errors when opening an artifact from the ethics matter are fixed.
        -   The Involved Party field is visible on the Matter Task form.
-   **Version 8.0.8 - September 2023**

    Fixed: Matter admin privileges modified to see all necessary data in Counsel Center.

-   **Version 8.0.2 - August 2023**

    New: Configure iManage as an external storage system integration to store documents attached to legal requests and matters.

-   **Version 7.0.1 - February 2023**

    Changed: Made Investigations workflow changes.

-   **Version 6.2.7 - January 2023**

    Changed: Updated permissions for users with the report\_viewer role to view a few reports in the Legal Executive dashboard and Legal Counsel Center landing page.

-   **Version 6.2.4 - November 2022**
    -   New:
        -   Added a new email notification to be sent to the matter owners when they no longer own the assigned matter.
        -   Added Task Configurations based on the new Approval Hub in the Employee Center to include approvals for legal matters, legal matter tasks, artifacts, and legal matter templates.
        -   Added the View record button on the legal matter approval page in the Standard Ticket page to open the legal matter record for reference before approving or rejecting it.
        -   Added the Microsoft SharePoint external storage option to store documents in the legal matter artifacts when enabled.
    -   Changed:
        -   The Request Details section on the Ethics Matter form is not available when an ethics complaint legal matter is attached as a primary ticket to Universal Request.
        -   Updated the legal\_matter\_config role to allow managing matter templates and document templates.
-   **Version 6.1.1 - August 2022**
    -   New:
        -   External storage for attachments in a legal matter
            -   Added a new option called "Enable External Storage for attachment" in the Options of the Intake Form with matter type selected.
            -   Added a new tab "Documents" in the Artifacts form to enable adding and deleting documents to a legal matter artifact, requesting access for users.
            -   Added a new tab "Document Access" in the Legal Matter form that is visible to users with the matter\_admin role.
            -   Added the option to request ad hoc approval for a document.
        -   Changed:
            -   When a legal matter is created from a legal request, all attachments in the legal request are copied to the legal matter under a new Artifacts record and shown in the Documents tab.
            -   The External Storage tab has been renamed to External Links in the Artifacts form.
            -   When an existing matter template is updated, any intake forms associated with that matter template are automatically updated to the latest published version.
-   **Version 5.0.5 - May 2022**
    -   New:
        -   Added a new related list 'Practice area leads' in the Practice Area form to add or remove practice area leads for a legal matter.
        -   Added a new related list 'Approver Groups' in the Matter Template form to add or remove user groups to approve legal matter templates.
        -   Assignment group change for a legal matter
            -   Added the option to change the assignment group in a legal matter.
            -   Added a new option called 'Editable Assignment group in Matter' in the Options of the Intake Form.
        -   Collaborator in a legal matter
            -   Added a new field 'Collaborator' in the Legal Matter form's Details tab to enable the matter owner to add more users to collaborate on the legal matter. The collaborators will have full access to the matter as the matter owner except for changing assignment group, assignment group permission, and assigned user.
            -   Added a new module called 'Collaborations' under Legal Matters, which displays a list of all legal matters in which the logged-in user is added as a collaborator.
        -   Added a new email notification that will be sent to a user who has been added as a collaborator in a legal matter.
    -   Removed:
        -   Removed the 'Additional collaborators' field from the Legal Matter form's Details tab. Additional collaborators in existing legal matters will show in the 'Watch list' field.
        -   Removed the 'Approver group' field from the Matter Template form.
-   **Version 4.2.1 - February 2022**
    -   New: Get insight, analyze trends, and drill down into the details of legal matters from the new Legal Executive dashboard, that is installed via Performance Analytics Content Pack for Legal Service Delivery app.
    -   Changed: Legal: Matter Management has been renamed Legal Matter Management
-   **Version 4.1.4 - December 2021**
    -   New:
        -   Added new email notifications for various legal matter actions
        -   Added the following new practice area tables that extends Legal Matter table:
            -   Crime \[sn\_lg\_matter\_crime\]: Crime practice area related to financial crimes like sanctions, bribery, fraud, etc.
            -   Real Estate \[sn\_lg\_matter\_real\_estate\]: Real Estate practice related to commercial real estates, contracts, etc.
            -   Health, Safety and Environment \[sn\_lg\_matter\_health\_safety\_and\_environment\]: Health, Safety and Environment practice related to occupational health and safety.
        -   Added the Legal Disposition \[sn\_lg\_ops\_legal\_disposition\] table to store dispositions from a legal matter and can be added to the Legal Matter form as a related list.
        -   Enabled approvals related to legal matter and their artifacts on the Employee Center portal.
    -   Fixed:
        -   Fixed an issue where the email notification for a new legal matter was sent to the user who submitted the legal request instead of the request fulfiller who created the legal matter.
        -   Fixed the error that appeared while adding a new checklist item in the Legal Matter Task tab.
-   **Version 4.0.4 - September 2021**
    -   New:
        -   Added the Assignment group permission field to set permissions for members of the assignment group to read, write, or have no access to a legal matter.
        -   Send and receive emails from the Legal Matter and Legal Matter Task form.
    -   Changed:
        -   Attachments in a legal matter or artifact cannot be removed until they have an ad hoc approval record in the Requested state. To remove such attachments, either cancel the ad hoc approval request or obtain the approval first.
        -   When you remove an attachment associated with a legal matter or artifact, it also deletes the associated ad hoc approval records.
-   **Version 3.6.1 - June 2021**
    -   New:
        -   Adhoc approval for a legal matter or its artifacts from a user or a user group
        -   Email notifications enabled for all the practice area tables for legal matters
-   **Version 3.5.3 - April 2021**
    -   Changed:
        -   Look-up fields for legal matters, phases, and tasks now show their Name instead of Number.
        -   URL field on the Artifacts &gt; External Storage form is changed to a text field.
    -   Fixed: Email notification for Approve/Reject of a legal matter task.
-   **Version 3.4.0 - March 2021**
    -   New:
        -   Lawyer-client confidentiality– The legal staff can keep internal legal notes separate from the underlying legal request.
        -   Matter artifacts– A means to organize legal documents, similar to folders.
        -   Matter templates– A means to codify standard operating procedures with the themed Legal task lists by practice area and matter type.
        -   Matter task management– Manage legal matter tasks, even those which the non-legal staff would work on.
        -   Milestones– Track important legal dates.

**Parent Topic:**[ServiceNow Store - Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-esm-legal-service-delivery.md)

