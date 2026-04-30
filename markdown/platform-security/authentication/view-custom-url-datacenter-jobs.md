---
title: Custom URL datacenter job information
description: Every custom URL that is associated to your instance has a corresponding ServiceNow datacenter job which runs and shows URL information that is pertinent to your instance as described in the table.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Custom instance URLs, Authentication, Access Management]
---

# Custom URL datacenter job information

Every custom URL that is associated to your instance has a corresponding ServiceNow datacenter job which runs and shows URL information that is pertinent to your instance as described in the table.

|Job field|Description|
|---------|-----------|
|Job ID|Unique ID of the job that checks the domain of the custom URL.|
|Last Run At|Date and time when the job last ran.|
|Payload|List of domains or custom URLs that were sent to the datacenter for CERT provisioning.|
|Poll Count|Number of times that the results have polled for this job.|
|Result|Verifies and validates each domain or custom URL sent in a payload.|
|Status|Status of the datacenter job.|

