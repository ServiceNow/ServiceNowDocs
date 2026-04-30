---
title: Discovery for cloud environment
description: ITOM Visibility cloud discovery solutions enable you to collect detailed information about your cloud-based infrastructure and your resources in major cloud service providers: Amazon Web Services \(AWS\), Microsoft Azure, Google Cloud Platform \(GCP\), IBM Cloud Platform, Oracle Cloud Infrastructure \(OCI\), and Alibaba Cloud.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for cloud environment

ITOM Visibility cloud discovery solutions enable you to collect detailed information about your cloud-based infrastructure and your resources in major cloud service providers: Amazon Web Services \(AWS\), Microsoft Azure, Google Cloud Platform \(GCP\), IBM Cloud Platform, Oracle Cloud Infrastructure \(OCI\), and Alibaba Cloud.

ITOM Visibility cloud discovery can be understood through the layers at which discovery operates and the methods used to perform discovery. Different methods or combination of methods at the different layers support various business outcomes, giving you the flexibility to customize your discovery approach to your organization's specific needs.

## Business outcomes

Effective cloud discovery is crucial for maintaining an accurate and up-to-date inventory of cloud resources. This comprehensive visibility into the cloud infrastructure enables organizations to drive several key business outcomes. It empowers informed decision-making, accelerates innovation by optimizing resource allocation, and helps cloud investments align directly with strategic business objectives.

|Business outcome|Cloud discovery role|
|----------------|--------------------|
|Regulatory compliance|Provides the necessary visibility and data to support regulatory compliance mandates.|
|SAM \(software asset management\)|Enables more effective software asset management by providing comprehensive visibility into cloud software deployments.|
|FinOps \(financial operations\)|Provides comprehensive visibility into cloud resources and their usage, enabling FinOps teams to optimize cloud spend across cloud providers, organizations, and cost centers.|
|SecOps \(security operations\)|Offers continuous visibility into cloud resources and their configurations, supporting the security and compliance of cloud environments.|
|Certificate management|Discovers and tracks certificates, their expiry, and usage, enabling teams to reduce the risk of certificate-related outages and assess potential business impact.|
|AIOps \(artificial intelligence for IT operations\)|Identifies and maps cloud resources, their configurations, and interdependencies. Cloud discovery provides the foundational data for AIOps platforms to monitor proactively, analyze, and predict potential issues, ultimately reducing outage risks and supporting business continuity.|

For more information on which cloud discovery methods best support each business outcome, see the **Matching methods to business outcomes** section.

## Cloud discovery layers

To achieve these business outcomes, you need to understand how cloud discovery works. Cloud discovery can be understood in two distinct layers: the cloud metadata \(or topology\) layer and the operating system \(OS\) layer. Each layer provides a different level of visibility into cloud infrastructure, from structural inventory to a detailed operational state. Think of it like mapping a neighborhood versus inspecting individual buildings.

The cloud metadata layer provides a high-level view of cloud infrastructure by outlining its structural components. This outline includes identifying resources like virtual machines, networks, and subnets, effectively creating an inventory of what exists. It’s similar to mapping all the buildings in a neighborhood, showing how everything is organized and interconnected. This layer helps to understand the overall architecture and resource relationships within a cloud environment.

The OS layer reveals the internal state of cloud resources, including installed software, active services, running processes, and system configurations. It’s like stepping inside each building in a neighborhood to inspect its internal setup. This deeper level of discovery helps monitor operations, verify configurations, and maintain compliance and security across environments.

These layers can be discovered through the different cloud discovery methods and together, the two layers enable comprehensive visibility from structural inventory to detailed operational insights.

## Cloud discovery methods

ITOM Visibility supports several methods for cloud discovery, depending on the layer. Different discovery methods address different organizational needs and constraints.

-   Cloud metadata layer: Pattern-based Cloud Discovery and Service Graph Connectors
-   OS layer: IP-based Horizontal Discovery, Agent Client Collector for Visibility - Content, and Service Graph Connectors

**Note:** The pattern-based Cloud Discovery and IP-based Horizontal Discovery methods operate at different layers but both use the Discovery and Service Mapping Patterns application.

-   **Pattern-based Cloud Discovery/IP-based Horizontal Discovery**

    The Discovery and Service Mapping Patterns application supports both cloud metadata and OS layer discovery. Patterns execute commands in a pull-based, scheduled approach by targeting devices within specified IP ranges. Key characteristics include:

    -   Requires OS and application credentials
    -   Needs firewall access from a MID Server
    -   Works with AWS, Azure, GCP, OCI, Alibaba Cloud, and IBM clouds
    -   Supports continuous visibility for AWS, Azure, and GCP
    For more information, see [Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md).

