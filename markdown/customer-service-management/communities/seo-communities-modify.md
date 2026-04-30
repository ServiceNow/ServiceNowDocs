---
title: Modify SEO in community pages
description: If an auto-generated SEO meta tag does not meet your needs, you can modify or replace the tag.
locale: en-US
release: xanadu
product: Communities
classification: communities
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Community pages that support SEO data, Community Service Portal, Configure a community, Communities, Customer Service Management]
---

# Modify SEO in community pages

If an auto-generated SEO meta tag does not meet your needs, you can modify or replace the tag.

## Before you begin

Role required: sn\_communities.admin

## About this task

The source code for this example question page \(ID **community\_question**\) shows the **description** meta tag \(highlighted in yellow\) that the Communities application injected into the page.

![Community question page example about a router overheating after a firmware upgrade with options for the Community to subscribe to, reply to, or upvote this question.](../images/seo-question-page.png)

```
<!DOCTYPE html><html lang="en" ng-app="sn.$sp" ng-init="portal_id =
'5b49418bdb4aa200b1f6f78eaf96195f'" style="height: 100%" class="page-
{{page.sys_id}} v{{page.sys_id}}" data-page-id="{{page.sys_id}}"><head sp-
metatags=""><title>Routing and Switching - Router overheating after firmware 
upgrade - Community</title><meta http-equiv="X-UA-Compatible" content="IE=edge;
IE=10"></meta><meta name="viewport" content="width=device-width, initial-
scale=1.0, maximum-scale=1.0, user-scalable=no"></meta><meta name="apple-
mobile-web-app-capable" content="yes"></meta><meta http-equiv="cache-control"
content="public"></meta><meta http-equiv="cache-control" content="no-cache">
</meta><meta http-equiv="cache-control" content="max-age=0"></meta><meta http-
equiv="pragma" content="no-cache"</meta><meta name="description"
content=Routing and Switching - Tomahawk (5000 Series) - My 5000 series router
has been overheating since I upgraded the firmware couple of days ago. Anybody"
custom-tag=""></meta><link href="favicon.ico?v=4" rel="shortcut icon"></link>
<link href="images/mobile/apple_touch_snc.png?v=09-26-2017_1830" rel="apple-
touch-icon"></link><link type="text/css" rel="stylesheet"
href="/styles/css_includes_$sp.cssx?v=09-26-2017_1830"></link><link
href="styles/scss/sp-bootstrap.scss?
portal_id=5b49418bdb4aa200b1f6f78eaf96195f&amp;v=21989c86db6dc300b14a75921f9619
d9" rel="stylesheet" type="text/css"></link><link rel="stylesheet"
type="text/css" href="styles/sp-patch.css?v=21989c86db6dc300b14a75921f9619d9">
</link><link href="/styles/scss/csm-styles.scss?
portal_id=5b49418bdb4aa200b1f6f78eaf96195f&amp;v=7d88d886db6dc300b14a75921f9619
71" type="text/css" rel="stylesheet"></link><link type="text/css"
rel="stylesheet" href="/scripts/icon-fonts/font-awesome/css/font-awesome.cssx?
v=09-26-2017_1830"></link><script data-description=NOW session, user_name, 
etc">window.NOW = window.NOW || {};
      //record watch / presence
      window.NOW.session_id = '302E95AADBA14700B14A75921F9619A0' ;
      window.NOW.user_name = xxxxxxx
      window.NOW.user_id = '6816f79cc0a8016401c5a33be04be441' ;

```

The **description** meta tag text is made up of three data fields that are taken from the **communitiy\_question** record. In the tag, the values are separated by a hyphen character.

-   The first portion of the **description** meta tag is the value of the `forum name` field in the question record. In the example, the forum name is `Routing and Switching`.
-   The second portion of the tag is the value of the `topic` field in the record — `Tomahawk (5000 Series)` in the example.
-   The third portion of the tag is generated from the first 100 characters of the `body` field in the record — `My 5000 series router has been overheating since I upgraded the firware couple of days ago. Anybody`.

In addition to the **description** meta tag for a question page, the Communities application injects a **title** tag \(highlighted in blue\). The title is generated dynamically using two values from the **communitiy\_question** record:

-   Forum name \(`Routing and Switching` in the example\)
-   Short description \(`Router overheating after firmware upgrade` in the example\)

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages**.

2.  In the list of portal pages, click the **ID** of the page to update \(in the example, **community\_question**\).

    See the list of [pages in Communities that support SEO data](../reference/communities-seo-data.md).

3.  On the Page form:

    -   Modify or add meta tags in the **Meta tags** related list.
    -   Modify the **Dynamic page title** by modifying the structure of the title text or by modifying or replacing the variables that generate the text. The variable definitions appear in the **Dynamic page variables** related list.
    ![Two screenshots: first displaying page details and highlighting the Dynamic page title field, second highlighting the Meta tags tab and Dynamic page title variables tab with the related list.](../images/seo-page-form.png)


**Parent Topic:**[Community pages that support SEO data](../reference/communities-seo-data.md)

