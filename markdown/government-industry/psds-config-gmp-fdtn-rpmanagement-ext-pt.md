---
title: Configure the related party extension point in Grants Management
description: Remove related parties from a proposal when an applicant removes key personnel or an authorized representative.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-config-gmp-fdtn-rpmanagement-ext-pt.html
release: australia
topic_type: task
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the related party extension point in Grants Management

Remove related parties from a proposal when an applicant removes key personnel or an authorized representative.

## About this task

The Add Authorized Representative and Key Personnel intake activities requires an implementation of the `sn_svc_appl_info.RPManagement` extension point. When an applicant is deleted from a proposal, the system calls each implementation of this extension point to remove the related party records for that applicant.

## Before you begin

Role required: admin

## Procedure

1.  Change your application scope to **Customer Service** by selecting the application picker \(\[Omitted image "globe-fill-24.svg"\]\) in the Unified Navigation bar and selecting **Application Scope** &gt; **Customer Service**.

2.  Navigate to **All** &gt; **Scripted Extension Points** &gt; **Scripted Extension Points**.

3.  In the API name column, search for `sn_svc_appl_info.RPManagement` and select the record.

4.  Under Related Links, select **Create Implementation**.

5.  In the dropdown next to **Accessible from** field, select **All application scopes**.

6.  Select **Update**.

7.  Change your application scope back to **Global** by selecting the application picker \(\[Omitted image "globe-fill-24.svg"\]\) in the Unified Navigation bar and selecting **Application Scope** &gt; **Global**.

8.  Verify the implementation.

    In the Grants Management portal, create a proposal and remove a key personnel or an authorized representative. The removed individuals are also removed as related parties for the same proposal.


## Result

The related party extension point is implemented. When an applicant removes key personnel or an authorized representative from a proposal, the system also removes them as related parties for that proposal.

**Parent Topic:**[Configure Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-config-gmp-foundation.md)

**Previous topic:**[Configure scripted extension points in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-config-gmp-fdtn-scripted-ext-pt.md)

**Next topic:**[Configure Restricted Caller Access \(RCA\) for Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-config-gmp-fdtn-doc-template-rca.md)

