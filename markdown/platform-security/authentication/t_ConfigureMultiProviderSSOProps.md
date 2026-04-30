---
title: Configure Multi-Provider SSO properties
description: Configure SSO properties and also add a property to the System Properties table to configure an IdP inclusion list.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Configure Multi-Provider SSO properties

Configure SSO properties and also add a property to the System Properties table to configure an IdP inclusion list.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Administration** &gt; **Properties**.

2.  Select the **Enable Multi-Provider SSO** check box.

    This selection adds the link Use external login to the login page.

3.  To [update the user table](../../saml/task/t_AdministerSAMLUserProvisioning.md) with the users in the IdP, select the **Enable Auto Importing** option.

4.  To enable the debug messages to appear at the bottom of the content frame, select the **Enable debug logging for the Multi-Provider SSO integration** check box.

    If enabled, the debug logging feature slows down performance and uses up disk space to generate logs.

5.  In the property **The field on the user table that identifies a user accessing the User identification login page**, enter the field on the User table that contains the value the IdP uses to identify the user. The default value is **user\_name**.

    The default value is **user\_name**.

    ![Multi-SSO properties.](../image/Multi-SSOProperties.png "Multiple Provider SSO properties")

6.  Click **Save**.

7.  Instruct your users to click the **Use external login** link when they log in to the instance.


**Related topics**  


[SAML user provisioning](../../saml/concept/c_SAMLUserProvisioning.md)

