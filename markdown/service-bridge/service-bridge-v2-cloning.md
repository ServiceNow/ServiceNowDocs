---
title: Cloning instances with Service Exchange
description: When installing Service Exchange, certain tables must be preserved or excluded to maintain connectivity after a clone.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service Exchange reference, Service Exchange]
---

# Cloning instances with Service Exchange

When installing Service Exchange, certain tables must be preserved or excluded to maintain connectivity after a clone.

If the default system profile is used, some of the Service Exchange table data isn’t preserved. To address this issue, you must create a custom clone profile with specific settings required for Service Exchange. Navigate to **All** &gt; **System Clone** &gt; **Clone Profiles** and select **New** to create a custom profile. For more details on clone profiles, see [Create a custom clone profile \(legacy\)](https://www.servicenow.com/docs/access?context=system-profile-clone&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). In this profile, you must validate if the following Service Exchange tables are included in the custom profile:

**Note:**

-   If the same company isn’t present on the provider and consumer instances, the Company field is deleted, and the inbound and outbound connections move to an Error state.
-   Even if the same company is present on both the instances, the Connection may be in an Error state. In this case, you must reestablish the connection and activate the Capture Definitions.

## Service Exchange tables to preserve

Add the following Service Exchange tables to the Clone Profile Preservers list if they’re missing. Remove any Service Exchange tables that aren’t in this list.

<table id="table_lrh_1gz_bfc"><thead><tr><th>

Users

</th><th>

Table names

</th></tr></thead><tbody><tr><td>

Provider

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
-   sn\_sb\_authorized\_user
-   sn\_sb\_error
-   sn\_sb\_identity
-   sn\_sb\_known\_error\_code
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
-   sn\_sb\_provider\_task
-   sn\_sb\_release
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_remote\_task
-   sn\_sb\_rps\_connection
-   sn\_sb\_scratchpad
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line
-   sn\_transport\_profile
-   sn\_transport\_queue
-   sys\_alias
-   sys\_user
-   sys\_user\_has\_role
-   user\_criteria

</td></tr><tr><td>

Consumer

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
-   sn\_sb\_authorized\_user
-   sn\_sb\_con\_authorized\_user
-   sn\_sb\_con\_consumer
-   sn\_sb\_con\_entitlement
-   sn\_sb\_con\_inbound\_field
-   sn\_sb\_con\_outbound\_field
-   sn\_sb\_con\_persona \(consumer side\)
-   sn\_sb\_con\_provider\_connection
-   sn\_sb\_con\_provider\_task
-   sn\_sb\_con\_remote\_record\_producer
-   sn\_sb\_con\_remote\_task
-   sn\_sb\_con\_remote\_task\_def
-   sn\_sb\_con\_remote\_task\_variable
-   sn\_sb\_con\_service\_bridge\_settings
-   sn\_sb\_con\_transform
-   sn\_sb\_error
-   sn\_sb\_identity
-   sn\_sb\_known\_error\_code
-   sn\_sb\_provider\_task
-   sn\_sb\_release
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_remote\_task
-   sn\_sb\_rps\_connection
-   sn\_sb\_scratchpad
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line
-   sn\_transport\_profile
-   sn\_transport\_queue
-   sys\_alias
-   sys\_user
-   sys\_user\_has\_role
-   user\_criteria

</td></tr></tbody>
</table>## Service Exchange tables to exclude

Add the following Service Exchange tables to the Clone Profile Exclusions list if they’re missing. Remove any Service Exchange tables that aren’t in this list.

<table id="table_mk2_x3z_bfc"><thead><tr><th>

Users

</th><th>

Table names

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

-   ih\_sync\_capture\_definition
-   ih\_sync\_definition
-   ih\_sync\_inbound\_definition
-   ih\_sync\_outbound\_definition
-   ih\_sync\_process\_event
-   ih\_sync\_remote\_system
-   scan\_finding
-   scan\_task
-   sn\_sb\_authorized\_user
-   sn\_sb\_connection
-   sn\_sb\_entitlement
-   sn\_sb\_error
-   sn\_sb\_identity
-   sn\_sb\_pro\_inbound\_field
-   sn\_sb\_pro\_outbound\_field
-   sn\_sb\_pro\_persona
-   sn\_sb\_pro\_provider
-   sn\_sb\_pro\_registration
-   sn\_sb\_pro\_remote\_record\_producer\_consumer\_criteria
-   sn\_sb\_pro\_remote\_task\_def
-   sn\_sb\_pro\_remote\_task\_def\_consumer\_criteria
-   sn\_sb\_pro\_remote\_task\_variable
-   sn\_sb\_pro\_transform
-   sn\_sb\_provider\_task
-   sn\_sb\_remote\_record\_producer
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_remote\_task
-   sn\_sb\_rps\_connection
-   sn\_sb\_scratchpad
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line
-   sn\_transport
-   sys\_alias

</td></tr><tr><td>

Consumer

</td><td>

-   ih\_sync\_capture\_definition
-   ih\_sync\_definition
-   ih\_sync\_inbound\_definition
-   ih\_sync\_outbound\_definition
-   ih\_sync\_process\_event
-   ih\_sync\_remote\_system
-   scan\_finding
-   scan\_task
-   sn\_sb\_authorized\_user
-   sn\_sb\_con\_consumer
-   sn\_sb\_con\_inbound\_field
-   sn\_sb\_con\_outbound\_field
-   sn\_sb\_con\_persona \(consumer side\)
-   sn\_sb\_con\_remote\_task\_def
-   sn\_sb\_con\_remote\_task\_variable
-   sn\_sb\_con\_transform
-   sn\_sb\_connection
-   sn\_sb\_entitlement
-   sn\_sb\_error
-   sn\_sb\_identity
-   sn\_sb\_provider\_task
-   sn\_sb\_remote\_record\_producer \(consumer side\)
-   sn\_sb\_remote\_script\_approval
-   sn\_sb\_remote\_task
-   sn\_sb\_rps\_connection
-   sn\_sb\_scratchpad
-   sn\_sb\_service\_bridge\_settings
-   sn\_sb\_transform\_line
-   sn\_transport
-   sys\_alias

</td></tr></tbody>
</table>**Parent Topic:**[Service Exchange reference](service-bridge-v2-reference.md)

