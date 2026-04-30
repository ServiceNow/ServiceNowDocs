---
title: Resolve time
description: The Resolve time field is available on the Incident \[incident\] and Request \[sc\_request\] tables. This field allows for easy reporting on how long it takes for requests to be closed, and is stored as an integer number of seconds.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Task fields for measuring work time, Default date and time fields, Date and Date/Time fields, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Resolve time

The **Resolve time** field is available on the Incident \[incident\] and Request \[sc\_request\] tables. This field allows for easy reporting on how long it takes for requests to be closed, and is stored as an integer number of seconds.

## Business rule calculation

Specific business rules calculate the **Resolve time** field when the record is resolved or marked closed, and measures the difference between the **Opened** and **Closed** dates. The field is stored in the system as an integer number of seconds.

-   On the Incident table, the field is calculated on closure by the business rule **mark\_closed**. The following lines of code calculate the resolve time:

    ```
    if (dataChange || current.calendar_stc.nil())
          current.calendar_stc = gs.dateDiff(opened, resolved, true);
    ```

-   When the incident is closed directly, the calculation is based on the **mark\_closed** business rule. The following lines of code calculate the resolve time:

    ```
    if (dataChange || current.calendar_stc.nil())
            current.calendar_stc = gs.dateDiff(opened, closed, true);
    ```


-   **[Display resolve time as a duration](../task/t_DisplayResolveTimeAsADuration.md)**  
You can display the resolve time as a human-readable duration rather than an integer representing a duration in seconds.

**Parent Topic:**[Task fields for measuring work time](c_TaskFieldsForMeasuringWorkTime.md)

