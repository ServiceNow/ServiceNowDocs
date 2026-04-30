---
title: Configure a private UI page for CMS links
description: With single sign-on \(SSO\) in place, you can generate email links that take users directly to tickets and applications through the CMS interface.
locale: en-US
release: zurich
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content pages in CMS, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure a private UI page for CMS links

With single sign-on \(SSO\) in place, you can generate email links that take users directly to tickets and applications through the CMS interface.

## Before you begin

Role required: content\_admin or admin

## About this task

You accomplish this procedure by creating a private UI page to redirect CMS links. Because the page is not public, it requires authentication and redirects to SSO appropriately.

## Procedure

1.  Check that your CMS site is private by completing the following steps.

    1.  Navigate to **Content Management** &gt; **Sites** &gt; **\[Your Site\]**

    2.  Verify that the **Login page** field has a page listed.

2.  Create a new UI page by completing the following steps.

    1.  Navigate to **System UI** &gt; **UI Pages**.

    2.  Click **New**.

    3.  Enter a **Name**, for example, **redirector**.

    4.  Enter the following Adobe Jelly code into the **HTML** field.

        ```
        <?xml version="1.0" encoding="utf-8"?><j:jelly trim="true" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null"><script type="script/javascript">
        		window.location.href="${sysparm_uri}";</script></j:jelly>
        ```

        The CMS now supports email links with following format:

        `http://<path to instance>/<UI page>.do?uri=/<CMS suffix>/<record type>.do%26sys_id=<record ID>`

        For example:

        `http://<instance name>.service-now.com/redirector.do?sysparm_uri=/ess/incident.do%26sys_id=46e3e949a9fe19810069b824ba2c761a`

        **Note:** If you are using SAML 2.0 update 1 for SSO, use the UI page **saml\_redirector** instead of creating a new UI page. For example, an email link to a SAML 2.0 redirector page would use the URL format:`http://<instance name>.service-now.com/` **saml\_redirector.do** `?sysparm_uri=/ess/incident.do%26sys_id=46e3e949a9fe19810069b824ba2c761a.`


**Parent Topic:**[Content pages in CMS](../concept/c_ContentPages.md)

