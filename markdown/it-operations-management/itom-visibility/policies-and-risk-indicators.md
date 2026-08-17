---
title: About Policy as Code Engine policies
description: Cryptographic Asset Compliance uses Policy as Code Engine \(PaCE\) policies to evaluate your cryptographic assets and flag risk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/policies-and-risk-indicators.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Explore, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# About Policy as Code Engine policies

Cryptographic Asset Compliance uses Policy as Code Engine \(PaCE\) policies to evaluate your cryptographic assets and flag risk.

Policies evaluate cryptographic assets and raises a risk indicator when an asset meets a risk condition. Separate policies apply to certificates, AWS KMS keys, and Azure Key Vault keys. Note that some policies calculate the overall risk level for an asset by combining the results of the other policies rather than raising an indicator of their own. For more information, see [Cryptographic Asset Compliance policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/policies.md).

Most policies are active by default and run automatically, so you don't have to set them up. However, the certificate authority trust policy is inactive by default because it depends on the certificate authorities that your organization trusts. You activate it after you add those authorities. For more information, see [Configure trusted certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/add-trusted-certificate-authorities.md).

## Managing policies

You can manage policies using PaCE. You can activate or deactivate a policy and edit its configuration, including the risk criticality that it assigns and review or revert your changes. For more information, see [Manage PaCE policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/pace-admin-manage-policies.md).

**Note:** Because a change affects how risk is calculated for the assets that the policy evaluates, avoid changing a policy, other than adding trusted certificate authorities.

