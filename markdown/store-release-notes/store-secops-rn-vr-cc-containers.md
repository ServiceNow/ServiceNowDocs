---
title: Vulnerability Response and Configuration Compliance for Containers release notes
description: Version history for the Vulnerability Response and Configuration Compliance for Containers application on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-cc-containers.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 15
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response and Configuration Compliance for Containers release notes

Version history for the Vulnerability Response and Configuration Compliance for Containers application on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.4.2 - June 2026 \(USEM\)**
    -   New: A link lets you navigate from the Wiz configuration module directly to the Configure VI Granularity module where you can configure the keys that generate Container Vulnerability Response findings.
    -   Changed: Enhancements and changes to support internal security directives for container vulnerability and configuration data.
    -   Fixed:
        -   Container vulnerable items \(CVITs\) ingested through the Wiz Container Vulnerability integration now show a valid vulnerability reference instead of appearing blank.
        -   Palo Alto Prisma Cloud Compute full-pull ingestion now replaces the host list on Discovered Container records instead of appending to it, so undeployed hosts no longer linger on images.
-   **Version 2.19.3 - June 2026**
    -   New: A link lets you navigate from the Wiz configuration module directly to the Configure VI Granularity module where you can configure the keys that generate Container Vulnerability Response findings.
    -   Changed: Enhancements and changes to support internal security directives for container vulnerability and configuration data.
    -   Fixed:
        -   Container vulnerable items \(CVITs\) ingested through the Wiz Container Vulnerability integration now show a valid vulnerability reference instead of appearing blank.
        -   Palo Alto Prisma Cloud Compute full-pull ingestion now replaces the host list on Discovered Container records instead of appending to it, so undeployed hosts no longer linger on images.
-   **Version 30.3.2 - April 2026 \(USEM\)**
    -   New: Added support for AWS ECS clusters and services in the container vulnerability integration. The integration now builds a unified relationship and hierarchy model for ECS assets — alongside existing Kubernetes support — to enable CVIT ingestion, service scoring, and impact analysis across both Discovery and Scanner data sources.
    -   Changed:
        -   The length of the source\_id column on the Container Image Finding \[sn\_vul\_container\_image\_findings\] table has been increased to accommodate longer AWS source identifiers.
        -   Deployment hierarchy data for both ECS and EKS is now precomputed and stored in a cache table, reducing redundant computation during import. ECS support is supported starting with this release. EKS support was already available and now benefits from the same optimized caching model.
    -   Fixed:
        -   The Short Description, Assignment Group, and Assigned to fields now autopopulate when creating a change from a Container Vulnerable Item \(CVUL\) in the Vulnerability Manager workspace.
        -   The Split Task UI action for Container Remediation Tasks \(CVUL\). Previously, splitting a remediation task left the Assignment Group and Assigned To fields empty on the newly created task
        -   The IsBaseImage flag has been deprecated on Container Vulnerable Items \(CVITs\) as it is image-specific data. It is now correctly mapped on the Discovered Container Image \[sn\_vul\_container\_image\] table, where it is imported from the Prisma Base Image integration payload.
        -   The Path field on Container Image Package records now matches the path on the related Container Image Finding record for Prisma and other third-party scanners
        -   The Impacted Services related list is now available on Container Vulnerable Item records, which is consistent with the related list that exists on Vulnerable Item records.
        -   A security vulnerability in the ContainerVulnerabilityAJAX script include where ACL checks were not enforced, allowing any authenticated user to invoke functions above their privilege level. Execute ACLs and role checks have been added to restrict access to authorized roles only.
        -   An integration run queued in the Ready state is now automatically triggered after the preceding integration run completes successfully. Previously, the PostIntegrationProcessor script include used setWorkflow\(false\) when closing a run, which prevented the workflow from picking up the next queued run — leaving it stuck indefinitely in the Ready state.
