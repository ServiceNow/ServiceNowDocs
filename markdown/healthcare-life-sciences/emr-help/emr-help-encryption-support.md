---
title: Encryption options in EMR Help
description: EMR Help provides encryption support to secure sensitive information.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Encryption options in EMR Help

EMR Help provides encryption support to secure sensitive information.

Encryption prevents unauthorized users from viewing sensitive EMR system data.

The following encryption options on the ServiceNow AI Platform are supported in the EMR Help application:

-   [Column Level Encryption](emr-help-encryption-support.md#section_v2g_g2x_cpb)
-   [Column Level Encryption Enterprise](emr-help-encryption-support.md#section_htr_f2x_cpb)

## Column Level Encryption

Column Level Encryption \(CLE\), is a built-in feature which permits encryption in encryption modules. The CLE plugin \(com.glide.encryption\) that enables the encryption of table columns and attachments associated with an EMR system in a service request is activated by default when your administrator installs the EMR Help application.

Once the CLE plugin \(com.glide.encryption\) is activated, set up an encryption module and associate it with the required roles that use the EMR Help application. You can encrypt tables or fields \(columns within a table\) but encryption is most useful for columns in the data table for request parameters that are marked as sensitive data.

By default, the **rmt\_help\_data\_view** encryption module associated with the sn\_ind\_rmt\_help\_viewer role is available for use with the EMR Help application. In addition, the **Additional Info** field \(column\) in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table and **Phone number** and **Email address** fields \(columns\) in the EMR Incident Data \[sn\_ind\_rmt\_help\_incident\_data\] table are encrypted by default.

To learn more, see [Field Encryption](https://www.servicenow.com/docs/access?context=field-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Column Level Encryption Enterprise

Column Level Encryption Enterprise provides an enhanced encryption capability and utilizes the Key Management Framework \(KMF\). For using the Column Level Encryption Enterprise option with the EMR Help application, your administrator must activate the plugin \(com.glide.now.platform.encryption\). As an administrator, you can choose to opt in to use CLE with KMF. For more information, see [Activate Column Level Encryption Enterprise](https://www.servicenow.com/docs/access?context=activate-platform-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Beginning with the Quebec release, the migration of keys and encrypted data from Encryption Support to Column Level Encryption is automated using scheduled jobs. For more information, see [Migrating to Column Level Encryption Enterprise](https://www.servicenow.com/docs/access?context=migration-to-platform-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

**Note:** Existing customers on the Paris release must contact ServiceNow Customer Support to migrate keys and encrypted data from Encryption Support to Column Level Encryption Enterprise.

