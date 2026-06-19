---
title: Acknowledge a policy
description: After a policy has been published, you can create an acknowledgement campaign to define a group of your employees who must provide an acknowledgement that a particular policy is in compliance. When the campaign has been defined, you can submit the request to the audience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/policy-and-compliance-management/ack-policy.html
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage control objectives and policies, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Acknowledge a policy

After a policy has been published, you can create an acknowledgement campaign to define a group of your employees who must provide an acknowledgement that a particular policy is in compliance. When the campaign has been defined, you can submit the request to the audience.

Changes to the audience or validity dates in an Acknowledgement Campaign aren't immediately reflected in the associated acknowledgement records. Instead, these updates are processed by the "Policy acknowledgement nightly run" scheduled job.

To apply changes immediately, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and manually trigger "Policy acknowledgement nightly run."

-   **[Set up a policy acknowledgement campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/setup-ack-request.md)**  
A policy campaign is the record used to prepare for a policy acknowledgement request. It defines the audience who must provide an acknowledgement that a particular policy is in compliance. A policy campaign is requested only if the compliance user decides it is needed.
-   **[Submit an acknowledgement request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/submit-ack-request.md)**  
After you have created an acknowledgement campaign, you can submit the acknowledgement request to the defined audience.
-   **[Respond to an acknowledgement request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/acknowledge_policy.md)**  
After you have been identified as a member of an audience to provide a policy acknowledgement, you must open and review the record, and then acknowledge it.
-   **[Work with acknowledgements using the Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/ack-using-service-portal.md)**  
After you have received a request to provide acknowledgement for a policy, you have the option of working with the request in the ServiceNow AI Platform, or you can perform your actions in the ServiceNow Service Portal.

**Parent Topic:**[Manage control objectives and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/r_PoliciesAndProcedures.md)

