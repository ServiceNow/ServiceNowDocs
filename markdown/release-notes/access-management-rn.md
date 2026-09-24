---
title: Access Management release notes
description: The ServiceNow Access Management application provides robust tools to manage security data on the ServiceNow AI Platform. Access Management includes many controls, such as access control lists \(ACLs\), security attributes, security data filters, and machine identity access control. These controls provide granular control and help improve security for managing data access. See the following sections for release notes by version.The Brazil Early Availability release adds security features for Access Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/access-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Access Management release notes

The ServiceNow® Access Management application provides robust tools to manage security data on the ServiceNow AI Platform. Access Management includes many controls, such as access control lists \(ACLs\), security attributes, security data filters, and machine identity access control. These controls provide granular control and help improve security for managing data access. See the following sections for release notes by version.

## About Access Management

-   Validate access controls configured within various resources and agentic assets with Access Analyzer.
-   Improve your security posture by ensuring that access to applications and data is granted on a least privilege basis with Zero Trust Access.
-   Use Access Findings, the proactive detection and remediation layer within Access Management Console, to run base system access checks against your instance on a daily schedule.
-   Restrict access to data by requiring users to pass a set of requirements before they can interact with it by using ACLs.
-   Control which Customer Service and Support employees can access your instance, and when, using the SNC Access Control plugin \(com.snc.snc\_access\_control\).

See [Access Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/access-management-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Access Management is a ServiceNow AI Platform feature that is active by default.


## Accessibility and localization

-   **Accessibility information**

    Coral is the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme uses brand-neutral illustrations. A dark theme option is available for web and mobile experiences.


## Brazil Early Availability

The Brazil Early Availability release adds security features for Access Management.

### What's changed

-   **[Explore Access Control Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/exploring-access-control-list.md)**

    Improve access control predictability by enforcing strict denial when none of the referenced roles referenced in an ACL exist on the instance. This behavior doesn't apply to ACLs that have a mix of valid and invalid roles. This behavior is on by default for new instances. If you upgraded to this release, use the **glide.security.acl\_with\_invalid\_roles\_strict\_deny** property to turn it on. Navigate to **All** &gt; **Access Management** &gt; **Access Findings** to find these ACLs in the Access Checks list.


