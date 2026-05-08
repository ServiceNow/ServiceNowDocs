---
title: Configure CI reclassification during IRE processing
description: During the Identification and Reconciliation Engine \(IRE\) CI identification process, a CI might need to be reclassified to a different sys\_class\_name type. By default, CIs are reclassified automatically. If automatic reclassification is disabled, then the CI is not reclassified and the system generates a reclassification task for your review.Reduce data loss during IRE processing by preventing a CI class change for specific source and target classes. A reclassification restriction rule affects only the Class attribute and does not prevent the update to the rest of the CI properties.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure CI reclassification during IRE processing

During the Identification and Reconciliation Engine \(IRE\) CI identification process, a CI might need to be reclassified to a different sys\_class\_name type. By default, CIs are reclassified automatically. If automatic reclassification is disabled, then the CI is not reclassified and the system generates a reclassification task for your review.

The class of a CI can be upgraded, downgraded, or switched to a different branch in the class hierarchy. For more details about reclassification operations, see [Reclassify a CI](../task/t_ManuallyReclassifyCI.md). You can use system properties and payload flags to configure the IRE behavior of CI reclassification, globally or individually per CI.

**Note:** CI reclassification is possible only between two classes that have identical identification rules.

## Configure automatic CI reclassification using system properties

You can use system properties to configure system-wide IRE behavior for CI reclassification. For information about CI reclassification-related properties, including access, see [Properties for Identification and Reconciliation](../reference/properties-id-reconciliation.md).

-   The following properties enable or disable automatic reclassification updates that are specified in a payload. These properties are set to **true** in the base system, enabling processing of CI updates, including CI reclassification updates.

    To disable any automatic reclassification update, set the respective property to **false**. In that case, IRE rejects a payload \(or a payload item in Enhanced IRE\) with the respective reclassification updates, and creates a [reclassification task](../task/t_ViewReclassificationTask.md).

    -   **glide.class.upgrade.enabled**
    -   **glide.class.downgrade.enabled**
    -   **glide.class.switch.enabled**
-   The following properties enable IRE to process CI updates with reclassification operations. However, depending on the property setting, IRE processes or skips the reclassification update. These properties are set to **false** in the base system, in which case IRE processes CI updates including any CI reclassifications.

    Set a property to **true** to configure IRE to process CI updates but not the CI respective reclassification update.

    -   **glide.identification\_engine.update\_without\_switch\_enabled**
    -   **glide.identification\_engine.update\_without\_downgrade\_enabled**
    -   **glide.identification\_engine.update\_without\_upgrade\_enabled**
    This set of properties takes precedence over the previous set of properties \(glide.class.&lt;reclassification&gt;.enabled\). For example, with the following conflicting property settings, the second property takes precedence over the first:

    -   **glide.class.downgrade.enabled** = **false**
    -   **glide.identification\_engine.update\_without\_downgrade\_enabled** = **true**

Example for IRE processing of a payload item with a switch of a CI from Linux Server to Window Server. With the following default property settings in the base system, IRE updates the attributes including the class switch:

-   **glide.class.switch.enabled** = **true**
-   **glide.identification\_engine.update\_without\_switch\_enabled** = **false**

However, with the following property settings, IRE updates the attributes but skips the class switch:

-   **glide.class.switch.enabled** = **true**
-   **glide.identification\_engine.update\_without\_switch\_enabled** = **true**

## Configure automatic CI reclassification in input payloads

You can use flags which correspond to the system properties, in the input payload of the CreateOrUpdateCIEnhanced\(\) or the createOrUpdateCI\(\)​ APIs. In the payload, set these flags to **true** or **false** to temporarily override the respective system property settings, at the payload item level.

For the following payload flags that control reclassification behavior, if any is set, the setting has precedence regardless of the setting of the corresponding **glide.class.xxx.enabled** property:

-   `classUpgrade`
-   `classDowngrade`
-   `classSwitch`

