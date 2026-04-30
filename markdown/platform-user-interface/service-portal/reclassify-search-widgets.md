---
title: Reclassify cloned or customized search widgets
description: Search widgets that you cloned or customized before a system upgrade may not be compatible with AI Search. You can resolve this issue by running a fix script that reclassifies search widget instances.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable and configure AI Search in Service Portal, AI Search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Reclassify cloned or customized search widgets

Search widgets that you cloned or customized before a system upgrade may not be compatible with AI Search. You can resolve this issue by running a fix script that reclassifies search widget instances.

## Before you begin

1.  [Enable and configure AI Search in Service Portal](enable-ais-sp.md)
2.  Run the Portal Analyzer to identify all cloned or customized search widgets. For more information, see [Get a list of widgets per page](../concept/portal-analyzer.md#).
3.  For each cloned or customized search widget, copy the sys\_id value of each widget instance that is associated with the widget.
4.  For each cloned or customized search widget, ensure that the widget and its corresponding widget instances have the latest AI Search code from the base system search widget.

    **Warning:** Run the fix script only after you've updated all cloned or customized search widgets. If you run the fix script without first updating the widget code, the widgets won't be able to uptake the AI Search code later.


Role required: admin

## About this task

If you're unable to use AI Search in Service Portal, you may need to reclassify your cloned or customized search widgets. You can run the **Reclassifying Search widgets** fix script, which reclassifies widget instances to the *sp\_instance\_ais* class.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  On the list, find and open the record named **Reclassifying Search widgets**.

3.  On the form, update the script to define which widget instances to reclassify.

    Paste the sys\_id value of each search widget instance in the array. For example, you would enter the sys\_id values as follows:

    ```
    var instances = ["sys_id_1", "sys_id_2"];
    ```

4.  Save the form.

5.  Select **Run Fix Script**.


**Parent Topic:**[Enable and configure AI Search in Service Portal](enable-ais-sp.md)

