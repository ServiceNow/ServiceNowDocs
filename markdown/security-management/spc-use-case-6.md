---
title: Security Posture Control use case: Detecting internet exposure of cloud assets  and high-risk combinations
description: It is critical to monitor potential internet exposure of Cloud assets \(virtual machines\) on various ports to ensure that vulnerabilities on these assets are not exploited remotely. This use case helps you identify these assets.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Security Posture Control, Security Operations]
---

# Security Posture Control use case: Detecting internet exposure of cloud assets  and high-risk combinations

It is critical to monitor potential internet exposure of Cloud assets \(virtual machines\) on various ports to ensure that vulnerabilities on these assets are not exploited remotely. This use case helps you identify these assets.

Security Posture Control permits you to evaluate the configuration of cloud assets to help you identify those assets that are internet-facing, that is, which assets are reachable from anywhere on the internet and from what ports they are exposed.

Security Posture Control combines these insights with security tool coverage gaps and vulnerability data from third-party scanners such as Qualys, Rapid7, or Tenable to identify high-risk combinations.

Currently, this use case supports AWS and requires the following pre-requisites.

1.  The Service Graph Connector for AWS is activated for the same AWS accounts that you have configured.
2.  You have activated one or more of the policies that are included with the product in Security Posture Control.
    -   Cloud assets with SSH port 22 open to internet.
    -   Cloud assets with SSH port 22 open to internet and missing endpoint protection.
    -   Cloud assets with HTTP port 80 open to internet and missing endpoint protection.
    -   Cloud assets with critical vulnerabilities and SSH port 22 open to internet \(Requires Vulnerability Response\).
    -   Cloud assets with critical vulnerabilities, missing endpoint protection and SSH port 22 open to internet \(Requires Vulnerability Response\).
    -   Cloud assets with HTTP ports open to internet, critical vulnerabilities, and missing endpoint protection \(Requires Vulnerability Response\).