For the following payload flags that control reclassification behavior, the system checks if either the flag or its corresponding **glide.identification\_engine.update\_xxx\_enabled** property is true to allow the update without the respective reclassification operation:

-   `updateWithoutUpgrade`
-   `updateWithoutDowngrade`
-   `updateWithoutSwitch`

Also, you can pass payload level settings \(which apply to all items within a payload\), per data source, by specifying CI reclassification properties on the Robust Import Set Transformers form. For more information, see Robust import set transformer properties.

The following sample JSON payload enables automatic reclassification for the specified CI:

```
{ items: [{className: 'cmdb_ci_server', classUpgrade: true, classDowngrade: true, classSwitch: true, values: {name: 'linux123', serial_number: '12srt567', ip_address: '10.2.3.4'}, }]}
```

## Reclassification restriction rules

Prevent IRE from downgrading or switching a CI class during payload processing to help prevent data loss. A reclassification restriction rule prevents a CI class change for specific source and target classes, while still processing any other property updates for the CI.

You can use a reclassification restriction rule, for example, to prevent a CI class downgrade from **cmdb\_ci\_linux\_server** \(source class\) to **cmdb\_ci\_server** \(target class\). Or, to prevent a CI class switch from Linux Server to Windows Server. Reclassification restriction rules can be useful when using a Service Graph Connector which might lead to a class downgrade or switch, and a potential loss of important data.

To control the application of reclassification restriction rules:

-   Use the **glide.identification\_engine.reclassification\_restriction\_rules\_enabled** system property to globally enable or disable the application of active reclassification restriction rules. This property is set to **true** by default.
-   Use the **skipReclassificationRestrictionRules** payload flag in an IRE payload to prevent the application of active reclassification restriction rules.

    For example, a payload with the **skipReclassificationRestrictionRules** flag:

    ```
    {
      "items": [
        {
          "className": "cmdb_ci_server",
          "values": {
            "short_description": "Linux server description",
            "name": "Linux Server 1"
          },
          "settings": {
            "skipReclassificationRestrictionRules": "true"
          }
        }
      ]
    }
    ```


For information about how to create a reclassification restriction rule, see [Create a reclassification restriction rule](c_CIReclassification.md#).

**Parent Topic:**[Configuring CMDB Identification and Reconciliation](configuring-ire.md)

## Create a reclassification restriction rule

Reduce data loss during IRE processing by preventing a CI class change for specific source and target classes. A reclassification restriction rule affects only the **Class** attribute and does not prevent the update to the rest of the CI properties.

### Before you begin

Role required: sn\_cmdb\_admin or itil\_admin \(sn\_cmdb\_editor and itil have read access only\)

### About this task

If during IRE processing of a payload, a CI needs to be reclassified \(downgrade or switch class\), IRE checks reclassification restriction rules. If any reclassification restriction rule applies to the current CI reclassification, IRE processes the CI properties update, but skips the CI reclassification.

IRE output provides specific details about any processing related to reclassification restriction rules.

A reclassification restriction rule applies only to the direction between the specified source and the target classes. The rule doesn't prevent a reclassification in the opposite direction, from the specified target class to the source class. To restrict reclassification between two classes in both directions, specify two separate reclassification restriction rules, one for each direction.

### Procedure

1.  Enter `cmdb_ire_reclassification_restriction.list` in the filter navigator.

2.  Fill out the Reclassification Restriction form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the reclassification restriction rule.|
    |Source table|Current CI class.|
    |Source inheritance|Whether to apply the reclassification restriction rule to child classes of **Source table**.|
    |Target class|Reclassification target class.|
    |Target inheritance|Whether to apply the reclassification restriction rule to child classes of **Target table**.|
    |Type|CI reclassification type: **Downgrade** or **Switch**.|

3.  Click **Submit**.


### What to do next

In the Reclassification Restrictions list view, you can activate or deactivate a reclassification restriction rule by setting its **Active** value to true or false.

