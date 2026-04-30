---
title: F5 certificate discovery
description: The ServiceNow Discovery application uses The F5-SSH-SSL Certification pattern extension to find all associated certificates on F5 load balancers that use IPv4 addresses, IPv6 addresses, or both.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# F5 certificate discovery

The ServiceNow® Discovery application uses **The F5-SSH-SSL Certification** pattern extension to find all associated certificates on F5 load balancers that use IPv4 addresses, IPv6 addresses, or both.

The **The F5-SSH-SSL Certification** pattern extension is part of the **F5 load balancer** and **F5 load balancer SSH** patterns that discover [F5 BIG-IP load balancer](../../discovery/concept/c_LoadBalancerF5BIGIP.md). The **The F5-SSH-SSL Certification** pattern extension discovers F5 load balancer instances running on the hosts via SNMP/SSH, and then discovers certifications used by the running node of the load balancer.

**Note:** For load balancers running IPv6, only SSH is supported.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## IPv6 support limitations

-   F5 SNMP is not supported.
-   MID Server cannot run REST APIs with IPv6.

    To run discovery with F5 REST, see [KB0864769](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0864769).


## Prerequisites

-   **Verify the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   **Verify the configuration of F5 load balancer**
    -   Ensure that F5 load balancer instances are up and running.
    -   Make sure the host \(that has the F5 instance running on it\) can discover successfully with the Discovery user credentials.
-   **Verify the configuration of Discovery**

    Ensure that the Discovery user added in the ServiceNow AI Platform instance can run the following commands:

<table id="table_h4p_1p3_2nb"><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`modify`

</td><td>

Modifies the TMSH components. You can modify one or more property settings in multiple components.The `modify` command uses the following option: `display-threshold pager`

</td></tr><tr><td>

`display_threshold`

</td><td>

Allows you to re-enable a `display-threshold` in your script.

</td></tr><tr><td>

`list`

</td><td>

Displays components that you have permission to view or are passed as arguments.The `list` command looks for the following arguments:

-   `ssl-cert`
-   `certificate-key-size`
-   `checksum`
-   `create-time`
-   `expiration-string`
-   `issuer`
-   `subject`
-   `version`
-   `fingerprint`
-   `serial-number`
-   `subject-alternative-name`
-   `size`


</td></tr></tbody>
</table>-   **Verify the configuration of the patterns**

    Make sure that the **F5-SSH-SSL Certification** shared library is added to the extension section of the **F5 Load Balancer** and **F5 Load Balancer SSH** patterns, in order to collect the certification attributes.


## F5 certificate discovery class model

![F5 certification discovery class model](../image/F5cert-classmodel.png)

## Data collected by Discovery during horizontal discovery

The discovered data includes the following tables and fields.

|Table and field|Description|
|---------------|-----------|
|Base Configuration Item Cluster \[cmdb\]|
|Serial number|Serial Number associated with the CI.|
|Configuration Item \[cmdb\_ci\]|
|operational\_status|Operational status of the cluster node.|
|Unique Certificate \[cmdb\_ci\_unique\_certificate\]|
|fingerprint|Hash value of the certificate.|
|fingerprint algorithm|Algorithm used to hash the certificate.|
|subject common name|Identifies the hostname/domain associated with the certificate.|
|subject distinguished name|Identifying information of the subject.|
|issuer distinguished name|Distinguished name of the issuer.|
|comments| |
|renewal tracking|Indicates whether to create any priority 1 or priority 3 tasks for the expiring certificates.|
|issuer common name|Common name of the issuer.|
|valid From|Validity start period of the certificate.|
|serial Number|Serial Number associated with the CI.|
|subject country|The subject's two letter country code.|
|subject organization|Subject’s organization.|
|Version|X.509 version of the certificate.|
|Issuer|Entity that signed and issued the certificate.|
|subject organizational unit|Subject's organizational unit.|
|subject alternative name|List of fully qualified domain names secured by the certificate.|
|valid to|Validity end period of the certificate.|
|name| |
|State|Lifecycle states of the certificate.|
|root issuer|Root entity that signed and issued the immediate certificate.|
|key size|Size of the key used by the signing algorithm.|
|subject locality|Subject's locality.|
|subject state|Subject's state.|

## CI relationships

The **The F5-SSH-SSL Certification** pattern extension does not create any CI relationships.

**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

