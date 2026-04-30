---
title: Create Oracle API credentials
description: Create Oracle API credentials on the ServiceNow AI Platform to enable access to your Oracle resources during Oracle discovery.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Oracle API credentials]
breadcrumb: [Set up Oracle Cloud infrastructure \(OCI\) service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Create Oracle API credentials

Create Oracle API credentials on the ServiceNow AI Platform to enable access to your Oracle resources during Oracle discovery.

## Before you begin

Verify that your OCI user has at least read-only access to all Oracle services. For information on access permissions, consult your system administrator.

Retrieve the following properties from the Oracle Cloud Console:

-   Tenancy Oracle Cloud Identifier \(Tenancy OCID\)
-   User OCID
-   Key fingerprint
-   Private key

For instructions on retrieving these properties, go to the [Oracle Help Center](https://docs.oracle.com/en/) and search for the "Required Keys and OCIDs" article.

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials**.

2.  Select **New**.

3.  Select **Oracle API Credentials**.

4.  On the form, fill in the fields with the property values you retrieved.

    |Field|Value|
    |-----|-----|
    |Name|Unique and descriptive name for the Oracle credentials.|
    |Active|Option to select to use the credential.|
    |Tenancy Id|Oracle Cloud Identifier \(OCID\) for your tenancy.|
    |User Id|OCID of the OCI user.|
    |Key Fingerprint|Fingerprint of the public key.|
    |Private Key|RSA private key that is used for API signing authentication.|

5.  Select **Submit**.


## What to do next

Create OCI service accounts. For more information, see [Create OCI service accounts](create-oci-service-accounts.md).

**Parent Topic:**[Set up Oracle Cloud infrastructure \(OCI\) service accounts](../concept/set-up-oracle-cloud-infrastructure-oci-service-accounts.md)

