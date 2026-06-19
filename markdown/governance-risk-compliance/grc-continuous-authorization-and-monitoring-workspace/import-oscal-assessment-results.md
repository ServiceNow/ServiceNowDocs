---
title: Import OSCAL Assessment Results \(AR\)
description: Import an OSCAL Assessment Results \(AR\) package from another instance or external tool to create an engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-assessment-results.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 4
breadcrumb: [Import in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL Assessment Results \(AR\)

Import an OSCAL Assessment Results \(AR\) package from another instance or external tool to create an engagement.

## Before you begin

-   Catalog JSON file
-   Profile JSON file
-   SSP JSON file
-   Overlay JSON file \(optional\)
-   Assessment Plan \(AP\) JSON file
-   Assessment Results \(AR\) JSON file
-   POA&amp;M JSON file \(optional\)

Role required:

-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)
-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)

**Note:** Only JSON files in valid OSCAL format are supported. The AR cannot be imported as a standalone file. It must always be imported together with the SSP and its associated files.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the\[Omitted image "cam-oscal-import-icon.png"\] Alt text: OSCAL import icon.

3.  Select **New Import** from the **All OSCAL imports** landing page.

4.  In the **Details** section, complete the fields and select **Next**.

    |Field|Description|
    |-----|-----------|
    |OSCAL model|Select AR.|
    |Source|Enter a name to identify this import.|
    |Import status recipients|\(Optional\) Select users to notify when the import completes.|

5.  In the **Attachments** section, upload the required files in each section and select **Next** after completing each section.

    The following sections appear in order. Mandatory sections are marked with an asterisk \(\*\).

<table id="table_attachments_sections"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provide the attachments \*

</td><td>

Upload the mandatory files: -   Catalog — Catalog JSON file
-   Profile — Profile JSON file
-   SSP — SSP JSON file
 You can also optionally attach boundary, data flow, network, and enterprise architecture diagrams.

</td></tr><tr><td>

Overlay attachments

</td><td>

Upload an overlay JSON file if applicable. This section is optional.

</td></tr><tr><td>

Assessment plan attachments \*

</td><td>

Upload the AP JSON file linked to the AR that you are importing. The maximum file size is 1024 MB.

</td></tr><tr><td>

Assessment results attachments \*

</td><td>

Upload the AR JSON file. The maximum file size is 1024 MB.

</td></tr><tr><td>

POA&amp;M attachments

</td><td>

Upload a POA&amp;M JSON file if applicable. This section is optional. If provided, POA&amp;M items from this file are aggregated with the POA&amp;M items already present in the AR file.

</td></tr></tbody>
</table>6.  In the **User and Group Mapping** step, review the user and group mappings and update them if needed, then select **Next**.

    This step contains three sections completed in sequence: User mapping, Group mapping, and Roles and responsibility.

<table id="table_user_group_mapping_sections"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User mapping

</td><td>

Map the users listed in the OSCAL file to the corresponding ServiceNow users in your instance. Each row in the table shows three columns:

 -   OSCAL User: The user name as it appears in the OSCAL file.
-   ServiceNow User: The corresponding ServiceNow user. Users are mapped automatically when a ServiceNow user with a matching username is found. If no match is found, this field is empty and must be mapped manually.
-   Listed as: The roles the user is assigned to in the import. A user can be listed under multiple roles. For example, System Owner, Owner \(Control\), Attestation Respondents \(Control\), Assigned To \(POA&amp;M\), SCA, Assigned To \(Engagement\), ISSM, ISSO, Authorizing Official, AODR, Approver, Information Owner, System User, Issue Manager, Auditors, or Watchlist \(POA&amp;M\).

For OSCAL users without a corresponding ServiceNow user, select the appropriate ServiceNow user from the ServiceNow User field. You can also update any auto-mapped user if needed.

 \[Omitted image "oscal-ar-user-mapping.png"\] Alt text: User mapping

</td></tr><tr><td>

Group mapping

</td><td>

Map the groups listed in the OSCAL file to the corresponding ServiceNow groups in your instance. Each row shows the OSCAL group, the corresponding ServiceNow group, and the role the group is listed as. For example, Issue Manager Group. Groups are mapped automatically when a matching ServiceNow group is found. If no match is found, select the appropriate ServiceNow group manually. \[Omitted image "oscal-ar-group-mapping.png"\] Alt text: Group mapping

</td></tr><tr><td>

Roles and responsibility

</td><td>

Assign users to the authorization package roles for the imported files. The roles are pre-populated based on the user mappings completed in the User mapping section. The following roles are available: -   Authorizing Official \(AO\) \(required\)
-   System Owner \(required\)
-   Information System Security Officers \(ISSO\) \(required\)
-   Security Control Assessors \(SCA\) \(required\)
-   Authorizing Official Designated Representatives \(AODR\)
-   Information Owners
-   Information System Security Managers \(ISSM\)
-   System Users
 \[Omitted image "oscal-ar-roles-mapping.png"\] Alt text: Roles mapping

</td></tr></tbody>
</table>7.  In the **Preview and Override** step, review the summary of records that will be created, skipped, or overridden.

    The preview table shows the record types and their counts across three columns: **Will be created**, **Will be skipped**, and **Overridden**.

    **Note:** Existing control objectives from the same source and reference are skipped automatically, and new entries are created for any new sources.

    1.  If the engagement items from this package already exist on the instance, choose whether to skip or override them.

    2.  To skip specific object types, select the object from the **Select the ones you would wish to override** list, select **Skip**, select the records, and then select the **Override** button.

    3.  To override a specific object type, select the object from the **Select the ones you would wish to override** list, and select **Overridden**, and then select the **Override** option.

    4.  Select **Import** to start the import.

        A confirmation message appears indicating the import has started. Select **Close** to return to the OSCAL Import page.

        The import runs in the background and can take several minutes. When complete, the import record appears on the OSCAL Import page. If you specified import status recipients in the Details step, they are notified when the import completes.


**Parent Topic:**[Import in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.md)

