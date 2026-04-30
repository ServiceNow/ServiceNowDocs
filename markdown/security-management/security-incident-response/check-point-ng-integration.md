---
title: Check Point Next Generation Threat Prevention integration
description: This document describes the steps required to integrate Check Point Next Generation Threat Prevention \(NGTP\) capabilities with ServiceNow Security Incident Response \(SIR\) so that applications function properly together.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Check Point Next Generation Threat Prevention integration

This document describes the steps required to integrate Check Point Next Generation Threat Prevention \(NGTP\) capabilities with ServiceNow® Security Incident Response \(SIR\) so that applications function properly together.

Once installed and configured, the security incident analyst uses this integration to block malicious IP addresses, URLs, and Domains using Block Request List capabilities with the ServiceNow Security Incident Response \(SIR\) products. This Block Request List is configured on Check Point Gateways as a Custom Intelligence Feed. The Custom Intelligence Feeds feature provides an ability to add custom cyber intelligence feeds into the Next Generation Threat Prevention engine. It allows fetching feeds from a third-party server, in this case the ServiceNow Security Incident Response application, directly to the Check Point Next Generation Gateway to be enforced by Anti-Virus and Anti-Bot blades. The security incident response analyst creates entries for Check Point Block List from observables determined to be malicious on ServiceNow SIR security incidents.

For most implementations, a Block Request List is a csv file that is hosted on an external web server. For this integration, this web server is your ServiceNow AI Platform instance, which permits the Check Point next-generation Threat Prevention Engine to fetch the list of IP Addresses, URLs and Domains to be blocked.

To enforce the blocking observables on Check Point Gateway, ensure that Threat Prevention Policy is configured with Anti-Bot and Anti-Virus Blades activated. As the Block List entries are modified, the Threat Prevention Engine dynamically imports the list at the configured interval and enforces policy without a configuration change or a commit on the firewall. For this integration, ServiceNow AI Platform has created a table containing Block List entries that are retrieved by authorized Check Point next-generation Gateway at the configured retrieval intervals.

The integration includes the following features:

-   Flexibility to create multiple Block Lists that apply to multiple Check Point Gateways.
-   Detailed reporting on the types of sites being blocked \(phishing, malware, and allow listed sites\).
-   Tagging of ServiceNow AI Platform security incidents with Block List entries by the observable type \(URL, domain, IP address\).
-   Configuring Block List expiration periods to maintain Block List size by automatically expiring or removing older entries.
-   Searching Block List entries between different Block Lists.
-   Linking Block List entries to observable records and security incidents that include threat intelligence results and details about why an entry is blocked.

## Integration architecture diagram

Below is the high-level architecture diagram depicting the components involved and integration points between NOW Platform and Check Point Systems.

![Integration architecture](../image/integration-architecture.png)

**Note:** The Check Point Systems logo, Anti-Virus Blade image, and Anti Bot Blade image are from Check Point Systems ©. They are the Property of Check Point Systems.

## Plugins

The integration requires that the Security Incident Response \(com.snc.security\_incident\) plugin be activated.

To install Security Incident Response plugins:

1.  Log in to your instance with your HI credentials.
2.  Verify you have the administrator \(admin\) role.
3.  Navigate to System Definition&gt;plugins in your instance.
4.  Select and click Security Incident Response.

Once these plugins have been installed, you are able to upload the new Check Point integration plugin from the ServiceNow store and follow the following configuration instructions.

## Supported Check Point OS versions

This integration requires the Custom Intelligence Feed of Check Point and Anti-Bot and Anti-Virus blades. These are supported from R80.20 and higher. Install the hot fix of Custom Intelligence Feature known as Check Point R80.10 Jumbo HF take 121 and above. Refer to the Check Point Custom Intelligence Feed Documentation’s Installation section for more information on product compatibility matrix.

[https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit\_doGoviewsolutiondetails=&amp;solutionid=sk132193](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk132193)

After installing the hot fix, ensure that below commands are accessible on Check Point Gateway. SSH to the Gateway and login to expert mode.

![Commands available on the Check Point Gateway](../image/check-point-gateway-code.png)

## Supported ServiceNow versions

San Diego release version or later is supported.

## References

Below are some of the Check Point references which are useful in setting up the Pre-requisites.

1.  Custom Intelligence Feeds Feature - [https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit\_doGoviewsolutiondetails=&amp;solutionid=sk132193](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk132193)
2.  To set up Anti-Bot and Anti-Virus blades refer the Check Point User Guide. [http://downloads.checkpoint.com/dc/download.htm?ID=46534](http://downloads.checkpoint.com/dc/download.htm?ID=46534)
3.  To set up HTTPS Inspection on Check Point follow the link below. [https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit\_doGoviewsolutiondetails=&amp;solutionid=sk108202](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk108202)

## Permissions and roles

The following ServiceNow roles are required.

-   Administrator \(admin\) for installation of the integration application plugin
-   Security incident administrator \(sn\_si.admin\) for creating Block Lists in ServiceNow and approving requests for adding and deactivating Blocklist Entries.
-   Security analyst \(also referred to here as a SOC Analyst, sn\_si.analyst\) for creating and maintaining Block List Entry records.

For more information on assigning the security analyst role, on the [ServiceNow documentation website](https://servicenow.com/docs), navigate to Security operations&gt;Security Incident Response&gt; Assigning security analysts.

