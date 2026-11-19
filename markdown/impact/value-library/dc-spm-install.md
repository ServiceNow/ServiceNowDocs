---
title: Install the Data Collection Pack for SPM
description: To enable the Data Collection Pack, you must install dependent plugins and activate Data Collection jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/impact/value-library/dc-spm-install.html
release: yokohama
product: Value Library
classification: value-library
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection Content Pack for SPM, Data Collection Toolkit, Value Management, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Install the Data Collection Pack for SPM

To enable the Data Collection Pack, you must install dependent plugins and activate Data Collection jobs.

## Before you begin

The SPM Success Metric Definitions in this application rely on another application. Ensure that the required plugins are installed if they are not already installed. For more information, see [Install Data Collection Content Pack dependent plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/impact/value-library/dc-install-plugins.md).

Role required: Impact users

## Procedure

1.  Navigate to the Impact workspace on your instance.

2.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Value PA Data Collection Jobs**.

    \[Omitted image "dct\_install\_all.png"\] Alt text: Menu in product with All &gt; Impact &gt;Configuration&gt; Value PA Data Collection Jobs selected.

3.  Select **Value PA Data Collection jobs**.

4.  Search for and select the following:

    -   **Impact VM - SPM - Monthly Data Collection**
    -   **Impact VM - SPM - Historical Data Collection**
    If you're having trouble finding the data collection jobs, check whether the required data collection-dependent plugins are installed correctly. See [Install Data Collection Content Pack dependent plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/impact/value-library/dc-install-plugins.md).


