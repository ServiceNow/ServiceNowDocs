---
title: CPQ Upgrade Schedule
description: CPQ updates customer environments on a predictable bi-weekly schedule to deliver new features, enhancements, and fixes. Test environments are upgraded first, with production updates following after at least 14 days to ensure stability. You can identify your environment’s sector from its URL and refer to the Upgrade Calendar to see which version your instance is currently running.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# CPQ Upgrade Schedule

CPQ updates customer environments on a predictable bi-weekly schedule to deliver new features, enhancements, and fixes. Test environments are upgraded first, with production updates following after at least 14 days to ensure stability. You can identify your environment’s sector from its URL and refer to the Upgrade Calendar to see which version your instance is currently running.

CPQ Development iterates the application quickly, releasing new software to customers about every two weeks. Each release delivers new features, enhances existing features, and fixes bugs. The benefits of each release are outlined in the corresponding Build Notes publication. Build Notes are sent to account holders of the CPQ Support Center; they are also posted in the Support Center.

Customer environments are upgraded according to the following table:

|Sector|Upgrade Window|Notes|
|------|--------------|-----|
|test|Biweekly, Thursday 8:00p CT| |
|prod|Biweekly, Friday 8:00p CT|A build is pushed to production no less than 14 days after it was introduced to test environments. To reduce the risk of upgrading prod environments as fiscal periods are ending, the schedule avoids upgrading prod environments at the ends of calendar months.|

To determine which version of CPQ your environment is on, first determine the sector of your environment by inspecting its URL. The sector precedes "logik.io" in the URL. For example, in the URL https://customName.prod.logik.io, the sector is prod. Then, find the current day in the [Upgrade Calendar](https://calendar.google.com/calendar/embed?src=c_ucaqgepi0m001s34faoai41n4g%40group.calendar.google.com&ctz=America%2FChicago). Review the corresponding test or prod entry for this day.

**Parent Topic:**[CPQ reference](../reference/servicenow-cpq-reference.md)

