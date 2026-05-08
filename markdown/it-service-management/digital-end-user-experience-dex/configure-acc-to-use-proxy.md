---
title: Configure ACC to use a proxy for all traffic
description: Configure the Agent Client Collector \(ACC\) to use a proxy for all traffic by setting environment variables. Using a proxy helps you enhance security, monitor and control internet usage, improve performance through caching, protect privacy, and enforce compliance with your organization's policies.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Configure ACC to use a proxy for all traffic

Configure the Agent Client Collector \(ACC\) to use a proxy for all traffic by setting environment variables. Using a proxy helps you enhance security, monitor and control internet usage, improve performance through caching, protect privacy, and enforce compliance with your organization's policies.

## Before you begin

Consider the following aspects before configuration.

-   Ports, protocols, and firewall/proxy configurations required to enable ACC to reach the ServiceNow cloud
-   Network-based security tools \(IDS, proxy, SSL interception, NAC\) that might block ACC connectivity
-   DNS resolution and routing for stable connectivity and failover support
-   Support of WebSockets by the proxy
-   Firewall rules that prohibit access to ITOM gateway

Role required: admin

## About this task

Proxy setup is needed in the following use cases:

-   You're using ACC for DEX or ACC-V without a MID Server.
-   You must route traffic through an internal proxy to reach the ServiceNow cloud.

## Procedure

1.  Run diagnostics to verify that the endpoint can reach ServiceNow before making changes.

<table id="choicetable_onx_ylc_1fc"><thead><tr><th align="left" id="d348933e113">

Option

</th><th align="left" id="d348933e116">

Command

</th></tr></thead><tbody><tr><td id="d348933e122">

**Windows**

</td><td>

PowerShell: `.\servicenow-net-check.ps1`

</td></tr><tr><td id="d348933e134">

**macOS**

</td><td>

```
# See if DNS resolution succeeds
nslookup itomcnc-prod-gateway-amer.sncapps.service-now.com

# See if you can ping ITOM cloud services
ping -c 5 itomcnc-prod-gateway-amer.sncapps.service-now.com

# See if you can establish a TCP connection
nc -zv itomcnc-prod-gateway-amer.sncapps.service-now.com 443

# See if you can make a HTTP request to the ServiceNow install server
curl -i https://install.service-now.com/

```

</td></tr></tbody>
</table>2.  Open the acc.yml file from the following location.

    |Option|Path|
    |------|----|
    |**Windows**|`C:\ProgramData\ServiceNow\agent-client-collector\config`|
    |**macOS**|`/Library/Application\ Support/servicenow/agent-client-collector/config`|

3.  In acc.yml with a version of ACC greater than 4.3.0, set the proxy as shown in the following example:

    `https-proxy: "http://intproxy0.your-corp.com:8080"`

4.  Set up proxy authentication by setting the user name and password in the environment variable itself:

    `HTTPS_PROXY="http://username:password@intproxy0.your-corp.com:8080"`

5.  Set the NO\_PROXY environment using a comma-separated list of hosts to not proxy.

    For example, `localhost`.

6.  Test connectivity using a proxy server with mTLS used by ITOM Cloud Services.

    You need the following files from your local endpoint:

    -   `cacert.pem` - Certificate Authority certificate file used to validate the server identity \(downloaded from ServiceNow with openssl\)
        -   Windows:

            ```
            openssl s_client -showcerts -connect itomcnc-prod-gateway-amer.sncapps.service-now.com:443 <NUL | findstr /B /C:"-----BEGIN CERTIFICATE-----" /C:"-----END CERTIFICATE-----" > cacert.pem
            ```

        -   macOS:

            ```
            openssl s_client -showcerts -connect itomcnc-prod-gateway-amer.sncapps.service-now.com:443 </dev/null | sed -ne '/-BEGIN CERTIFICATE-/,/-END CERTIFICATE-/p' > cacert.pem
            ```

    -   `cnc_chain.crt` - client certificate file to present to the server for mutual TLS authentication \(`agent-client-collector/cert/cnc`\).
    -   `priv_key.pem` - private key associated with the client certificate \(`agent-client-collector/cert/cnc`\).
7.  Fetch assets using a proxy with mTLS.

    ```
    # Will attempt to fetch an asset used by ACC-V using a proxy. The file is not saved.
    # Remember, replace intproxy0.your-corp.com:8080 with your internal host and port.
    curl -v --proxy http://intproxy0.your-corp.com:8080 --cacert cacert.pem --cert cnc_chain.crt --key priv_key.pem --request GET --output NUL https://itomcnc-prod-gateway-amer.sncapps.service-now.com:443/content/v1/assets/afaa52edc32f7150f640f2ff050131c8/a4ef65d00adbab1659f460f8d4e311d8db65f519994f63d176951ce1e0297e08
    
    ```

8.  Inspect the output of the cURL to see if the command succeeded using the proxy.


**Parent Topic:**[Advanced configuration](../concept/dex-advanced-configuration.md)