-   **Version 2.18.3 - April 2026**
    -   New: Added support for AWS ECS clusters and services in the container vulnerability integration. The integration now builds a unified relationship and hierarchy model for ECS assets — alongside existing Kubernetes support — to enable CVIT ingestion, service scoring, and impact analysis across both Discovery and Scanner data sources.
    -   Changed:
        -   The length of the source\_id column on the Container Image Finding \[sn\_vul\_container\_image\_findings\] table has been increased to accommodate longer AWS source identifiers.
        -   Deployment hierarchy data for both ECS and EKS is now precomputed and stored in a cache table, reducing redundant computation during import. ECS support is supported starting with this release. EKS support was already available and now benefits from the same optimized caching model.
    -   Fixed:
        -   The Short Description, Assignment Group, and Assigned to fields now autopopulate when creating a change from a Container Vulnerable Item \(CVUL\) in the Vulnerability Manager workspace.
        -   The Split Task UI action for Container Remediation Tasks \(CVUL\). Previously, splitting a remediation task left the Assignment Group and Assigned To fields empty on the newly created task
        -   The IsBaseImage flag has been deprecated on Container Vulnerable Items \(CVITs\) as it is image-specific data. It is now correctly mapped on the Discovered Container Image \[sn\_vul\_container\_image\] table, where it is imported from the Prisma Base Image integration payload.
        -   The Path field on Container Image Package records now matches the path on the related Container Image Finding record for Prisma and other third-party scanners
        -   The Impacted Services related list is now available on Container Vulnerable Item records, which is consistent with the related list that exists on Vulnerable Item records.
        -   A security vulnerability in the ContainerVulnerabilityAJAX script include where ACL checks were not enforced, allowing any authenticated user to invoke functions above their privilege level. Execute ACLs and role checks have been added to restrict access to authorized roles only.
        -   An integration run queued in the Ready state is now automatically triggered after the preceding integration run completes successfully. Previously, the PostIntegrationProcessor script include used setWorkflow\(false\) when closing a run, which prevented the workflow from picking up the next queued run — leaving it stuck indefinitely in the Ready state.
-   **Version 2.17.2 - January 2026**
    -   Changed:
        -   The image repository name format for new and existing discovered container images has been updated to align with the discovery format. The supported format is registry/repository. A separate finding is created for a repository present in each registry.
        -   Appended all repositories that are associated with an image to the Repository field on the discovered container image records.
-   **Version 30.2.4 - January 2026 \(USEM\)**
    -   Changed:
        -   The image repository name format for new and existing discovered container images has been updated to align with the discovery format. The supported format is registry/repository. A separate finding is created for a repository present in each registry.
        -   Appended all repositories that are associated with an image to the Repository field on the discovered container image records.
