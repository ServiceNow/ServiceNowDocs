---
title: Properties for Identification and Reconciliation
description: Use the Identification and Reconciliation properties to configure the identification and reconciliation engine \(IRE\).
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Reference, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Properties for Identification and Reconciliation

Use the Identification and Reconciliation properties to configure the identification and reconciliation engine \(IRE\).

These properties are available for Identification and Reconciliation. To view and edit these properties, the sn\_cmdb\_admin or admin role is required.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_cny_5y4_ts"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce the requirement that required attributes cannot be null during identification and reconciliation.

 glide.required.attribute.enabled

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**

</td></tr><tr><td>

Allow class upgrade during IRE identification and reconciliation.

 glide.class.upgrade.enabled

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

 When **false**, IRE rejects a payload \(or a payload item in Enhanced IRE\) with the respective reclassification update, and creates a [reclassification task](../task/t_ViewReclassificationTask.md).

</td></tr><tr><td>

Allow class downgrades during IRE identification and reconciliation.

 glide.class.downgrade.enabled

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

 When **false**, IRE rejects a payload \(or a payload item in Enhanced IRE\) with the respective reclassification update, and creates a [reclassification task](../task/t_ViewReclassificationTask.md).

</td></tr><tr><td>

Allow class switching during IRE identification and reconciliation.

 glide.class.switch.enabled

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

 When **false**, IRE rejects a payload \(or a payload item in Enhanced IRE\) with the respective reclassification update, and creates a [reclassification task](../task/t_ViewReclassificationTask.md).

</td></tr><tr><td>

glide.identification\_engine.update\_without\_upgrade\_enabled

</td><td>

Enable IRE to process CI updates with upgrade reclassification updates. This property takes precedence over the **glide.class.upgrade.enabled** property.

 -   Type: true \| false
-   Default value: false
-   Location: Add to System Properties \[sys\_properties\] table.
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

 Depending on the property setting, IRE processes or skips the upgrade update:

-   **true**: IRE processes the CI updates but doesn't process the CI upgrade reclassification update.
-   **false**: IRE processes the CI updates including the CI upgrade reclassification update.

</td></tr><tr><td>

glide.identification\_engine.update\_without\_downgrade\_enabled

</td><td>

Enable IRE to process CI updates with downgrade reclassification updates. This property takes precedence over the **glide.class.downgrade.enabled** property.

 -   Type: true \| false
-   Default value: false
-   Location: Add to System Properties \[sys\_properties\] table.
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

 Depending on the property setting, IRE processes or skips the downgrade update:

-   **true**: IRE processes the CI updates, but doesn't process the CI downgrade reclassification update.
-   **false**: IRE processes the CI updates including the CI downgrade reclassification update.

</td></tr><tr><td>

glide.identification\_engine.update\_without\_switch\_enabled

</td><td>

Enable IRE to process CI updates with switch reclassification updates. This property takes precedence over the **glide.class.switch.enabled** property.

 -   Type: true \| false
-   Default value: false
-   Location: Add to System Properties \[sys\_properties\] table.
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

 Depending on the property setting, IRE processes or skips the switch update:

-   **true**: IRE processes the CI updates, but doesn't process the CI switch reclassification update.
-   **false**: IRE processes the CI updates including the CI switch reclassification update.

</td></tr><tr><td>

glide.identification\_engine.reclassification\_restriction\_rules\_enabled

</td><td>

Globally enable or disable the application of active reclassification restriction rules.

 -   Type: true \| false
