---
title: Lifecycle event script includes and APIs
description: Script includes call workflows within Lifecycle Events.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [Lifecycle Event Script Includes, APIs]
breadcrumb: [Activate Lifecycle Events, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Lifecycle event script includes and APIs

Script includes call workflows within Lifecycle Events.

The following script includes are provided with Lifecycle Events:

|Name|Description|
|----|-----------|
|hr\_ActivitySet|Main script include for Lifecycle Events workflows and activity management.|
|LaunchActivities|API to launch an instance of all activities under an activity set. Called when a Lifecycle Event case is created.|
|getAvailableDependentActivitySets\(activitySet\)|Retrieves a collection of dependent activity sets for an activity set.|
|isActivitySetCompleted|Checks when all activities in a set are complete.|
|IsActivitySetActive|Checks when an activity set is active.|

The following APIs are provided with Lifecycle Events: hr\_LEType - Contains methods related to Lifecycle Event types, activity sets, and activity set activities.Methods related to Lifecycle Event Types:

-   createLEType\(@param - REQUIRES: Array of js objects having field name value pairs\) - Returns js object with status - 'success'.
-   updateLEType\(@param - REQUIRES: Array of js objects having field's name value pairs and Lifecycle Event Type Id\) - Returns js object with status - 'success'.
-   removeLEType\(@param - REQUIRES: Lifecycle Event Type Id\) - Returns js object with status - 'success'.

Methods related to Activity Sets:

-   createActivitySet\(@param - REQUIRES: Array of js objects having field's name value pairs\) - Returns js object with status - 'success'.
-   updateActivitySet\(@param - REQUIRES: Array of js objects having field's name value pairs and ActivitySetId\) - Returns js object with status - 'success'.
-   removeActivitySet\(@param - REQUIRES: activitySetId\) - Returns js object with status - 'success'.

Advanced:

-   Hr\_triggerUtil – Convenience methods for advanced scripting on running activity sets.
-   checkActivitySetsCompleted\(activitySetList\) – Verify when activity sets in the list are complete.
-   checkForElapsedDate\(date\) – Verify when the date passed in has elapsed.
-   checkForElapsedDateWithOffset\(date, offset, offsetUnits, offsetType\)

**Parent Topic:**[Activate Lifecycle Events](../task/activate-enterprise-onboarding-and-transitions-scoped.md)

