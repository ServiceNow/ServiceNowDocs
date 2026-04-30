---
title: Enable users to choose the identity provider for login
description: SSO federation support enables users to choose which IdP to log in to.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Enable users to choose the identity provider for login

SSO federation support enables users to choose which IdP to log in to.

## Before you begin

Role required: admin

## About this task

SSO federations aggregate metadata from multiple IdPs and service providers, including your instance. Federations then publish the metadata as an XML file, which includes information like IdP names and IdP certificates. Administrators can then instruct the instance to read the XML file and automatically populate the SSO Properties table with all the necessary IdP information.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Federation**.

2.  Click **New**.

3.  Fill in the fields, as appropriate \(see table\).

4.  Click **Submit**.

5.  After you configure a federation, enable the Refresh SSO Metadata scheduled job, and then [configure the users who you want to access the federation IdPs](../../authentication/concept/idpauthflow.md). Use the sys\_ID of the federation record you just created.

    Use the sys\_ID of the federation record that you just created.

    ![SSO Federations](../image/SSOFederation.png)

    The instance populates the SSO properties table with the IdP information. When users who are configured to use the federation log in, they are redirected to the discovery service URL you configured. Then they select the IdP and provide the necessary credentials. Alternatively, you can send users a URL with the IdP in the parameter.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a descriptive name for the federation.|
    |Active|Select the check box to enable the instance to pull the XML file from the federation.|
    |Type|Select the type of authentication this federation supports.|
    |Discovery Service URL|Enter the URL of the discovery service for this federation. This is the site where users are directed to select an IdP and log in.|
    |Meta Data URL|Enter the URL of the XML file that holds the federation metadata.|
    |x509 Certificate|Select the federation certificate.|
    |Domain|Select the domain that the data will belong to.|

    **Note:** The InCommon federated identity management IdP is preconfigured.


