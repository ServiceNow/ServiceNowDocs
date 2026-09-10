---
title: Define login scenarios
description: You can direct all users to the same page after login.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/t\_LoginScenarios.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Local authentication, Authentication, Access Management]
---

# Define login scenarios

You can direct all users to the same page after login.

## Before you begin

Role required: admin

This procedure requires the Content Management \(CMS\) plugin to be active. If you're using a Personal Developer Instance \(PDI\) or a basic instance without CMS enabled, the following navigation path may not be available. Verify that the **com.glide.cms** plugin is active before proceeding.

## About this task

When users log on to an instance directly, the system accesses the value in the property **glide.entry.page.script**. The default value of this property uses the CMSEntryPage script include. Verify that this script include exists in your instance before following the procedure.

To force the system to direct all users to the same page after login:

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Configuration** &gt; **Configuration Page**.

2.  Select a value for the Login page field, or create a new page as desired.

    If this page is not the site default page, it always redirects here. If it is a site default page, it applies login rules. If this value is null, the system uses navpage.do as the entry page. Do not enter a login page here; otherwise, users need to log in twice.

    Logging Into an Instance to access a record:

    When users log into an instance to access a record by its globally unique identifier \(sys\_id\), such as http://\{instance\}.service-now.com/incident.do?sys\_id=\{sys\_id\}, then the system does the following:

    1.  Directs the user to a login page if not already logged in.
    2.  Directs the user to the appropriate record if they are allowed to access it. If the user does not have access rights to the record, a denial of access message appears.
    Logging Into the Service Portal or a CMS site:

    When users log on the Service Portal or a CMS site, such as http://&lt;instance&gt;.service-now.com/site-name/page.do, the system does the following:

    -   If there is a value in the Login page field on the Service Portal or the CMS site form, it directs the user to that login page and applies login rules, if any, to the user.
    -   If there is no login page specified, it directs the user to the value in the Home page field on the Service Portal or the CMS site form.
    Logging Into the Service Portal or a CMS Site to access a record:

    When users log on to the Service Portal or a CMS site to access a record, such as http://\{instance\}.service-now.com/ess/incident\_detail.do?sysparm\_document\_key=incident,\{sys\_id\}, the system follows the same procedure and finally takes the user to the record. If the user does not have access rights to the record, a denial of access message appears.


