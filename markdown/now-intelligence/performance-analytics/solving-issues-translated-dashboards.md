---
title: Solving issues on translated dashboards
description: Users can only find translated dashboards under certain configurations. You can translate the dashboard name to make it searchable.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Solving issues on translated dashboards

Users can only find translated dashboards under certain configurations. You can translate the dashboard name to make it searchable.

## Before you begin

On instances with language plugins enabled, the application first determines the database behind the instance. If the database is MySQL, then it looks for the user's session language and searches for the translated dashboard. For more information about language plugins, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The search function only works for translated dashboards when the instance uses the MySQL database and the dashboard translation is provided.

Role required: admin

## Procedure

1.  Log in to the instance in the source language.

2.  Navigate to **All** &gt; **Performance Analytics** &gt; **Dashboards**.

3.  Open the dashboard that you want to translate.

4.  Select your user icon and choose **Preferences**.

5.  Select the **Language &amp; Region** tile.

6.  From the **Language** menu, select the target language and close the dialog.

    Extra languages are available when there are enabled language plugins on the instance.

7.  From the context menu \(![](../../dashboards/image/icon-context-p.png)\), select **Dashboard Properties**.

8.  Translate the dashboard name into the target language and click **Update**.


## Result

Users can search for the dashboard using the translated name when their system is set to the target language.

