---
title: Import set performance
description: The algorithm transforms import sets from their staging table into their final destination.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Import set performance

The algorithm transforms import sets from their staging table into their final destination.

Importing data via an import set requires two phases:

1.  The data is loaded from a data source into a staging table
2.  The data is transformed from the staging table into a target table

The transform algorithm operates in "blocks" of 100 records at a time as opposed to the previous algorithm which transformed a single record at a time. The newer approach allows the application server to pre-fetch a variety of information relevant to each block of records, reducing the number of unique interactions with the database and improving throughput.

Who should expect to see a performance improvement?

Any customer using import sets should expect to see a performance improvement in large transformations.

What kinds of transformations benefit the most from these changes?

Transformations with a large number of reference or choice type columns see the largest improvement.

What kind of transformations benefit the least?

Transformations that with complex or unkeyed coalesce conditions see a proportionately smaller benefit.

