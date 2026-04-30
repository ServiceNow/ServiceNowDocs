---
title: Set up Content Analytics tracking
description: To use Content Analytics with custom pages or widgets, add the tracking profile to your Employee Center or service portal theme header and add the cdaAnalytics service to your custom widgets.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Content Analytics, Setup continuous improvement, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Set up Content Analytics tracking

To use Content Analytics with custom pages or widgets, add the tracking profile to your Employee Center or service portal theme header and add the cdaAnalytics service to your custom widgets.

## Before you begin

Role required: sn\_cda.analytics\_admin

## About this task

More steps for page tracking:

Add the tracking profile to your Employee Center or service portal theme header.

```
<widget
id="cda-site-analytics"
options="{ 'tracking_profile_name': '{PROFILE_NAME}', 'enable_logging': false}"
></widget>
```

**Note:** If you don’t specify a tracking profile in the options, content analytics tries to use the default tracking profile. See [Create a Content Analytics tracking profile](ecpro-content-analytics-setup.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Headers &amp; Footers**.

2.  Select your header \(Content Publishing Header, Employee Center Header, ESC Header, or HRMadrid Header\).

3.  If necessary, clone the header.

    For more information, see [Service Portal configuration page](https://www.servicenow.com/docs/access?context=service-portal-configuration-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US). Or, you can use Angular Providers, see [Reuse components with Angular Providers](https://www.servicenow.com/docs/access?context=angular-providers&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

4.  If using a clone from the Content Publishing header, search for the cda-site-analytics widget tag in the **Body HTML template** field.

5.  Then replace PROFILE\_NAME with the profile that you want to use for tracking.

    For more information, see [Configure a portal header menu](https://www.servicenow.com/docs/access?context=configure-header-menu&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

6.  If you’re using a different header, add the following to the Body HTML and replace PROFILE\_NAME:

    ```
    <widget
    id="cda-site-analytics"
    options="{ 'tracking_profile_name': '{PROFILE_NAME}', 'enable_logging': false}"
    ></widget>
    ```

    If you don’t specify a tracking profile in the widget options, content analytics tries to use the default tracking profile \(if it exists\).

    Track Employee Center events

    To track Employee Center events, add the cdaAnalytics service to your custom widgets. See [Widget developer guide](https://www.servicenow.com/docs/access?context=widget-dev-guide&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    For example:

    ```
    function ($scope, cdaAnalytics) {
    $scope.onButtonClick = function() {
    
    // track event using the default tracker (no argument for getTracker)
    cdaAnalytics.getTracker() .then(function(tracker) {
    tracker.trackEvent(
    '{Desired Category}',
    '{Desired Action}',
    '{Desired Name}'
    );
    });
    
    // track event using specific tracker
    cdaAnalytics.getTracker ('Human Resources Portal Tracker').then(function (tracker) {
    tracker.trackEvent(
    'Human Resources',
    'Video Viewed',
    'Open Enrollment 2018'
    );
    });
    };
    }
    ```

7.  Navigate to **Service Portal** &gt; **Widgets**.

8.  Select a widget or create one.

9.  Add cdaAnalytics to the Related List of Angular Providers.

10. Update the client controller of the widget to use the cdaAnalytics service.


