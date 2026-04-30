---
title: Privacy assessment configurations
description: To perform a processing activity criticality and privacy risk assessment, two risk assessment methodologies \(RAMs\) are provided by default.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Risk assessments, Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Privacy assessment configurations

To perform a processing activity criticality and privacy risk assessment, two risk assessment methodologies \(RAMs\) are provided by default.

The RAM is a configuration or a record in the risk assessment engine. It is a part of the Advanced Risk application. The RAM is used for assessing either the risks or objects in your organization. A configured RAM is an object with associated assessment types that have associated factors. This allows an organization to have different methodologies for assessing risk. To understand more about the factors or questions used in the assessments, refer to [Factors in Advanced Risk Assessment](../../grc-risk/concept/factors.md).

The privacy-specific RAM records have the **Domain** field set to **Privacy**. As a privacy administrator, you can make a copy of the default RAMs and modify them. To understand more about RAM configurations, refer to [Configure a risk assessment methodology](../../grc-risk/task/configure-ram.md). To understand how you can make a copy of a RAM, refer to and [Copy a risk assessment methodology](../../grc-risk/task/copy-ram.md).

**Note:** Because only two RAMs are permitted for use at a time, you must retire the old criticality RAM and publish the new RAM to utilize the criticality automation.

It is important to consider the following points when performing risk assessments.

-   In the **Privacy** domain, you can only modify a RAM. Creation of a RAM is not permitted.
-   Only two active RAMs are allowed. If you must copy or modify more than two RAMs, you must retire one.
-   The RAM can be configured and its order can be modified according to your requirements.
-   Users with the following roles can perform the privacy-related criticality and detailed privacy risk assessments.
    -   Privacy business user \(sn\_privacy.business\_user\)
    -   Privacy analyst who owns the processing activity
    -   Privacy assessment responder \(sn\_privacy.assessment\_responder\)
    -   Privacy manager \(sn\_privacy.manager\)

**Parent Topic:**[Risk assessments in Privacy Management](risk-assessments-in-privacy-management.md)

