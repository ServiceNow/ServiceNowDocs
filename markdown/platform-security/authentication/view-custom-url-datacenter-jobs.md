---
title: Custom URL datacenter job information
description: Every custom URL that is associated to your instance has a corresponding ServiceNow datacenter job which runs and shows URL information that is pertinent to your instance as described in the table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/view-custom-url-datacenter-jobs.html
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Custom instance URLs, Authentication, Access Management]
---

# Custom URL datacenter job information

Every custom URL that is associated to your instance has a corresponding ServiceNow datacenter job which runs and shows URL information that is pertinent to your instance as described in the table.

|Job field|Description|
|---------|-----------|
|Job ID|Unique ID of the job that checks the domain of the custom URL.|
|Last Run At|Date and time when the job last ran.|
|Payload|List of domains or custom URLs that are sent to the datacenter for CERT provisioning.|
|Poll Count|Number of times that the results have been polled for this job.|
|Result|Verification and validation of each domain or custom URL sent in a payload.|
|Status|Status of the datacenter job.|

