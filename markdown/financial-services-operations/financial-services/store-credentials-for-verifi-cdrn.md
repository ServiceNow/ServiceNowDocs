---
title: Storing credentials for Verifi CDRN
description: Credential storage information for securely managing Issuer ID and Shared Secret values for Financial Services Operations Integration with Verifi.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/store-credentials-for-verifi-cdrn.html
release: australia
product: Financial Services
classification: financial-services
topic_type: reference
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Configure the Authentication Profile, Configure, Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Storing credentials for Verifi CDRN

Credential storage information for securely managing Issuer ID and Shared Secret values for Financial Services Operations Integration with Verifi.

|Credential|Suggested Store Key|Notes|
|----------|-------------------|-----|
|UAT Issuer ID|verifi.cdrn.uat.issuer\_id|Numeric string, e.g. "11743".|
|UAT Shared Secret|verifi.cdrn.uat.secret|32-character string; keep separate from Production.|
|Production Issuer ID|verifi.cdrn.prod.issuer\_id|Different value from UAT.|
|Production Shared Secret|verifi.cdrn.prod.secret|Different value from UAT.|

**Parent Topic:**[Configure the Authentication Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configure-the-authentication-profile.md)

