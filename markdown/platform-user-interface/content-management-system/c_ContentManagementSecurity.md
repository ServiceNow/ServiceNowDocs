---
title: Content Management security
description: There are several methods for securing CMS sites and pages. Site security is set in the Login page field on the site record. You can control if a page is public or private through the URL.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Content sites, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content Management security

There are several methods for securing CMS sites and pages. Site security is set in the Login page field on the site record. You can control if a page is public or private through the URL.

Every content page has its own URL that users can access outside of the platform. Depending on how the Login page or roles are defined, the URL may or may not be public.

-   If the content page has no defined **Read** role or there is no defined Login page, any internet user can navigate to the URL and view the content page.
-   If there is a defined **Read** role, then anyone who goes to the URL is asked to log in before they can view the site.
-   If there is a defined Login page on the site record, all pages in the site are private.

## Content Management URLs

The format for Content Management URLs is as follows.

`<path to the instance> + /<site suffix> + /<page suffix> + .do`

The &lt;site suffix&gt; is defined by the **URL Suffix** field on the site form. The &lt;page suffix&gt; is defined by the **URL Suffix** field in the page form. The URL suffix is case-sensitive.

For example, the page **Austere - Site Entry** has a site **URL Suffix** of **austere** and a page **URL Suffix** of **entry**. The constructed URL looks like the following URL.

`<instance name>.service-now.com/austere/entry.do`

If the site **URL Suffix** field is left blank, the &lt;site suffix&gt; is **cms**, as shown in this example:

`instance.service-now.com/cms/page.do`

If the page **URL Suffix** is left blank, the name of the page is used as shown in this example:

`instance.service-now.com/austere/Page Name.do`

Special characters in the name of the page have to be escaped.

## Login pages instead of login rules

You set a login page on the site record to allow users to log in or out directly through the content site.

Login rules were used in earlier versions to dictate what users saw after logging in, based on their roles or permissions. Login rules still work, but their use is deprecated.

**Parent Topic:**[Content sites](c_ContentSite.md)