-   **Agent Client Collector for Visibility - Content**

    An agent-based, push-based cloud discovery that provides near real-time discovery and supports OS layer discovery. Key characteristics include:

    -   Supports deployment with or without a MID Server
    -   Doesn't require OS-level credentials
    -   Works on Windows, Linux, and macOS
    -   Uses system accounts, local service accounts, or Microsoft gMSA
    -   Supports OS layer discovery only
    -   Works with AWS, Azure, and GCP
    For more information, see [Agent Client Collector for Visibility](../../agent-client-collector/concept/acc-visibility-landing-page.md).

-   **Service Graph Connectors**

    Third-party connectors that perform scheduled imports by pulling data directly from cloud provider APIs. Service Graph Connectors support both cloud metadata and limited OS layer discovery. Key characteristics include:

    -   Requires read access to the provider's system
    -   Doesn't require OS credentials or MID Server firewall access
    -   Works with AWS, Azure, and GCP
    -   Supports continuous visibility for AWS
    For more information, see [Integrating third-party data into CMDB](https://www.servicenow.com/docs/access?context=cmdb-third-party-integrations&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


Each method has its own requirements and supports different use cases, depending on the cloud provider. For more information, see:

-   AWS: [AWS cloud discovery methods and use cases](../../it-operations-management/reference/aws-discovery-methods-use-case.md)
-   Azure: [Azure cloud discovery methods and use cases](../../it-operations-management/reference/azure-discovery-methods-use-case.md)
-   GCP: [GCP cloud discovery methods and use cases](../../it-operations-management/reference/gcp-discovery-methods-use-case.md)

For a list of AWS, Azure, and GCP resources discovered by Discovery and Service Mapping Patterns and Service Graph Connectors, see [Cloud discovery solutions comparison](../../it-operations-management/concept/cloud-discovery-methods-comparison.md).

## Continuous visibility

Beyond choosing a cloud discovery method, you must also consider when and how often discovery occurs. Cloud environments are highly dynamic, with resources constantly being created, modified, or deleted. Traditional scheduled discovery often fails to keep up with these rapid changes, leading to a stale and inaccurate CMDB. Continuous visibility addresses this challenge by capturing changes as they happen in the cloud. There are two main types of continuous visibility: pull-based and push-based.

In pull-based discovery, the ServiceNow instance connects to cloud providers at set intervals to retrieve and update CMDB data. This approach promotes regular synchronization and offers more frequent updates than traditional scheduled scans. The pattern-based Cloud Discovery method supports this approach for both Azure and GCP.

In push-based discovery, the cloud environment itself is configured to send change events directly to the ServiceNow instance. This approach enables near real-time updates to the CMDB. Both Service Graph Connectors and the pattern-based Cloud Discovery method support push-based discovery for AWS.

**Note:** Continuous visibility for Amazon AWS Cloud, Microsoft Azure Cloud, and Google Cloud Platform doesn’t require Cloud Provisioning and Governance.

For more information, see:

-   Azure: [Microsoft Azure Alert driven discovery](../../it-operations-management/concept/microsoft-azure-alert-driven-discovery.md#)
-   GCP: [Configure the Google Cloud Logging service to auto-update the CMDB](../../it-operations-management/task/gcp-stackdriver-service.md)
-   AWS: [AWS events-driven discovery](../../it-operations-management/concept/aws-events-driven-discovery.md)

## Choosing methods for desired business outcomes

Choosing the right discovery methods at the cloud metadata and OS layers for your desired business outcomes is essential for optimizing your configuration management strategy and achieving operational goals.

Cloud metadata layer discovery methods support the following business outcomes:

|Business outcomes|Pattern-based Cloud Discovery|Service Graph Connectors|
|-----------------|-----------------------------|------------------------|
|Regulatory compliance|Yes|Yes|
|Basic AIOps|Yes|Yes|
|Continuous visibility|AWS, Azure, and GCP|AWS only|

OS layer discovery methods support the following business outcomes:

|Business outcomes|IP-based Horizontal Discovery|Agent Client Collector for Visibility - Content|Service Graph Connectors|
|-----------------|-----------------------------|-----------------------------------------------|------------------------|
|Regulatory compliance|Full|Full|Limited|
|SAM|Enterprise|Enterprise|Basic|
|FinOps|Yes|Yes|No|
|SecOps|Yes, including file-based discovery|Yes, including file-based discovery|No|
|Certificate management|Yes|Yes|No|
|AIOps|Full|Full|Limited|
|Oracle GLAS \(Global Licensing Advisory Services\) audits|Yes|Yes|No|
|Hibernating or autoscaling resource visibility|No|Yes|No|

## Managing your cloud resources

Discovery Admin Workspace provides a centralized location for managing and monitoring discovery operations, including performance monitoring, issue diagnosis, and maintaining configuration accuracy. From tracking schedules and diagnosing errors to tuning configurations and accessing insights, Discovery Admin Workspace integrates key tools to improve efficiency and visibility. You can identify critical tasks, manage discovery processes, and resolve issues with enhanced diagnostics and reporting. For more information, see [Discovery Admin Workspace](discovery-admin-workspace.md).

