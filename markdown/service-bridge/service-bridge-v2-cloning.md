---
title: List of preserve and exclude tables for cloning
description: When installing Service Exchange, certain tables must be preserved or excluded to maintain connectivity after a clone.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Service Exchange]
---

# List of preserve and exclude tables for cloning

When installing Service Exchange, certain tables must be preserved or excluded to maintain connectivity after a clone.

If the default system profile is used, some of the Service Exchange table data isn’t preserved. To address this issue, you must create a custom clone profile with specific settings required for Service Exchange. Navigate to **All** &gt; **System Clone** &gt; **Clone Profiles** and select **New** to create a custom profile. For more details on clone profiles, see [Create a custom clone profile](https://www.servicenow.com/docs/access?context=configure-clone-profile&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). In this profile, you must:

-   Remove the **Remote Process Sync Disable Records** script from the Cleanup scripts related list,
-   Validate if the following Service Exchange tables are included in the custom profile.

**Note:** After a clone, you must reestablish the connection and activate the Capture Definitions. See [Reestablish connection after a clone for a provider](../task/service-bridge-v2-cloning-instances.md) and [Reestablish connection after a clone for a consumer](../task/service-bridge-v2-cloning-instances-con.md).

## Service Exchange tables to preserve

Add the following Service Exchange tables to the Clone Profile Preservers list if they’re missing. Remove any Service Exchange tables that aren’t in this list.

<table id="table_rsh_4jy_wgc"><thead><tr><th>

 

</th><th>

Preserve Tables

</th><th>

Exclude Tables

</th></tr></thead><tbody><tr><td>

Global

</td><td>

-   catalog\_ui\_policy
-   catalog\_ui\_policy\_action
-   ih\_sync\_capture\_definition
-   ih\_sync\_definition
-   ih\_sync\_inbound\_definition
-   ih\_sync\_outbound\_definition
-   ih\_sync\_process\_event
-   ih\_sync\_remote\_system
-   item\_option\_new
-   sc\_cat\_item\_catalog
-   sc\_cat\_item\_category
-   sc\_cat\_item\_user\_criteria\_mtom
-   sc\_cat\_item\_user\_criteria\_no\_mtom
-   sc\_category
-   scan\_finding
-   scan\_task
-   sn\_sb\_con\_entitlement
-   sn\_sb\_error
-   sn\_sb\_known\_error\_code
-   sn\_sb\_con\_provider\_connection
-   sn\_sb\_con\_provider\_task
-   sn\_sb\_release
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_rps\_connection
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line
-   sn\_transport\_queue

</td><td>

-   ih\_sync\_capture\_definition
-   ih\_sync\_definition
-   ih\_sync\_inbound\_definition
-   ih\_sync\_outbound\_definition
-   ih\_sync\_process\_event
-   ih\_sync\_remote\_system
-   scan\_finding
-   scan\_task
-   sn\_sb\_error
-   sn\_sb\_pro\_persona
-   sn\_sb\_remote\_task
-   sn\_sb\_rps\_connection
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line
-   sys\_alias

</td></tr><tr><td>

Base

</td><td>

-   sn\_sb\_authorized\_user
-   sn\_sb\_error
-   sn\_sb\_identity
-   sn\_sb\_known\_error\_code
-   sn\_sb\_provider\_task
-   sn\_sb\_release
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_remote\_task
-   sn\_sb\_scratchpad
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line

</td><td>

-   sn\_sb\_authorized\_user
-   sn\_sb\_connection
-   sn\_sb\_entitlement
-   sn\_sb\_error
-   sn\_sb\_identity
-   sn\_sb\_provider\_task
-   sn\_sb\_remote\_record\_producer
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_remote\_task
-   sn\_sb\_scratchpad
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line

</td></tr><tr><td>

Provider

</td><td>

-   sn\_sb\_pro\_authorized\_user
-   sn\_sb\_pro\_consumer\_connection
-   sn\_sb\_pro\_entitlement
-   sn\_sb\_pro\_provider
-   sn\_sb\_pro\_provider\_task
-   sn\_sb\_pro\_registration
-   sn\_sb\_pro\_remote\_choice\_definition
-   sn\_sb\_pro\_remote\_record\_producer
-   sn\_sb\_pro\_remote\_service
-   sn\_sb\_pro\_remote\_task
-   sn\_sb\_pro\_remote\_task\_variable
-   sn\_sb\_pro\_service\_bridge\_settings
-   sn\_sb\_pro\_transform

</td><td>

-   sn\_sb\_pro\_inbound\_field
-   sn\_sb\_pro\_outbound\_field
-   sn\_sb\_pro\_provider
-   sn\_sb\_pro\_registration
-   sn\_sb\_pro\_remote\_record\_producer\_consumer\_criteria
-   sn\_sb\_pro\_remote\_task\_def
-   sn\_sb\_pro\_remote\_task\_def\_consumer\_criteria
-   sn\_sb\_pro\_remote\_task\_variable
-   sn\_sb\_pro\_transform

</td></tr><tr><td>

Consumer

</td><td>

-   sn\_sb\_con\_authorized\_user
-   sn\_sb\_con\_consumer
-   sn\_sb\_con\_entitlement
-   sn\_sb\_con\_inbound\_field
-   sn\_sb\_con\_outbound\_field
-   sn\_sb\_con\_provider\_task
-   sn\_sb\_con\_remote\_record\_producer
-   sn\_sb\_con\_remote\_task
-   sn\_sb\_con\_remote\_task\_def
-   sn\_sb\_con\_remote\_task\_variable
-   sn\_sb\_con\_service\_bridge\_settings
-   sn\_sb\_con\_transform

</td><td>

-   sn\_sb\_con\_consumer
-   sn\_sb\_con\_inbound\_field
-   sn\_sb\_con\_outbound\_field
-   sn\_sb\_con\_persona
-   sn\_sb\_con\_remote\_task\_def
-   sn\_sb\_con\_remote\_task\_variable
-   sn\_sb\_con\_transform

</td></tr><tr><td>

Remote Process Sync Transport

</td><td>

sn\_sb\_rps\_connection \(Provider only\)

</td><td>

sn\_sb\_rps\_connection \(Provider only\)

</td></tr><tr><td>

Transporter

</td><td>

-   sn\_transport\_profile\*
-   sn\_transport\_queue\*

</td><td>

Na

</td></tr><tr><td>

Employee Profile

</td><td>

-   user\_criteria
-   sys\_alias
-   sys\_user
-   sys\_user\_has\_role

</td><td>

 

</td></tr></tbody>
</table>"\*" - Applicable for both provider and consumer.

**Parent Topic:**[Service Exchange reference](service-bridge-v2-reference.md)

