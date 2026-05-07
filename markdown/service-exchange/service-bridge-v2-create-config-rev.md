---
title: Create configuration revisions
description: As a provider, you can edit and create revisions of entitlements that contain updated functionality that can be developed and deployed to consumers.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Create configuration revisions

As a provider, you can edit and create revisions of entitlements that contain updated functionality that can be developed and deployed to consumers.

When the new revision is deployed, consumers can either activate and use the new revision, or continue to use the old revision. The new revision can be activated only if the consumer is using a Service Exchange application version that is compatible with the Service Exchange application version compatibility set on the revision. If the consumers want to use the new revision, they must upgrade their Service Exchange application to the minimum compatibility that is set on the configuration.

## Configuration revision life cycle

A configuration can be one of the following:

-   Remote task definition
-   Remote record producer

**Note:** The following sections describe the various stages in the configuration revision life-cycle of a remote task definition. You can:

-   [Create a configuration revision](service-bridge-v2-create-config-rev.md#section_l2g_psf_tbc)
-   [Archive a configuration revision](service-bridge-v2-create-config-rev.md#section_zjw_2qc_sbc)
-   [Retire a configuration](service-bridge-v2-create-config-rev.md#section_x1w_dqc_sbc)
-   [Copy a configuration revision](service-bridge-v2-create-config-rev.md#section_gst_43n_tbc)
-   [Delete a configuration](service-bridge-v2-create-config-rev.md#section_igy_2jn_tbc)

You can follow the same process to create revisions for a remote record producer.

## Create a configuration revision

1.  Navigate to the **All** &gt; **Service Exchange Provider** &gt; **Remote task definitions**.
2.  Select the remote task definition for which you want to create a configuration revision.

    **Note:** The remote task definition that you select must be in the **Published** state.

    ![Service Exchange Remote Task Definition](../image/service-bridge-v2-remote-task-defn1.jpg)

    Note the **Compatibility** field. This field shows the Service Exchange version that is being used by the provider. If the consumer is using a compatible Service Exchange version, data can be synced between the provider and consumer instances. But if the consumer isn’t using a compatible version, any new entitlements can’t be activated until the corresponding Service Exchange version is upgraded. See [Mismatched version support](service-bridge-v2-mismatch-version.md) for additional information.

3.  Select **Checkout**.
4.  A new revision of the configuration is created and the State is set to **In Draft**.

    ![Revisions related list for a Service Exchange](../image/service-bridge-v2-revision-rel-list.jpg)

    You can view the older revision by navigating to the Revisions tab under the Related List section. As you can see in the preceding image, the older revision is still in the **Published** state.

5.  Make the necessary changes and select **Save** to save the changes. Select **Publish** to activate the newly created configuration revision. The newly activated revision is synced to the consumer instance. The State of the older revision is set to **Inactive**.

    **Note:** The inactive configuration is still available to the consumers and data synchronization will continue until this configuration is either archived or retired.

6.  On the consumer instance, navigate to **Service Exchange Consumer** &gt; **Provider Connections**. You can see the newly published configuration revision under the Entitlements tab in the Related Links section.![Configuration revisions entitled to consumer](../image/service-bridge-v2-config-rev-entitle.jpg)
7.  Select the newly published configuration reference and select the **Entity reference** link to navigate to the Remote task definition page.
8.  Select **Activate** to activate the new configuration revision. When the new revision is activated, the earlier revision moves to an **Inactive** state. Consumers can continue to use the earlier revision until it’s archived or retired.
9.  You can create multiple configuration revisions for a single configuration but only the latest published revision is active and can be used by the consumers.

    **Note:**

    -   If you create a configuration revision and select **Save**, the revision is set to the **Draft** state. If you open the **Published** revision of this configuration, you’ll notice that the **Checkout** and **Retire** options are unavailable. In this case, you must open the draft version to make any changes.
    -   If the newly created draft revision isn’t required, select **Cancel** to delete that draft revision. The already published revision is available to **Checkout** or **Retire**.

## Archive a configuration revision

You can archive an inactive configuration revision. When a revision is archived by the provider, it’s deactivated and the State is set to **Archived** on the consumer instance. The following steps describe how to archive a remote task definition configuration revision. The same process is applicable to the remote record producers and foundation data sync offerings.

1.  Navigate to the **All** &gt; **Service Exchange Provider** &gt; **Remote task definitions**.
2.  Select a remote task definition in the list.
3.  Navigate to the **Revisions** tab in the Related List.
4.  Select the inactive revision that you want to the archive.
5.  Click **Archive** to deactivate the remote task definition. Once archived, this revision is no longer available to consumers.

    **Note:** You can’t Publish, Update, or Checkout an archived configuration revision. You can use the **Copy** option to make a copy of the configuration.


## Retire a configuration

You can retire a published configuration. When you retire a configuration, the entire set of revisions associated with the configuration are retired. To retire a configuration, follow these steps:

1.  Navigate to the **All** &gt; **Service Exchange Provider** &gt; **Remote task definitions**.
2.  Select a remote task definition configuration on the list.
3.  Select **Retire** and then select **OK**. Once retired, this configuration is no longer available to consumers.

    **Note:** This option retires published and inactive configuration revisions. But configuration revisions in the **Archived** state aren’t retired.

4.  If you want to use the remote task definition again, you can:
    -   Select **Checkout** to create a new configuration revision.
    -   Select **Copy** to make a duplicate copy of the new configuration.

## Copy a configuration revision

You can make a duplicate copy of a configuration revision that is one of the following states:

-   Published
-   Inactive
-   Archived
-   Retired

1.  Navigate to the **All** &gt; **Service Exchange Provider** &gt; **Remote task definitions**.
2.  Select a remote task definition configuration revision that is in any of the preceding states.
3.  Select **Copy** to make a copy of the configuration revision.

## Delete a configuration

You can delete a configuration that has been retired. There may be many retired revisions present but the **Delete** option is available only for the latest retired configuration revision. When a revision is deleted, the entire configuration set is deleted.

1.  Navigate to the **All** &gt; **Service Exchange Provider** &gt; **Remote task definitions**.
2.  Select a remote task definition that is in the **Retired** state.
3.  Select **Delete** to delete the configuration if it’s no longer required. Once deleted, all records associated with this identity are deleted and can’t be undone.

