---
title: Target tables for scanner integrations in unified exposure pipeline
description: For scanners configured using unified exposure pipeline, provides information about the impacted target tables in Unified Security Exposure Management \(USEM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/uep-scanners-target-tables.html
release: brazil
topic_type: reference
last_updated: "2026-11-19"
reading_time_minutes: 6
breadcrumb: [Reference, Unified Security Exposure Management, Security Operations]
---

# Target tables for scanner integrations in unified exposure pipeline

For scanners configured using unified exposure pipeline, provides information about the impacted target tables in Unified Security Exposure Management \(USEM\).

|Scanner|Scanner inputs|Finding tables|Asset tables|
|-------|--------------|--------------|------------|
|Akamai App Security|Web app vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|Akamai Edge DNS|Domain name assets|NA|Discovered item|
|Armis Centrix|Host vulnerabilities, host misconfigurations|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|Armis EASM|Web app vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|Armis VA|Host vulnerabilities|Vulnerable Item Detection, Vulnerable Item|Discovered item|
|AWS Security Hub|Cloud misconfigurations, host vulnerabilities, container vulnerabilities, serverless vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Container Image Finding, Container Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Container Image\)|
|Azure Cloud|Cloud misconfigurations|Configuration Test, Test Result|Discovered item|
|BitSight Security Ratings|Web app vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|Black Duck|Code package vulnerabilities \(SCA\)|Application Vulnerable Item|Discovered Item \(Application\)|
|BMC Client Management|Host assets only|NA|Discovered item|
|BrightSec|Web app vulnerabilities \(DAST\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Bugcrowd|Web app vulnerabilities \(bug bounty\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Burp Suite|Web app vulnerabilities \(DAST\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Checkmarx|Code vulnerabilities \(SAST\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Checkmarx One|Code vulnerabilities \(SAST\), IaC misconfigurations, code package vulnerabilities \(SCA\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Cisco DNA Center|Host vulnerabilities|Vulnerable Item Detection, Vulnerable Item|Discovered item|
|Cloudflare|Domain name assets only|NA|Discovered item|
|Cortex Xpanse|Web app vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|Coverity|Code vulnerabilities \(SAST\)|Application Vulnerable Item|Discovered Item \(Application\)|
|CrowdStrike Falcon|Host vulnerabilities, cloud misconfigurations|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|CrowdStrike Falcon Shield|Cloud and SaaS misconfigurations|Configuration TestTest Result|Discovered item|
|Cycode|Cloud misconfigurations, code vulnerabilities \(SAST\), container vulnerabilities, web app vulnerabilities, IaC misconfigurations, code package vulnerabilities \(SCA\)|Container Image Finding, Container Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered itemDiscovered Item \(Container Image\), Discovered Item \(Application\)|
|CyCognito|Web app vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|Cylance|Host assets only|NA|Discovered item|
|DigitSec|Code vulnerabilities \(SAST\), IaC misconfigurations, code package vulnerabilities \(Salesforce\)|Application Vulnerable Item|Discovered Item \(Application\)|
|F5 BIG-IP|Host assets only|NA|Discovered item|
|GCP|Cloud misconfigurations|Configuration Test, Test Result|Discovered item|
|GitHub|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|Application Vulnerable Item|Discovered Item \(Application\)|
|GitLab|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\), container vulnerabilities|Container Image Finding, Container Vulnerable Item, Application Vulnerable Item|Discovered item, Discovered Item \(Container Image\), Discovered Item \(Application\)|
|Gitleaks|Code vulnerabilities \(secrets\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Google Workspace|Host misconfigurations \(device posture\), users|Configuration Test, Test Result|Discovered item|
|HackerOne|Cloud misconfigurations, host vulnerabilities, code vulnerabilities, web app vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Application\)|
|HCL AppScan Cloud|AppSec findings, brokered via Synqly and mapped through OCSF|Application Vulnerable Item\(assumed\)|Discovered Item \(Application\)\(assumed\)|
|Invicti|Web app vulnerabilities \(DAST\)|Application Vulnerable Item|Discovered Item \(Application\)|
|IONIX|Cloud misconfigurations, web app vulnerabilities|Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Application\)|
|Lacework|Cloud misconfigurations, host misconfigurations, host vulnerabilities, container vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Container Image Finding, Container Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Container Image\)|
|Mend.io|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Microsoft Defender|Host vulnerabilities, host misconfigurations|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|Moose \(display name "Armis AppSec"\)|Cloud misconfigurations, code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Application\)|
|Nessus|Host vulnerabilities|Vulnerable Item Detection, Vulnerable Item|Discovered item|
|Nexpose|Host vulnerabilities|Vulnerable Item Detection, Vulnerable Item|Discovered item|
|NinjaOne|Host vulnerabilities|Vulnerable Item Detection, Vulnerable Item|Discovered item|
|Onapsis|Host vulnerabilities, host misconfigurations \(SAP layer\)|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|OpenText \(Fortify\)|Findings brokered via Synqly and mapped through OCSF|Application Vulnerable Item\(assumed\)|Discovered Item \(Application\)\(assumed\)|
|Orca|All nine categories: cloud misconfigurations, host misconfigurations, host vulnerabilities, code vulnerabilities, container vulnerabilities, web app vulnerabilities, IaC misconfigurations, code package vulnerabilities, serverless vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Container Image Finding, Container Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Container Image\), Discovered Item \(Application\)|
|Palo Alto Cortex XDR|Host vulnerabilities, host misconfigurations|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|Panorays|Web app vulnerabilities \(third-party risk\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Prisma Cloud|Cloud misconfigurations, host misconfigurations, host vulnerabilities, code vulnerabilities, container vulnerabilities, web app vulnerabilities, IaC misconfigurations, serverless vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Container Image Finding, Container Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Container Image\), Discovered Item \(Application\)|
|Qualys|Host vulnerabilities, host misconfigurations, web app vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Application\)|
|Rapid7 InsightVM|Host vulnerabilities, host misconfigurations, web app vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Application\)|
|Reco|Cloud and SaaS misconfigurations|Configuration Test, Test Result|Discovered item|
|runZero|Host assets only|NA|Discovered item|
|Salt Security|Web app and API vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|SecurityScorecard|Host vulnerabilities, web app vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Application Vulnerable Item|Discovered item, Discovered Item \(Application\)|
|Semgrep|Code vulnerabilities \(SAST\)|Application Vulnerable Item|Discovered Item \(Application\)|
|SentinelOne|Host vulnerabilities|Vulnerable Item Detection, Vulnerable Item|Discovered item|
|Sigrid|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|Application Vulnerable Item|Discovered Item \(Application\)|
|Snyk|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\), container vulnerabilities, IaC misconfigurations|Container Image Finding, Container Vulnerable Item, Application Vulnerable Item|Discovered Item \(Container Image\), Discovered Item \(Application\)|
|SonarQube|Code vulnerabilities \(SAST\), IaC misconfigurations|Application Vulnerable Item|Discovered Item \(Application\)|
|Tanium|Host vulnerabilities, host misconfigurations|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|Tenable IO|Host vulnerabilities, host misconfigurations, cloud misconfigurations, web app vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Application\)|
|Tenable SC|Host vulnerabilities, host misconfigurations|Vulnerable Item Detection, Vulnerable Item, Configuration Test, Test Result|Discovered item|
|Upwind|Cloud misconfigurations, host vulnerabilities, container vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Container Image Finding, Container Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Container Image\)|
|Veracode|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\), web app vulnerabilities|Application Vulnerable Item|Discovered Item \(Application\)|
|Wiz|Cloud misconfigurations, host misconfigurations, host vulnerabilities, code vulnerabilities, container vulnerabilities, code package vulnerabilities, serverless vulnerabilities|Vulnerable Item Detection, Vulnerable Item, Container Image Finding, Container Vulnerable Item, Application Vulnerable Item, Configuration Test, Test Result|Discovered item, Discovered Item \(Container Image\), Discovered Item \(Application\)|
|Zafran|Severity and exploitability enrichment on existing findings, no findings of its own|NA|NA|
|Zimperium|Host vulnerabilities, code vulnerabilities \(mobile\)|Vulnerable Item Detection, Vulnerable Item, Application Vulnerable Item|Discovered item, Discovered Item \(Application\)|

**Parent Topic:**[Unified Security Exposure Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/unified-security-exposure-management-reference.md)

