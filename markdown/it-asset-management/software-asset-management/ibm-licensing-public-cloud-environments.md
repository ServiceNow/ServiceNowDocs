---
title: IBM licensing in public cloud environments
description: When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Authorized SAM Provider \(IASP\) Program, the Software Asset Management application supports IBM licensing rules in public cloud environments.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Virtualization technologies and cloud platforms supported by IASP integrations, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM licensing in public cloud environments

When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Authorized SAM Provider \(IASP\) Program, the Software Asset Management application supports IBM licensing rules in public cloud environments.

A public cloud is a cloud computing model through which computing resources are owned and managed by a third-party cloud provider but shared by multiple clients via the Internet. Clients can access these shared computing resources through the virtual machines \(VMs\) that are running on virtual servers within each public cloud.

The Software Asset Management application supports sub-capacity processor value unit \(PVU\) and virtual processor core \(VPC\) licensing for IBM software products in public cloud environments. Supported public cloud providers include Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\).

With sub-capacity licensing in public cloud environments, you must license the virtual cores that are assigned to the cloud-based VMs on which you install and run an IBM software product. You can determine the total number of rights that are required for a license based on the sum of virtual cores that must be licensed across your cloud-based VMs. To determine the number of rights that are required for a PVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md).

**Important:** When determining the number of rights that are required for a PVU license used for VMs deployed in a public cloud environment, you must always use a standard PVUs per Core value of 70, regardless of which public cloud environment you choose.

**Parent Topic:**[Virtualization technologies and public cloud platforms supported by IBM Authorized SAM Provider \(IASP\) integrations](supported-virtualization-technologies-iasp-integrations.md)

