---
title: Define a relative duration
description: You can define a relative duration to work out duration time for SLAs.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define a relative duration

You can define a relative duration to work out duration time for SLAs.

## Procedure

-   From the left navigation pane, select **System Scheduler** &gt; **Relative Durations.**.

    Four base Relative Durations are available:

    -   Two business days by 4pm
    -   Three business days by 4pm
    -   Next business day by 4pm
    -   End of next business day
    **Note:** The business schedule you use defines business day durations. If you define no schedule, by default the durations are 24 X 7.


## Example

Look at the End of next business day Relative Duration. From the Relative Durations list, select the **End of next business day** Relative Duration. The variable *days* is set to one, because the result of this calculation should land one day in the future. The rest of the script is as in the screenshot. If desired, you can customize the time at which you want the Relative Duration to end \(currently set to 5pm\).

![End of Next Business Day Relative Duration](../image/EndOfNextBusDay.png)

There is one more important Relative Duration design aspect that is used by the other three out-of-box Relative Durations. To illustrate this design lets look at **2 business days by 4pm**.

As you can see in the image, within the script there is an if-statement. This if-statement is checking to see if the calculated time is after 10am. If it is, then an extra day is added to the calculation. Hence the description of `2 business days by 4pm if before 10am`.

![2 Business Days by 4 pm Relative Duration](../image/TwoBusDays.png)

The "End of the business day" has nothing to do with the associated schedule. The end time of 17:00 is hard-coded into this Relative Duration script. If you want the time to be different than 5pm, you must change it in the script.

**Parent Topic:**[Using time configuration](../using-time-configuration.md)

