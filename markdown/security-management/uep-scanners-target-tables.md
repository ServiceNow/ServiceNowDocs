---
title: Target tables for scanner integrations in unified exposure pipeline
description: For scanners configured using unified exposure pipeline, provides information about the impacted target tables in Unified Security Exposure Management \(USEM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/uep-scanners-target-tables.html
release: australia
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 4
breadcrumb: [Reference, Unified Security Exposure Management, Security Operations]
---

# Target tables for scanner integrations in unified exposure pipeline

For scanners configured using unified exposure pipeline, provides information about the impacted target tables in Unified Security Exposure Management \(USEM\).

|Scanner|Scanner inputs|Target finding tables|Target asset tables|
|-------|--------------|---------------------|-------------------|
|Akamai App Security|Web app vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Akamai Edge DNS|Domain name assets|NA|`sn_sec_cmn_src_ci`|
|Armis Centrix|Host vulnerabilities, host misconfigurations|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|Armis EASM|Web app vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Armis VA|Host vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`|`sn_sec_cmn_src_ci`|
|AWS Security Hub|Cloud misconfigurations, host vulnerabilities, container vulnerabilities, serverless vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`|
|Azure Cloud|Cloud misconfigurations|`sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|BitSight Security Ratings|Web app vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Black Duck|Code package vulnerabilities \(SCA\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|BMC Client Management|Host assets only|NA|`sn_sec_cmn_src_ci`|
|BrightSec|Web app vulnerabilities \(DAST\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Bugcrowd|Web app vulnerabilities \(bug bounty\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Burp Suite|Web app vulnerabilities \(DAST\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Checkmarx|Code vulnerabilities \(SAST\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Checkmarx One|Code vulnerabilities \(SAST\), IaC misconfigurations, code package vulnerabilities \(SCA\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Cisco DNA Center|Host vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`|`sn_sec_cmn_src_ci`|
|Cloudflare|Domain name assets only|NA|`sn_sec_cmn_src_ci`|
|Cortex Xpanse|Web app vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Coverity|Code vulnerabilities \(SAST\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|CrowdStrike Falcon|Host vulnerabilities, cloud misconfigurations|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|CrowdStrike Falcon Shield|Cloud and SaaS misconfigurations|`sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|Cycode|Cloud misconfigurations, code vulnerabilities \(SAST\), container vulnerabilities, web app vulnerabilities, IaC misconfigurations, code package vulnerabilities \(SCA\)|`sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`, `sn_vul_app_release`|
|CyCognito|Web app vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Cylance|Host assets only|NA|`sn_sec_cmn_src_ci`|
|DigitSec|Code vulnerabilities \(SAST\), IaC misconfigurations, code package vulnerabilities \(Salesforce\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|F5 BIG-IP|Host assets only|NA|`sn_sec_cmn_src_ci`|
|GCP|Cloud misconfigurations|`sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|GitHub|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|GitLab|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\), container vulnerabilities|`sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vul_app_vulnerable_item`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`, `sn_vul_app_release`|
|Gitleaks|Code vulnerabilities \(secrets\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Google Workspace|Host misconfigurations \(device posture\), users|`sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|HackerOne|Cloud misconfigurations, host vulnerabilities, code vulnerabilities, web app vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|HCL AppScan Cloud|AppSec findings, brokered via Synqly and mapped through OCSF|`sn_vul_app_vulnerable_item` \(assumed\)|`sn_vul_app_release` \(assumed\)|
|Invicti|Web app vulnerabilities \(DAST\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|IONIX|Cloud misconfigurations, web app vulnerabilities|`sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|Lacework|Cloud misconfigurations, host misconfigurations, host vulnerabilities, container vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`|
|Mend.io|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Microsoft Defender|Host vulnerabilities, host misconfigurations|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|Moose \(display name "Armis AppSec"\)|Cloud misconfigurations, code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|`sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|Nessus|Host vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`|`sn_sec_cmn_src_ci`|
|Nexpose|Host vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`|`sn_sec_cmn_src_ci`|
|NinjaOne|Host vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`|`sn_sec_cmn_src_ci`|
|Onapsis|Host vulnerabilities, host misconfigurations \(SAP layer\)|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|OpenText \(Fortify\)|Findings brokered via Synqly and mapped through OCSF|`sn_vul_app_vulnerable_item` \(assumed\)|`sn_vul_app_release` \(assumed\)|
|Orca|All nine categories: cloud misconfigurations, host misconfigurations, host vulnerabilities, code vulnerabilities, container vulnerabilities, web app vulnerabilities, IaC misconfigurations, code package vulnerabilities, serverless vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`, `sn_vul_app_release`|
|Palo Alto Cortex XDR|Host vulnerabilities, host misconfigurations|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|Panorays|Web app vulnerabilities \(third party risk\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Prisma Cloud|Cloud misconfigurations, host misconfigurations, host vulnerabilities, code vulnerabilities, container vulnerabilities, web app vulnerabilities, IaC misconfigurations, serverless vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`, `sn_vul_app_release`|
|Qualys|Host vulnerabilities, host misconfigurations, web app vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|Rapid7 InsightVM|Host vulnerabilities, host misconfigurations, web app vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|Reco|Cloud and SaaS misconfigurations|`sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|runZero|Host assets only|NA|`sn_sec_cmn_src_ci`|
|Salt Security|Web app and API vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|SecurityScorecard|Host vulnerabilities, web app vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_app_vulnerable_item`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|Semgrep|Code vulnerabilities \(SAST\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|SentinelOne|Host vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`|`sn_sec_cmn_src_ci`|
|Sigrid|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\)|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Snyk|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\), container vulnerabilities, IaC misconfigurations|`sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vul_app_vulnerable_item`|`sn_vul_container_image`, `sn_vul_app_release`|
|SonarQube|Code vulnerabilities \(SAST\), IaC misconfigurations|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Tanium|Host vulnerabilities, host misconfigurations|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|Tenable IO|Host vulnerabilities, host misconfigurations, cloud misconfigurations, web app vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|
|Tenable SC|Host vulnerabilities, host misconfigurations|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`|
|Upwind|Cloud misconfigurations, host vulnerabilities, container vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`|
|Veracode|Code vulnerabilities \(SAST\), code package vulnerabilities \(SCA\), web app vulnerabilities|`sn_vul_app_vulnerable_item`|`sn_vul_app_release`|
|Wiz|Cloud misconfigurations, host misconfigurations, host vulnerabilities, code vulnerabilities, container vulnerabilities, code package vulnerabilities, serverless vulnerabilities|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_container_image_findings`, `sn_vul_container_image_vulnerable_item`, `sn_vul_app_vulnerable_item`, `sn_vulc_test`, `sn_vulc_result`|`sn_sec_cmn_src_ci`, `sn_vul_container_image`, `sn_vul_app_release`|
|Zafran|Severity and exploitability enrichment on existing findings, no findings of its own|NA|NA|
|Zimperium|Host vulnerabilities, code vulnerabilities \(mobile\)|`sn_vul_detection`, `sn_vul_vulnerable_item`, `sn_vul_app_vulnerable_item`|`sn_sec_cmn_src_ci`, `sn_vul_app_release`|

**Parent Topic:**[Unified Security Exposure Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/unified-security-exposure-management-reference.md)

