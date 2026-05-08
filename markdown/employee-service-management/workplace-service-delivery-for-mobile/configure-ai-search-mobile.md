---
title: Configure AI search for Workplace Service Delivery for Mobile
description: Install and configure AI search with Workplace Service Delivery for Mobile. Users can use AI search to search for campus, buildings, floors, or spaces.
locale: en-US
release: australia
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Service Delivery for Mobile, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Configure AI search for Workplace Service Delivery for Mobile

Install and configure AI search with Workplace Service Delivery for Mobile. Users can use AI search to search for campus, buildings, floors, or spaces.

## Before you begin

Role required: admin

**Note:** To enable AI search for Workplace Service Delivery for Mobile, you need to request for AI search and activate AI search. For more information about how to install and configure AI Search, see AI Search.

## Procedure

1.  Navigate to **AI Search** &gt; **AI Search Status**.

    A message is displayed that AI search application is not available and enabled on your instance.

2.  Click the **Request AI Search** button to trigger automatic activation of AI Search on your instance.

    Your request is processed and it may take some time for the AI Search application to be activated.

3.  After installing and configuring AI search, ensure that you have installed Workplace Core and Workplace Service Delivery for Mobile.

4.  Navigate to **All** &gt; **Search Configurations** &gt; **NowMobile App Search Configurations**.

5.  Change the Search engine to AI Search.

6.  Click **Save**.

7.  Navigate to **All** &gt; **AI Search Index** &gt; **Indexed Sources** &gt; **Workplace Location Table**.

8.  Select the **Index All Tables** button on the top right pane to open the Indexed Source History page.

    Indexed Source is queued for indexing. You can monitor the progress by refreshing this page. Once the Ingestion State is **Indexed**, the process is complete.


## Result

When the **Ingestion State** is **Indexed**, the AI search configuration is complete and you can login to the Workplace Service Delivery for Mobile app to search for campuses, buildings, and spaces using AI search.

**Parent Topic:**[Configure Workplace Service Delivery for Mobile](../concept/configure-wsd-mobile.md)

**Previous topic:**[Configure the Toggle map view property](configure-toggle-map-view.md)

**Next topic:**[Configure map properties for Location directory](wsd-mobile-map-config-properties-loc-directory.md)

