---
title: Defining login scenarios
description: You can direct all users to the same page after login.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Local Authentication, Authentication, Access Management]
---

# Defining login scenarios

You can direct all users to the same page after login.

## Before you begin

Role required: admin

## About this task

When users log on to an instance directly, such as going to http://\{instance\_name\}.service-now.com/, the system does the following:

1.  Accesses the value in the property **glide.entry.page.script**. The default value of the property is derived from a script include named CMSEntryPage.
2.  Directs the user to the instance login page if the entry page requires a login.
3.  Applies login rules, if any, to the user.

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


