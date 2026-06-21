---
title: Configure additional properties in the Edge Encryption properties file
description: After installing the Edge Encryption proxy server in your network and setting up your keystore and keys, configure the additional Edge Encryption properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/edge-encryption/set-props.html
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure additional properties in the Edge Encryption properties file

After installing the Edge Encryption proxy server in your network and setting up your keystore and keys, configure the additional Edge Encryption properties.

## Before you begin

Role required: admin

## Procedure

1.  Open the `<installation directory>/conf/edgeencryption.properties` file and configure the following Edge Encryption proxy server properties:

    -   [Target \(instance\) properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption-proxy-server-properties.md)
    -   [User account properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption-proxy-server-properties.md)
    -   [Proxy properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption-proxy-server-properties.md)
    -   If using order preserving encryption types or encryption patterns, configure the [Proxy database properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption-proxy-server-properties.md)
    -   [Clear text and static IV properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-encryption-proxy-server-properties.md)
2.  Save and close the file.


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/manual-proxy-install.md)

**Previous topic:**[Configure encryption keys on the instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/t_RotateEncryptionKeys.md)

**Next topic:**[Configure a web proxy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/t_SetUpWebProxyProperties.md)

