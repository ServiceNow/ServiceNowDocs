---
title: Configure digest token authentication for EMR Help
description: Configure ServiceNow single sign-on with Epic utilizing digest token authentication.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure digest token authentication for EMR Help

Configure ServiceNow single sign-on with Epic utilizing digest token authentication.

The ServiceNow instance receives a username and a digest token within an unencrypted HTTP Header from an Epic Hyperspace FDI Record. ServiceNow reads the HTTP header values and validates the digest token. If the digest token validates successfully, then the instance searches for a matching user credential in the User table. If there is a matching value, the user is logged in. If the digest token does not validate successfully or there is no matching user in the user table the user is redirected to a standard login page and no access is granted.

Digest Token Authentication with Epic Hyperspace/Hyperdrive requires:

-   A Generated encryption key unique to the Epic Hyperspace/Hyperdrive implementation
-   A script include or javascript library that can decrypt AES256
-   A configured Integration Record \(FDI\) in Hyperspace that will pass the user and digest token to the target instance in the URL parameter
-   A ServiceNow administrator
-   An Epic Analyst

For instructions on how to do this configuration, see the [How to Configure Digest Token Authentication for EMR Help with Epic Hyperspace and Hyperdrive \[KB1002504\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1002504) article in the Now Support Knowledge Base.

