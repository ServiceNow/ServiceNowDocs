---
title: List of preservers and exclusions tables for cloning
description: When installing Service Exchange, certain tables must be preserved or excluded to maintain connectivity after a clone.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Service Exchange]
---

# List of preservers and exclusions tables for cloning

When installing Service Exchange, certain tables must be preserved or excluded to maintain connectivity after a clone.

If the default system profile is used, some of the Service Exchange table data isn’t preserved. To address this issue, you must create a custom clone profile with specific settings required for Service Exchange. Navigate to **All** &gt; **System Clone** &gt; **Clone Profiles** and select **New** to create a custom profile. For more details on clone profiles, see Create a custom clone profile. In this profile, you must:

-   Remove the **Remote Process Sync Disable Records** script from the Cleanup scripts related list,
-   Validate if the following Service Exchange tables are included in the custom profile.

**Note:** After a clone, you must reestablish the connection and activate the Capture Definitions. See [Reestablish connection after a clone for a provider](../task/service-bridge-v2-cloning-instances.md) and [Reestablish connection after a clone for a consumer](../task/service-bridge-v2-cloning-instances-con.md).

## Service Exchange tables to preserve and exclude

The following scenarios describe how clone operations affect table data based on table configuration in the preservers and the exclusions tables list.

|Preservers tables|Exclusions tables|Result on target instance|
|-----------------|-----------------|-------------------------|
|Included|Included|Target table retains existing data. The system preserves existing records and copies no records from the source.|
|Included|Not included|Target table retains existing records and receives additional records from the source table. The system does not overwrite existing records.|
|Not included|Included|Target table is empty after the clone. The system discards existing target records and copies no records from the source.|
|Not included|Not included|Target table contains only source table data. The system replaces all pre-existing target records with records from the source.|

Update the Clone Profile Preservers and Exclusions lists to include only the Service Exchange tables specified in the following preservers and exclusions tables. Add any missing tables from the specified lists and remove any Service Exchange tables that are not included in these lists.

<table id="table_rsh_4jy_wgc"><thead><tr><th>

 

</th><th>

Preservers table

</th><th>

Exclusions table

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
-   sn\_fds\_pro\_consumer\_criteria
-   sn\_fds\_pro\_inbound\_offering\_item
-   sn\_fds\_pro\_offering\_item
-   sn\_fds\_con\_outbound\_offering
-   sn\_fds\_con\_outbound\_subscription

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
-   sn\_fds\_pro\_consumer\_criteria
-   sn\_fds\_pro\_inbound\_offering\_item
-   sn\_fds\_pro\_inbound\_subscription
-   sn\_fds\_pro\_offering\_item
-   sn\_fds\_con\_m2m\_company\_offering
-   sn\_fds\_con\_outbound\_offering\_item
-   sn\_fds\_con\_outbound\_subscription

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

N/a

</td></tr><tr><td>

Employee Profile

</td><td>

-   user\_criteria
-   sys\_alias
-   sys\_user
-   sys\_user\_has\_role

</td><td>

sys\_alias

</td></tr><tr><td>

Foundation Data Sync

</td><td>

-   sn\_fds\_data\_processing\_queue
-   sn\_fds\_offering
-   sn\_fds\_offering\_item
-   sn\_fds\_request
-   sn\_fds\_subscription
-   sn\_fds\_subscription\_item

</td><td>

-   sn\_fds\_data\_processing\_queue
-   sn\_fds\_offering\_item
-   sn\_fds\_subscription
-   sn\_fds\_subscription\_item

</td></tr><tr><td>

Foundation Data Sync for Providers

</td><td>

-   sn\_fds\_pro\_inbound\_offering\_request
-   sn\_fds\_pro\_offering
-   sn\_fds\_pro\_offering\_request

</td><td>

-   sn\_fds\_pro\_inbound\_offering
-   sn\_fds\_pro\_inbound\_offering\_request
-   sn\_fds\_pro\_inbound\_subscription\_item
-   sn\_fds\_pro\_offering
-   sn\_fds\_pro\_subscription
-   sn\_fds\_pro\_subscription\_item

</td></tr><tr><td>

Foundation Data Sync for Consumers

</td><td>

-   sn\_fds\_con\_offering
-   sn\_fds\_con\_offering\_item
-   sn\_fds\_con\_offering\_request
-   sn\_fds\_con\_outbound\_offering\_request
-   sn\_fds\_con\_subscription
-   sn\_fds\_con\_subscription\_item

</td><td>

-   sn\_fds\_con\_offering\_item
-   sn\_fds\_con\_subscription
-   sn\_fds\_con\_subscription\_item

</td></tr><tr><td>

Health

</td><td>

-   sn\_sb\_issue
-   sn\_sb\_health\_connection\_stats
-   sn\_sb\_health\_issue

</td><td>

-   sn\_sb\_issue
-   sn\_sb\_health\_connection\_stats
-   sn\_sb\_health\_issue

</td></tr></tbody>
</table>"\*" - Applicable for both provider and consumer.

The following scenarios describe how clone operations affect table data based on table configuration in the Clone profile preservers list and the Exclude tables list.

The following examples use tables from this page to illustrate each scenario:

**sn\_sb\_service\_bridge\_settings** \(included in both lists\): The system preserves connection settings you configured on the target instance after the clone. Settings from the source instance do not overwrite them.

**sn\_sb\_con\_entitlement** \(included in Clone profile preservers only\): The target instance retains existing entitlement records and receives additional entitlement records from the source instance.

**sn\_sb\_error** \(included in Exclude tables only\): The error records table is empty on the target instance after the clone. The system discards error records that existed on the target and copies none from the source.

**sn\_fds\_offering** \(not included in either list\): The system replaces the target table with source data. Records that existed on the target instance before the clone are replaced by source instance records.

