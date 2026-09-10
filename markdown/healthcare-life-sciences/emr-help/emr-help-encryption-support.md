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

By default, the EMR Help application encrypts the following fields \(columns\) by using the **sn\_ind\_rmt\_help.emr\_data** encryption module, a Key Management Framework \(KMF\) crypto module that uses the AES-256 algorithm:

-   The **Additional Info** field in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table.
-   The **Phone number** and **Email address** fields in the EMR Incident Data \[sn\_ind\_rmt\_help\_incident\_data\] table.

The **emr\_data\_viewer** module access policy grants the sn\_ind\_rmt\_help.viewer role permission to decrypt and view these encrypted fields. Users without the sn\_ind\_rmt\_help.viewer role see the encrypted values.

Field Encryption capabilities are required. For more information, see [Activate Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/activate-platform-encryption.md).

**Parent Topic:**[EMR Help reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/healthcare-life-sciences/emr-help/emr-reference.md)

