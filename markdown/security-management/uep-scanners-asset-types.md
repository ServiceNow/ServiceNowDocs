---
title: Scanner integration exposures in unified exposure pipeline
description: For scanners configured using the unified exposure pipeline, provides information about the exposures that each integrated scanner updates in Unified Security Exposure Management \(USEM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/uep-scanners-asset-types.html
release: australia
topic_type: reference
last_updated: "2026-11-19"
reading_time_minutes: 2
breadcrumb: [Reference, Unified Security Exposure Management, Security Operations]
---

# Scanner integration exposures in unified exposure pipeline

For scanners configured using the unified exposure pipeline, provides information about the exposures that each integrated scanner updates in Unified Security Exposure Management \(USEM\).

<table><thead><tr><th>

Scanner

</th><th colspan="3">

Vulnerabilities

</th><th colspan="1">

Compliance/Policy findings

</th><th>

Asset information

</th></tr><tr><th>

Scanner integration

</th><th>

Host Vulnerabilities \(VIT\)Asset types: host, cloud, domain, vm\_image

</th><th>

Container Vulnerabilities \(CVIT\)Asset types: docker\_image

</th><th>

Application Vulnerabilities \(AVIT\)Asset types: code, scanned\_url

</th><th>

Configuration Test Results \(CTR\)Asset types: host, cloud, domain, vm\_image

</th><th>

Ingested asset types

</th></tr></thead><tbody><tr><td>

Akamai App Security

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

scanned\_url

</td></tr><tr><td>

Akamai Edge DNS

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

domain\_name

</td></tr><tr><td>

Armis Centrix

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Armis EASM

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

scanned\_url

</td></tr><tr><td>

Armis AppSec

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

Armis VMDR

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host

</td></tr><tr><td>

AWS Security Hub

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

host, cloud, docker\_image

</td></tr><tr><td>

Azure Cloud

</td><td>

No

</td><td>

 

</td><td>

 

</td><td>

Yes

</td><td>

cloud

</td></tr><tr><td>

Azure Devops

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

code

</td></tr><tr><td>

BigFix

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host

</td></tr><tr><td>

BitSight Security Ratings

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Black Duck

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

BrightSec

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Bugcrowd

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Burp Suite

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Checkmarx

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

Checkmarx One

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

Cisco DNA

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host

</td></tr><tr><td>

Cloudflare

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

domain\_name

</td></tr><tr><td>

Cortex Xpanse

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Coverity

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

CrowdStrike

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host, cloud

</td></tr><tr><td>

Crowdstrike Falcon Shield

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

cloud

</td></tr><tr><td>

Cycode

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td><td>

cloud, domain\_name, docker\_image, code

</td></tr><tr><td>

Cycognito

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

DigitSec

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

F5 Big IP

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host

</td></tr><tr><td>

GCP

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

cloud

</td></tr><tr><td>

GitHub

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

GitLab

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

docker\_image, code

</td></tr><tr><td>

Google Workspace

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Hacker One

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

cloud, domain\_name

</td></tr><tr><td>

Invicti

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

domain\_name, scanned\_url

</td></tr><tr><td>

Ionix

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Lacework

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

host, cloud, docker\_image

</td></tr><tr><td>

Mend io

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

MS Defender

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Nessus

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Nexpose

</td><td>

Yes

</td><td>

 

</td><td>

 

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Ninja One

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Orca

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td><td>

host, cloud, domain\_name, docker\_image, code

</td></tr><tr><td>

Palo Alto Cortex XDR

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Prisma

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

host, cloud, docker\_image

</td></tr><tr><td>

Qualys

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host, domain\_name

</td></tr><tr><td>

Rapid7 Insight VM

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host, domain\_name

</td></tr><tr><td>

Reco

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

cloud

</td></tr><tr><td>

RunZero

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host

</td></tr><tr><td>

Salt Security

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

domain\_name

</td></tr><tr><td>

Security Score Card

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

host, domain\_name, scanned\_url

</td></tr><tr><td>

Semgrep

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

Sentinel One

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host

</td></tr><tr><td>

ServiceNow

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

host, cloud, domain\_name

</td></tr><tr><td>

Sigrid

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

Snyk

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

docker\_image, code

</td></tr><tr><td>

Sonar Qube

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

code

</td></tr><tr><td>

Tanium

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Tenable io

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host, domain\_name

</td></tr><tr><td>

Tenable sc

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr><tr><td>

Upwind

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host, cloud

</td></tr><tr><td>

Veracode

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

domain\_name, code

</td></tr><tr><td>

Wiz

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

Yes

</td><td>

host, cloud, vm\_image, domain\_name, docker\_image

</td></tr><tr><td>

Zimperium

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

host

</td></tr></tbody>
</table>**Parent Topic:**[Unified Security Exposure Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/unified-security-exposure-management-reference.md)

