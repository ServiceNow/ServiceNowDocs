---
title: Using CPQ and Salesforce CPQ with community users
description: When partner and community users cannot authenticate in Salesforce, they can use a Runtime Client Token to authenticate with CPQ. Follow these setup steps.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Using CPQ and Salesforce CPQ with community users

When partner and community users cannot authenticate in Salesforce, they can use a Runtime Client Token to authenticate with CPQ. Follow these setup steps.

Community sites \(also known as Digital Experience sites\) require different user types than are normally used in Salesforce platform. Notably, these are for partner or community users that donʼt have the option to authenticate in Salesforce. Even if the community users have access to the CPQ Connected App, they need to use it through the Digital Experience site, so the login flow \(which automatically redirects to Salesforce\) wonʼt work in this case.

These are the steps to use a Runtime Client Token, along with custom Visualforce pages that are included as part of the CPQ Extension package, to authenticate with CPQ instead of the normal login flow.

## Audience

This article is for anyone that needs to use ServiceNow CPQ and Salesforce CPQ with a partner community or in a customer community environment. This page assumes that:

-   Basic setup of CPQ and Salesforce is complete.

    **Note:** The Visualforce pages referenced in this page are available only in CPQ Extension Package version 2.3 or later. CPQ Extension Package Version 2.3 itself requires the Base Managed Package version 2.2 or later.

-   A Digital Experience site that includes Salesforce CPQ quotes is available.
    -   This guide is not necessary if only Salesforce profiles \(such as System Administrator, Standard User, and so on\) will be using this site instead of Partner or Community users.
    -   If a Digital Experience site is not already available, note that at the time of this writing:
        -   Salesforce CPQ is not compatible with LWR templates, and Quote objects are only available on Aura.
        -   Partner/Customer users must have CPQ permission set licenses assigned to them.
        -   Sharing Settings should be enabled to allow access to all the CPQ related objects, such as: Products, Opportunities, Price Books, Quotes, Product Option, Product Feature, and so on.

## CPQ setup

A runtime client is required to authenticate community users. If a runtime client is not already available, follow these steps to create one:

1.  In CPQ Admin, go to Utilities &gt; Runtime Clients and click **+ New**.
2.  Provide a name, make sure at least Config is selected under "Permissions", and add the CPQ siteʼs URL to Origins.

    The Origin must be exact: it must include https://, and should have one origin with the trailing "/" and one without. On https://dev5.dev.logik.io, there should be an Origin of https://dev5.dev.logik.io and https://dev5.dev.logik.io/.

    ![Set up](../images/cpq-community-origin.png)

3.  Save.
4.  Copy the value using the clipboard icon under “Token” image.png.

    You will save this value to Salesforce Settings during Salesforce setup.


## Salesforce setup

1.  From the Salesforce App Launcher, search for and open the CPQ Admin Custom Settings page.

    ![Menu](../images/cpq-salesforce-logik-admin-settings.png)

2.  Next to the Runtime Client Token, click **Set**, paste the copied token from CPQ Admin, then Save.

    ![Admin package](../images/cpq-salesforce-runtime-client-token.png)

3.  Go to Security &gt; Session Settings.
4.  Under “Clickjack Protection”, select Enable clickjack protection for customer Visualforce pages with standard headers.
5.  Under “Trusted Domains for Inline Frames”, add \*.force.com. Set IFrameType to VisualforcePages.
6.  From Setup home, go to Apps &gt; Packaging &gt; Installed Packages.
7.  Next to the Salesforce CPQ package \(not the CPQ extension for CPQ\), click **Configure**.

    ![Uninstalled packages](../images/cpq-salesforce-cpq-configure.png)

8.  Under the Additional Settings tab, set the “External Configurator URL” to /apex/LGK\_\_CpqConfiguration.

    This field may be set to a full URL in CPQ, such https://dev5.dev.logik.io/ui/configure. The new value /apex/LGK \_CpqConfiguration is meant to be compatible with both Salesforce and Community users, so it can replace the CPQ URL.


