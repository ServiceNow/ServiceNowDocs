---
title: Encryption options in EMR Help
description: EMR Help provides encryption support to secure sensitive information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/emr-help/emr-help-encryption-support.html
release: zurich
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 1
breadcrumb: [Reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Encryption options in EMR Help

EMR Help provides encryption support to secure sensitive information.

Encryption prevents unauthorized users from viewing sensitive EMR system data.

The following encryption options on the ServiceNow AI Platform are supported in the EMR Help application:

-   [Column Level Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/emr-help-encryption-support.md)
-   [Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/emr-help-encryption-support.md)

## Column Level Encryption

Column Level Encryption \(CLE\) encrypts individual columns \(fields\) and attachments associated with an EMR system in a service request. Encryption is most useful for columns in the data table for request parameters that are marked as sensitive data.

By default, the EMR Help application encrypts the following fields \(columns\) by using the **sn\_ind\_rmt\_help.emr\_data** encryption module, a Key Management Framework \(KMF\) crypto module that uses the AES-256 algorithm:

-   The **Additional Info** field in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table.
-   The **Phone number** and **Email address** fields in the EMR Incident Data \[sn\_ind\_rmt\_help\_incident\_data\] table.

The **emr\_data\_viewer** module access policy grants the sn\_ind\_rmt\_help.viewer role permission to decrypt and view these encrypted fields. Users without the sn\_ind\_rmt\_help.viewer role see the encrypted values.

## Column Level Encryption Enterprise

Column Level Encryption Enterprise provides an enhanced encryption capability and utilizes the Key Management Framework \(KMF\). For using the Column Level Encryption Enterprise option with the EMR Help application, your administrator must activate the plugin \(com.glide.now.platform.encryption\). As an administrator, you can choose to opt in to use CLE with KMF. For more information, see [Activate Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/activate-platform-encryption.md).

Beginning with the Quebec release, the migration of keys and encrypted data from Encryption Support to Column Level Encryption is automated using scheduled jobs. For more information, see [Migrating to Column Level Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/migration-to-platform-encryption.md).

**Note:** Existing customers on the Paris release must contact ServiceNow Customer Support to migrate keys and encrypted data from Encryption Support to Column Level Encryption Enterprise.

**Parent Topic:**[EMR Help reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/emr-reference.md)

