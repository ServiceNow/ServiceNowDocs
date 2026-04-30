---
title: Feature mapping for Oracle Database options and management packs
description: The Software Asset Management application automatically maps discovered Oracle features to the Oracle Database options and management packs that they’re associated with. These mappings can help you determine the usage and license compliance of your database options and management packs.If a discovered feature is associated with more than one Oracle Database option or management pack, you can change the database option or management pack that the feature usage data is applied to by updating the default mapping for that feature.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Oracle Database options and management packs, Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Feature mapping for Oracle Database options and management packs

The Software Asset Management application automatically maps discovered Oracle features to the Oracle Database options and management packs that they’re associated with. These mappings can help you determine the usage and license compliance of your database options and management packs.

Every Oracle Database option and management pack contains a set of features that enhance the capabilities of the Oracle Database. For example, the Oracle Active Data Guard option provides real-time data protection and availability for Oracle Database using features such as automatic block repair, global data services, and application continuity. For more information on the features that are supported by each database option and management pack, refer to the [Oracle documentation](https://docs.oracle.com/en/).

When you run a discovery, the ServiceNow® Discovery application locates and identifies both the database options and management packs that are installed in your Oracle environment and the features that are associated with them. This data is then sent to the Software Asset Management application, where it can be normalized and reconciled.

After the data is normalized, the Software Asset Management application uses the Oracle Feature Option Mapping \[samp\_feature\_option\_mapping\] table to map your features to the appropriate database options and management packs at the database instance level. Any subsequent usage data that you retrieve for each feature via the SAM - Evaluate database option usage from Oracle GLAS data scheduled job can then be applied to the mapped database options and management packs. The Software Asset Management application uses this data with predefined database option and management pack usage rules to determine which database options and management packs are being used on each database instance. The resulting usage information is included in the Oracle reconciliation process to help you determine the license compliance of your database options and management packs.

**Parent Topic:**[Oracle Database options and management packs](../reference/oracle-options.md)

## Update the default mapping for a feature

If a discovered feature is associated with more than one Oracle Database option or management pack, you can change the database option or management pack that the feature usage data is applied to by updating the default mapping for that feature.

### Before you begin

Role required: admin

### About this task

Oracle features can be associated with multiple database options and management packs. However, the Software Asset Management application can map each feature to only one database option or management pack at a time.

The Software Asset Management application automatically maps each discovered feature to an appropriate database option or management pack based on default mappings that have been predefined for each feature. Usage data for each feature can then be applied to the mapped database options and management packs to help you determine if they are in use.

If any of your discovered features are associated with more than one database option or management pack, you can update the default mappings for those features based on how you are using each feature and what entitlements you have purchased for the associated database options and management packs. By updating the default mappings for those features, you can change the database options and management packs that the corresponding feature usage data is applied to, thereby enabling you to better optimize the license compliance positions of your database options and management packs based on your organization's needs.

**Note:** You can update the default mappings only for features that are associated with multiple database options and management packs.

### Procedure

1.  On the page header of your ServiceNow instance, select **All**.

2.  In the menu navigation filter, enter `samp_option_for_feature_inuse.list`.

    The Default option for feature in use list opens. This list displays the default mappings for all discovered features that are currently in use and can be mapped to more than one database option or management pack.

3.  From the list of available features, select the feature that you want to change the default mapping for.

4.  From the **Default database option in use** drop-down on the Default option for feature in use form, select the database option or management pack that you want to map the feature to.

    **Note:** The **Default database option in use** drop-down is automatically filtered to display only the database options and management packs that the selected feature is associated with.

5.  Select **Update**.

    You automatically return to the Default option for feature in use list, which displays the new default mapping.


### What to do next

To activate the new default mapping, you must run the SAM - Evaluate database option usage from Oracle GLAS data scheduled job. You can either run the job on-demand or wait for the next scheduled job. After the job completes successfully, usage data for the specified feature can then be applied to the newly mapped database option or management pack.

