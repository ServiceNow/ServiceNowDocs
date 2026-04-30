---
title: Google API Credentials Form
description: Fill in the Google API Credentials form to configure the credentials.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Google Cloud Platform service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Google API Credentials Form

Fill in the Google API Credentials form to configure the credentials.

|Field|Description|
|-----|-----------|
|Name|Set a unique name for the Google Cloud API credentials.|
|Active|Option for enabling this credential for discovery. Select this check box to enable discovery.|
|Applies to|MID Server to which you apply the credentials. Select **All MID servers**.|
|Order|Order in which the platform runs this credential as it attempts to log in to devices. A smaller number indicates that the credential appears higher in the list. Establish the credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number, or none, the instance tries the credentials in a random order. The default value is 100.|
|Email|Your GCP email address.|
|Secret Key|Secret key that you generated on the Google Cloud Console.|
|Credential alias|A credential alias that is used by the credentials to authorize actions.|

**Parent Topic:**[Set up Google Cloud Platform service accounts](../../it-operations-management/concept/set-up-gcp-service-accounts.md)