-   **Version 2.16.1 - December 2025**
    -   New: Add "Fix available" column to the Container Vulnerable Items \[sn\_vul\_container\_image\_vulnerable\_item\] table.
    -   Fixed:
        -   Resolved a state transition issue that blocked CVITs from moving from “Closed–False Positive” to "Closed–Fixed" status.
        -   Fixed the VIT state logic so that when previously resolved vulnerabilities resurface, these detections automatically transition from closed to open, enabling accurate monitoring of recurring security issues.
        -   Fixed a UI issue where theFalse Positive andRequest Exception buttons were not working for CVITs and CVULs. Updated validation now correctly supports empty Integration fields and handles missing keys in \`sn\_vul\_container\_image\_vulnerability\_keys\`.
        -   Addressed a date synchronization problem affecting Container Vulnerability Item Tasks \(CVITs\). The roll-up logic has been revised so that “first found” now reflects the earliest occurrence and “last found” reflects the most recent, improving accuracy in vulnerability tracking and reporting.
-   **Version 2.14.5 - September 2025**
    -   Fixed: Improved state management: The state management system for vulnerable items has been improved to handle cases where these items are in the 'In Review' state and their associated remediation task is deleted.
    -   Changed:
        -   Streamlined CVIT status transitions: The transition from "Closed FP" to "Closed Fixed" is now enabled for container vulnerable items \(CVITs\). This change aligns with recent updates in the Vulnerability Response \(VR\) and Configuration Compliance \(CC\) modules, ensuring consistency across the system.
        -   Enhanced change request creation: When a change request is created from a remediation task, the task's details are now accurately copied to the corresponding fields in the Change Request. Specifically, the Short Description and full Description from the remediation task are preserved in the Change Request, maintaining complete context and reducing manual effort.
-   **Version 2.14.4 - August 2025**
    -   New: Enhancements support more scanner data on imports. Namespaces and hierarchy cluster are considered and populated in the discovered container image \[sn\_vul\_container\_image\] table if this data is imported.
    -   Changed:
        -   With improvements to refine state management logic, you might see overall improvements in the following areas:
            -   State roll-down from remediation tasks \(RTs\) to findings and roll-up from findings to RTs for all modules.
            -   Handling of mixed states such as 'Deferred' and 'Closed'.
            -   Closing RTs in sub-states such as 'In-Review'.
            -   Reopening RTs based on the 'Assigned To' field.
            -   Aligning false positive transitions with scanner results as the source of truth to help reduce manual effort and clarify task ownership.
    -   Fixed:
        -   State changes in vulnerability findings are rolled up correctly to their associated container vulnerable items.
        -   A cross-scope access error that was triggered when reopening closed container vulnerable items.
        -   An issue that prevented saving images with the same name but different IDs.
-   **Version 2.13.5 - June 2025**

    Fixed: Exception rules are automatically approved when they are created by users with granular roles.

-   **Version 2.13.3 - May 2025**
    -   Changed:
        -   The most current scanner metadata for Cloud Account ID, Kubernetes Namespace, and Cluster Name is included from the last integration run. This metadata is visible on the Discovered Container Image record and helps you identify and track ownership across your container environments.
        -   Enhancements to the Vulnerability Manager and IT Remediation workspaces:
            -   The Unassign workflow is supported for container vulnerable items \(CVITs\) and remediation tasks. Streamline vulnerability assignments in the workspaces with the Unassign UI action from the more actions menu on a CVIT.
            -   Reassign incorrectly assigned CVITs, clarify ownership for reassessment, and maintain accurate triage records in workspace views.
    -   Fixed:
        -   Exception rule handling for CVR to ensure container remediation tasks remain closed and CVITs remain unlinked from container remediation tasks after an exception rule expires.
        -   State roll up from CVITs to container remediation tasks to ensure that a remediation task transitions to Deferred if all of its associated vulnerable items are in the Deferred state.
        -   Missing registry values in CVITs by ensuring registry information is set when CVITs are created for the Prisma Cloud Compute Registry Integration.
        -   Navigation panel so that Auto-close Rules is displayed under the Administration section.
        -   VCA records for CVITs so the Details, Approval Name, Desired Value, and Current fields are populated during exception requests.
-   **Version 2.12.3 - March 2025**
    -   Fixed:
        -   An issue with requesting extensions for exception rules in version 2.12.2.
        -   Resolution notes are added to the Work notes section of a container vulnerable item \(CVIT\) record when it moves to the Resolved state.
-   **Version 3.1.3 - February 2025**
    -   Changed:
        -   Registry can now be added as a CVIT granular key.
        -   The CVIT granularity configuration includes two options \(Scanner or Discovery Information\) to allow selection of granularity based on scanner or discovery data, depending on whether the ITOM plugin is installed.
        -   Added path as a unique key for findings key. This means, a package can be present in multiple locations leading to multiple findings
        -   Populate Cloud Resource Type in Discovered Items upon executing Prisma Host Integration
-   **Version 2.11.4 - December 2024**
    -   Changed: When you select the Request Extension button to extend an exception rule, you have the option to extend both the deferred until date' and the exception rule valid to' date.
    -   Fixed:
        -   If a remediation owner selects the Resolve button, then the Resolve pop-up window gets displayed as expected.
        -   Tags added to the container vulnerable item are displayed in the workspace list view if a tag is associated with it, and the Tags column is included in the list view.
-   **Version 2.11.3 - November 2024**
    -   New:
        -   Workspace search: Efficiently search using the record numbers and open the records in either the Vulnerability Manager Workspace or the IT Remediation Workspace, depending on your assigned role.
        -   Navigating to Workspaces from the All menu: If the 'sn\_vul\_cmn\_ws.navigate\_to\_workspace' system property is enabled, selecting predefined filter links in the Container Vulnerability Response module from the 'All' menu will automatically open these links in the Vulnerability Manager Workspace and IT Remediation Workspace based on your roles.
        -   Granular Role-based access control:Enhanced the role management in Vulnerability Manager Workspace \(for watch topics and lists\) and IT Remediation Workspace \(for lists\). This allows precise access control and configuration tailored to specific user roles.
        -   Customizable Age calculation: The Age and Age Closed calculations for a container vulnerable item can now be customised so that they are calculated from a choice of available date fields. That is, you can now select any of the available date fields such as last found, created, etc. with reference to which the Age and Age Closed must be calculated. For more information on how to configure these age calculations, refer to the KB1703270 KB article.
        -   Refresh the Saved Filter visualizations:You can now refresh the visualizations for saved filters on the Vulnerability Manager Workspace Home page either once or daily. Additionally, you can manually update these visualizations on demand to reflect the latest data.
        -   Performance improvement in Workspaces: The glide.ui.list.seismic.omit.count' system property allows you to deactivate the record/row count display on the lists in the Vulnerability Manager Workspace and IT Remediation Workspace, optimizing performance for large datasets.
        -   You can now re-evaluate the exception rules for a set of selected container vulnerable items directly in the Vulnerability Manager Workspace instead of re-evaluating these rules for all records in the classic UI.
        -   Properties module: A new Properties module has been added to the navigation menu under the Administration section. This module enables direct modification of the flag values, offering a user-friendly method to manage and update system properties directly from the interface.
        -   Vulnerability Response Prisma Registry integration:Now you can ingest the static image findings obtained from the Prisma registry scan into the ServiceNow Container Vulnerability Response
        -   Ability to define auto-close rules with advanced conditions to automatically close older or stale container vulnerability items \(CVITs\) based on defined filter criteria on container vulnerabilities.
-   **Version 2.10.4 - September 2024**

    Changed: When you add path as granularity for findings in the integration instance parameter, the system includes path as one of the unique keys while creating the findings.

-   **Version 2.10.3 - August 2024**
    -   New:
        -   When vulnerable items are imported, they can be added to remediation tasks based on the configured remediation task rules.
        -   Starting with v23.0 of Vulnerability Response and 2.10 of Vulnerability Response and Configuration Compliance for Containers, you can evaluate assignments, remediation target dates, remediation tasks, and risk scores for container vulnerable items directly from the Vulnerability Manager Workspace. You don't need to evaluate these properties for all the records.
    -   Changed:
    -   -   Auditing is disabled on State updated on, Deferral notes, Resolution date, Integration, Integration Instance, Remediation effort, In remediation effort.
-   The Rollup container vulnerable item values to vulnerability and group schedule job is improved to create background jobs with multithreading capabilities. This enhancement enables processing of multiple records simultaneously, thus significantly speeding up the overall task.
    -   Fixed: The My approval module now shows approval requests for extension of exception rules.
-   **Version 2.6.9 - June 2024**
    -   Fixed:
        -   The count of container vulnerable items are now accurately aggregated to the corresponding vulnerabilities.
        -   Issues with the UI of the Create Change Request modal window.
-   **Version 2.6.5 - May 2024**

    New: The Vulnerability Manager workspace list view now includes a bulk edit option for container vulnerable items. This allows for simultaneous updates to the state, assignment group, and exception request of multiple items.

-   **Version 2.5.3 - February 2024**
    -   Changed: Auto-close feature closes the container-vulnerable items \(CVITs\) based on the last found date of the vulnerable time \(VIT\) instead of the last scan date of the discovered image.
    -   Fixed: Docker Image mapping issue is fixed with the Prisma Image base integration.
-   **Version 2.3.3 - December 2023**

    Fixed: When an exception rule is cancelled, the VIT state changes to the Open state.

-   **Version 2.3.2 - November 2023**
    -   New:
        -   Users can now request extension for a deferred Remediation Task or Vulnerable Item or Exception Rule by clicking the Request Extension button.
        -   Added a new field, image\_digest to include the complete SHA ID3.
    -   Changed: Changed the image ID to the first 12 characters of the SHA2 which is sent to IRE.
-   **Version 2.2.3 - August 2023 \(Vancouver\)**
    -   New:
        -   Governance Risk and Compliance \(GRC\) Exception Management support is provided for Container Vulnerability Response in the workspace.
        -   Added registry, repo, and tag information in the Discovered container image.
    -   Changed: The Container Vulnerability Management overview dashboard is now available in the Next Experience UI.
-   **Version 2.1.2 - May 2023**
    -   New:
        -   Remediation status will be evaluated when the container vulnerable item \(CVIT\) is closed.
        -   Integration processes were timing out after one hour, even if the import queue entry was still being processed. As a result, the integration run status was being updated as 'Error'. Starting from V2.1.0, timestamps \(heartbeats\) are sent periodically to indicate that the queue is alive and processing valid data.
-   **Version 2.0.6 - March 2023**
    -   Fixed:
        -   The container admin can now see the container related libraries in the workspace list view.
        -   The Unassign button for containers is now working as expected.
-   **Version 2.0.4 - February 2023**
    -   New:
        -   Added support for workspace for Vulnerability Response and Configuration Compliance for Containers application.
        -   Deferred until date oncontainer vulnerable items \(CVITs\)will persist and not be cleared unless it is manually reopened.
        -   For manual exceptions, if a deferred CVIT is reopened within the deferral window, it will be automatically deferred.
        -   Manage vulnerability exception requests for CVITs using either Vulnerability Response or GRC: Policy and Compliance Management integration.
-   **Version 1.2.2 - November 2022**
    -   New: Unassign approval workflow for Container Vulnerable Items.
    -   Fixed:
        -   Populate resolution date on container vulnerability item \(CVIT\) when moved to Resolved state and clear it when re-opened.
        -   Container remediation attributes on Vulnerability entry table are now moved from Vulnerability Response to Container Vulnerability Response scope.
        -   Fixed the ability to cancel integration run.
-   **Version 1.0.6 - May 2022**
    -   Fixed: Fixed an issue of container vulnerable item \(CVIT\) reopening when marked as Closed-False Positive.
    -   Changed: Updated the unique index on Discovered Container Images table to include "Integration instance" attribute.
-   **Version 1.0.5 - March 2022**

    Vulnerability Response and Configuration Compliance for Containers helps organizations respond to container vulnerabilities quickly and efficiently by connecting security and application teams, and providing real-time visibility into your security posture. Container Vulnerability Response connects the workflow and automation capabilities of the ServiceNow AI Platform® with vulnerability scan data from leading container security vendors to give your teams a single platform for a response that can be shared between security and application teams.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

