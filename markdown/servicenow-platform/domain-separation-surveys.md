---
title: Domain separation and Surveys
description: Domain separation is supported in Surveys. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Surveys reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Surveys

Domain separation is supported in Surveys. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Overview

As a survey creator, survey\_admin can create surveys in the assigned domain. A Global domain survey\_admin can create or edit survey in any domain.

As a survey taker, a user can access the survey record and take the survey based on the domain of the survey record and user. Global domain users can take a survey in any domain.

## How domain separation works in Surveys

There are several main areas to consider in how domain separation works in Surveys.

**Surveys in domain-separated instances**

The following domains are available by default after activating the Domain Support-Domain Extensions Installer \[com.glide.domain.msp\_extensions.installer\] plugin. Only ServiceNow employees can activate this plugin.

-   Global
-   Acme
-   Cisco

**Access to surveys in domain-separated instances**

Based on the domain of the survey record and users, users can access the survey record and take the survey.

Global domain users can access survey records in any domain. Users in any other domain can access records in their domain and Global domain. For example, users in the Acme domain can access records in the Acme domain and the Global domain.

Global domain users can take a survey in any domain. Users in any other domain can take surveys in their domain as well as the Global domain. For example, users in Acme domain can take surveys in the Acme domain and the Global domain.

<table id="table_wmp_jlq_jdb"><tbody><tr><td>

**Location of the survey record**

</td><td colspan="3">

**Users who can access and take the survey**

</td></tr><tr><td>

N/A

</td><td>

Global

</td><td>

Acme

</td><td>

Cisco

</td></tr><tr><td>

Global

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Acme

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Cisco

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td></tr></tbody>
</table>Any domain user can assign a survey in that domain to the same domain user or a Global domain user. For example, an Acme domain user can assign a survey to a Global domain user or an Acme domain user. Users from other domains are not visible to the Acme domain user.

Although the Global domain user can view a survey from other domains, this user cannot assign the survey of one domain to a user from a different domain. For example, a Global domain user can assign a survey from the Acme domain to another Global domain user or an Acme domain user, but not to a Cisco domain user.

**Note:** When a task is closed in a child domain and the assigned survey is either in the child domain or the global domain, the user from the child domain can then take the survey.

**Trigger conditions in domain-separated instances**

A Global domain user can create a triggered condition for a survey from any domain. The Global domain user can create an incident and trigger the survey by selecting a user from the other domain in the **User field** under **Caller**. However, the Global user cannot assign the survey to the user of different domain.

A user can assign a trigger condition to a survey if the user belongs to the Global domain or the Survey domain.

If there is no domain path for a trigger condition, users from any domain can view the trigger condition. For example, in the `asmt_condition` table that has no column for the domain path, users from the Acme domain can view the trigger condition created by the Cisco domain users.

**Parent Topic:**[Surveys reference](../reference/survey-reference.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