-   Default value: true
-   Location: Add to System Properties \[sys\_properties\] table.
-   Learn more: [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

</td></tr><tr><td>

Allow the update of an empty field by a lower priority data source.

 glide.reconciliation.override.null

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**

</td></tr><tr><td>

Controls how identification processes a small set of duplicate CIs.

 glide.identification\_engine.skip\_duplicates

</td><td>

-   Type: true \| false
-   Default value: true
-   Other values:
    -   **true**

If the number of duplicate CIs is less than the threshold specified by **glide.identification\_engine.skip\_duplicates.threshold**, then the oldest of the duplicate CIs is picked as a match and gets updated. That oldest CI is also designated as the main CI for that set of duplicate CIs.

For the rest of the duplicate CIs, the **duplicate\_of** field is set as a reference to the main CI.

    -   **false**

Matching a CI fails, and an error is logged.

-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**

</td></tr><tr><td>

Maximum number of CIs that can be in a set of duplicate CIs to allow identification to process the duplicate CIs according to the setting of **glide.identification\_engine.skip\_duplicates**.

 glide.identification\_engine.skip\_duplicates.threshold

</td><td>

If the number of duplicate CIs exceeds the threshold, then identification processes the duplicate CIs as if **glide.identification\_engine.skip\_duplicates** is set to false.

 -   Type: Integer
-   Default value: 5
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**

</td></tr><tr><td>

Maximum number of log runs that can be displayed when navigating to **Configuration** &gt; **Identification Logs**.

 glide.identification\_logs.max\_run\_ids

</td><td>

-   Type: integer
-   Default value: 1000
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**

</td></tr><tr><td>

glide.cache.size.service\_cache

</td><td>

Maximum cache size \(in MB\) that is used by the identification engine for inbound and outbound relations. When the limit is reached, the least recently used cached data is discarded, releasing space for new data.**Note:** You cannot disable the service cache.

 -   Type: Integer
-   Default value: 20
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.granular\_insert\_locking

</td><td>

Determines whether to use multiple granular insert locks or single global insert lock. Set to false if there are performance issues associated with the usage of multiple granular insert locks.

 -   Type: true \| false
-   Default value: true
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.batch\_update\_last\_discovered

</td><td>

Controls batch update of **last\_discovered** field in CIs that are being processed by the identification engine. Set to false if there are business rules that apply to the **last\_discovered** field, and you want to trigger these rules when calling an Identification and Reconciliation API.

 -   Type: true \| false
-   Default value: true
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.related\_items\_local\_cache\_count

</td><td>

For optimization, a custom number of locally cached query result entries of related/lookup items.

 -   Type: integer
-   Default value: 15000
-   Location: Add to System Properties \[sys\_properties\] table.

 **Note:** If there is a memory issue due to optimization related to using local cache, set the **glide.identification\_engine.related\_items\_local\_cache\_count** and the **glide.identification\_engine.dependent\_items\_local\_cache\_count** properties to 0.

</td></tr><tr><td>

glide.identification\_engine.dependent\_items\_local\_cache\_count

</td><td>

For optimization, a custom number of locally cached query result entries of dependent CIs.

 -   Type: integer
-   Default value: 10000
-   Location: Add to System Properties \[sys\_properties\] table.

 **Note:** If there is a memory issue due to optimization related to using local cache, set the **glide.identification\_engine.related\_items\_local\_cache\_count** and the **glide.identification\_engine.dependent\_items\_local\_cache\_count** properties to 0.

</td></tr><tr><td>

glide.identification\_engine.independent\_items\_local\_cache\_count

</td><td>

For optimization, a custom number of locally cached query result entries of independent CIs.

 -   Type: integer
-   Default value: 100000
-   Location: Add to System Properties \[sys\_properties\] table.

 Setting the value to 0 avoids using local cache for independent CIs which might affect performance.

</td></tr><tr><td>

glide.cmdb.logger.source.identification\_engine

</td><td>

Enable and configure what type of details the system logs when using IRE outside the scope of identification simulation. For example, when using an API, ECC queue or scheduled jobs.

 -   Type: string
-   Values: info, warn, error, debug, or debugVerbose
-   Location: Add to System Properties \[sys\_properties\] table.

**Note:** Depending on the setting, the system can generate large amounts of data that might affect overall system performance. Set the value with caution, and limit the level of details and use time to the minimum necessary for testing or debugging.

 For more troubleshooting information, see the [How to capture IRE \[identification and reconciliation engine\] debug logs \[KB0750382\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0750382) knowledge base article.

</td></tr><tr><td>

glide.identification\_engine.partial\_payload\_items\_max\_size

</td><td>

Maximum number of items allowed when creating a partial payload. When that limit is reached, the partial payload is split.

 For example, when IRE creates a partial payload, items and associated relations and references, are all merged in one partial payload. This merge could result in a large partial payload.

 Adjusting this property can help with performance issues related to IRE processing of partial items.

 -   Type: integer
-   Default: 1000
-   Learn more: [Identification and Reconciliation Engine \(IRE\)](../concept/ire.md)
-   Location: Add to System Properties \[sys\_properties\] table

</td></tr><tr><td>

glide.identification\_engine.partial\_items\_process\_limit

</td><td>

Maximum number of partial items to be fetched in a single IRE call. After reaching this limit, IRE fetches only partial items corresponding to complete items in the input payload.

 Adjusting the value can help with performance issues related to IRE processing of partial items.

 -   Type: integer
-   Default: 2000
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.partial\_items\_process\_absolute\_limit

</td><td>

Absolute limit of the number of partial items for IRE to fetch, after which, IRE stops fetching partial payloads from the CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\] table. Adjusting the value can help with performance issues related to IRE processing of partial items.

 -   Type: integer
-   Default: 5000
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.skip\_updating\_source\_last\_discovered\_if\_older

</td><td>

Determines how IRE updates the **last\_discovered** and the **discovery\_source** attributes in the CMDB.

-   true: If **last\_discovered** is provided in the payload and it is older than the **last\_discovered** of the CI in the CMDB, IRE does not use the payload values to update the **last\_discovered** and the **discovery\_source** attributes in the CMDB.
-   false: Even if the **last\_discovered** provided in the payload is older than the **last\_discovered** of the CI in the CMDB, IRE uses the payload values to update the **last\_discovered** and the **discovery\_source** attributes in the CMDB.

 **Note:** Only the attributes mentioned above are affected by this property in an update operation.

 -   Type: true \| false
-   Default: true
-   Learn more: [Identification and Reconciliation Engine \(IRE\)](../concept/ire.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.ire\_message\_listener\_skip\_updating\_source\_last\_discovered\_to\_now

</td><td>

If Robust Transform Engine \(RTE\) does not pass the **ire.skip\_updating\_last\_scan\_to\_now** custom property on the Robust Import Set Transformer form, IRE uses the value of this property for the **skip\_updating\_source\_last\_discovered\_to\_now** [IRE option](../concept/ire.md).

 -   Type: true \| false
-   Default: false
-   Learn more: [Identification and Reconciliation Engine \(IRE\)](../concept/ire.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.skip\_updating\_last\_scan\_if\_older

</td><td>

Determines how IRE uses the **source\_recency\_timestamp** value in a payload to determine whether to update the **last\_scan** attribute in the Source \[sys\_object\_source\] table.

-   true: If **source\_recency\_timestamp** is provided in the payload and it is older than the **last\_scan** of the CI in the CMDB, IRE does not update the **last\_scan** attribute in the Source \[sys\_object\_source\] table.
-   false: Even if the **source\_recency\_timestamp** provided in the payload is older than the **last\_scan** of the CI in the CMDB, IRE uses the payload value to update the **last\_scan** attribute in the Source \[sys\_object\_source\] table.

 You can check the input payload for a CI and the **last\_scan** attribute value in the Source \[sys\_object\_source\] table to learn if IRE will update that **last\_scan** value or not.

 **Note:** Only the attributes mentioned above are affected by this property in an update operation.

 -   Type: true \| false
-   Default: true
-   Learn more: [About mapping data columns to CMDB classes and attributes](../concept/create-etl-transform-map.md#) and [Identification and Reconciliation Engine \(IRE\)](../concept/ire.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.ire\_message\_listener\_skip\_updating\_last\_scan\_to\_now

</td><td>

If RTE does not pass the **ire.skip\_updating\_last\_scan\_to\_now** custom property on the Robust Import Set Transformer form, IRE uses the value of this property for the **ire.skip\_updating\_last\_scan\_to\_now** [IRE option](../concept/ire.md).

 -   Type: true \| false
-   Default: false
-   Learn more: [About mapping data columns to CMDB classes and attributes](../concept/create-etl-transform-map.md#) and [Identification and Reconciliation Engine \(IRE\)](../concept/ire.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.platform\_domain\_separation\_enabled

</td><td>

Toggles domain separation support mode during IRE processing.

-   false: IRE processes run only within the current domain. Basically disabling parent domains access to child domains during IRE processing.
-   true: IRE domain separation follows the platform domain separation behavior. Basically, enabling parent domains to look access into all its child domains during IRE processing.

 -   Type: true \| false
-   Default: false
-   Learn more: [Domain separation and CMDB Identification and Reconciliation](../concept/domain-separation-identification-reconciliation.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.enable\_identifier\_optional\_condition

</td><td>

Enables advanced options for regular identifier entries in identification rules. Those advanced options let you add conditions to narrow the set of records that will be searched for a matching CI.

**Note:**

This property affects only regular identifier entries \(it doesn't affect lookup or hybrid identifier entries\).

In the base system, identifier entries of various classes are pre-configured with advanced options conditions. All these pre-configured conditions in regular identifier entries will automatically apply when you set this property to **true**.

To prevent unexpected behavior, review those predefined conditions in regular identifier entries before setting this property to **true**. In the **Filter** box in the primary navigation, enter `cmdb_identifier_entry.list`. Then, in the Identifier Entry list view, review the 'Optional condition' column.

 -   Type: true \| false
-   Default: false
-   Learn more: [Create a CI identification rule](../task/t_CreateCIIdentificationRule.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.enable\_reconciliation\_filter\_before\_update

</td><td>

Determines whether filter conditions of a reconciliation rule are applied before a value change during payload processing, or after.

 -   Type: true \| false
-   Default: false
-   Learn more: [Create a static reconciliation rule](../concept/create-reconciliation-rule.md#), [Create a dynamic reconciliation rule](../concept/create-reconciliation-rule.md#)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.skip\_sys\_object\_source\_matching

</td><td>

Determines whether IRE identification processes have the priority in being used to uniquely identify CIs in a payload, over the use of **sys\_object\_source** lookup.

 When set to true, the system prioritizes sending any payload that contains a criterion attribute to be processed by IRE identification instead of using **sys\_object\_source** lookup. This can be useful in situation that can potentially generate duplicate CIs. For example, using sources in which identifying attributes are changing while the source native key isn't.

 However, when **source\_native\_key** is the only identifiable attribute \(for example, if none of the identification rules can run because attributes and values for rule identifiers aren't present in the payload\), then **source\_native\_key** is used for identification even when the property is set to **true**.

 -   Type: true \| false
-   Default: false
-   Learn more: [Identification and Reconciliation Engine \(IRE\)](../concept/ire.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled

</td><td>

Enables IRE behavior of creating de-duplication tasks for duplicate related items in a lookup table detected during a lookup-based identification.

 Set the property to reflect on whether such duplication is valid in the organization and doesn't require remediation, or isn't valid and the duplication should be remediated.

 -   Type: true \| false
-   Default: false
-   Learn more: [Detecting duplicate CIs](../concept/id-detect-dup-ci.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

glide.identification\_engine.dynamic\_ire\_enabled

</td><td>

Switch between using Dynamic IRE or Static IRE. Set to 'true' to use Dynamic IRE and to turn off Static IRE.

 -   Type: true \| false
-   Default: false
-   Learn more: [Dynamic IRE](../concept/dynamic-ire.md)
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr></tbody>
</table>