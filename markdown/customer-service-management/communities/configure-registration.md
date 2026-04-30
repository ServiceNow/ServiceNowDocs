---
title: Enable users to self-register to a community
description: Once users have accessed public forums and decided they want to join the community, they can self-register to the community. External user registration provides a way of validating users and requires them to accept the community Terms and Conditions.
locale: en-US
release: zurich
product: Communities
classification: communities
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring communities, Communities, Customer Service Management]
---

# Enable users to self-register to a community

Once users have accessed public forums and decided they want to join the community, they can self-register to the community. External user registration provides a way of validating users and requires them to accept the community Terms and Conditions.

Community administrators perform the following tasks to configure external user registration.

-   Configure the [external user registration properties](../reference/communities-properties.md).
-   [Configure moderation filters](../task/configure-moderation-filters.md) to enter banned words for the user name.
-   [Configure the required strength for passwords](https://www.servicenow.com/docs/access?context=config-pwd-strength-rqmts&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   [Create an email template](https://www.servicenow.com/docs/access?context=t_CreateAnEmailTemplate&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and content. The email template that you can change is **communities.ext.regn.confirm**.
-   If not already configured, [create community terms and conditions](../task/create-terms-conditions.md) that each community user must review and accept. Communities delivers preconfigured Terms and Conditions that you can modify according to your needs.
-   To enable external users to update their time zone when registering, add ACLs to external users in the User table \[sys\_user\].

