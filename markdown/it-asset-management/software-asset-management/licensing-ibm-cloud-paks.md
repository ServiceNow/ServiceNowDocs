---
title: Licensing for IBM Cloud Paks
description: When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Authorized SAM Provider \(IASP\) Program, the Software Asset Management application supports licensing rules for IBM Cloud Paks.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Licensing for IBM Cloud Paks

When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Authorized SAM Provider \(IASP\) Program, the Software Asset Management application supports licensing rules for IBM Cloud Paks.

An IBM Cloud Pak is a prepackaged set of IBM software products that can help you achieve a specific business goal. For example, the IBM Cloud Pak for Business Automation contains various IBM software products that automate business operations to help improve performance.

Each IBM Cloud Pak is licensed as a bundle using a supported IBM license metric, such as the Virtual Processor Core \(VPC\) license metric. However, you can determine the total number of rights that are required for a Cloud Pak based on the number of rights that are required for each software product within the Cloud Pak. These software products are also referred to as Bundled Programs. You can calculate the number of rights that are required for a Bundled Program by using a supported IBM license metric, such as the VPC and Resource Value Unit \(RVU\) license metrics. You must then use a corresponding conversion ratio to convert this number to the number of rights that are required for deploying the Bundled Program as part of the Cloud Pak. After you convert this number for each Bundled Program that you want to deploy, you can use the sum of the converted numbers to determine the total number of rights that are required for the Cloud Pak.

In the following example, a user wants to deploy various Bundled Programs as part of the IBM Cloud Pak for Integration:

|Bundled Program within the IBM Cloud Pak for Integration|Bundled Program to Cloud Pak ratio|Number of rights required for the Bundled Program|Number of rights required for deploying the Bundled Program as part of the Cloud Pak|
|--------------------------------------------------------|----------------------------------|-------------------------------------------------|------------------------------------------------------------------------------------|
|MQ Advanced|2 VPCs: 1 VPC|40|20|
|App Connect Enterprise|1 VPC: 3 VPCs|20|60|
|API Connect|1 VPC: 1 VPC|10|10|
|Datapower|1 VPC: 1 VPC|10|10|

Based on the conversion ratios and the number of rights that are required for each Bundled Program, you must license the Cloud Pak using a total of 100 rights.

See [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md) for more information on VPC licensing.

**Parent Topic:**[Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md)

