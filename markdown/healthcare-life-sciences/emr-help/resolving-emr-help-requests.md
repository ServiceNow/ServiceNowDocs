---
title: Resolve EMR Help requests
description: You can use a ServiceNow instance to resolve requests generated in the EMR Help service portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/emr-help/resolving-emr-help-requests.html
release: zurich
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Resolve EMR Help requests

You can use a ServiceNow instance to resolve requests generated in the EMR Help service portal.

Work on task records that are automatically created when clinicians submit ServiceNow service requests from an EMR system.

As a fulfiller, for example, if you are an IT agent, you can access the task record for an IT service request on the ServiceNow instance linked with the EMR system. Incidents are the task type configured by default with the EMR Help application.

**Note:** The EMR Request Data related list of an incident form includes any EMR system-specific data. The data in the EMR Request Data related list is viewable only if you have the sn\_ind\_rmt\_help.viewer role in addition to the itil role. If you do not have the required roles, this related list appears empty.

In order to fulfill healthcare cases, you must first create your own custom healthcare case type. For more information on this, see [Configure healthcare case types for EMR Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/configure-hcls-case-types-for-emr-help.md).

Use Workspace to view requests submitted from an EMR system.

Use EMR Help for the following:

-   [Viewing and resolving ServiceNow IT service requests submitted from EMR systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/emr-help-issues-resolve.md)
-   [Viewing and resolving healthcare cases submitted from EMR systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/viewing-and-resolving-healthcare-cases-submitted-from-emr-systems.md)

