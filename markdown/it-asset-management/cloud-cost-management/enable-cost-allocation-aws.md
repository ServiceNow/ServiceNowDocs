---
title: Enable cost allocation in AWS for Kubernetes cluster
description: Enable cost allocation for a Kubernetes cluster in AWS Management Console before you run a AWS Billing download job to view the Kubernetes spend.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up access to AWS billing and usage data, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Enable cost allocation in AWS for Kubernetes cluster

Enable cost allocation for a Kubernetes cluster in AWS Management Console before you run a AWS Billing download job to view the Kubernetes spend.

## Before you begin

Role required: AWS Management Console administrator

-   You should be familiar with AWS policies.
-   Install Discovery and Service Mapping Patterns application \(sn\_itom\_pattern\) 1.10.2 or higher. For more information, see Install Discovery and Service Mapping Patterns.
-   Install CMDB CI Class Models \(sn\_cmdb\_ci\_class\) version 1.53.1 or higher. For more information, see CMDB CI Class Models app.
-   To set up Kubernetes discovery, see Kubernetes discovery using patterns.

## Procedure

1.  Log in to the [AWS Management Console](https://aws.amazon.com/console/).

2.  Search for and select **Cost Allocation Tags**.

3.  Select the **User-defined cost allocation tags** tab.

4.  Activate the following Kubernetes tags to appear in the billing data:

    -   Static Tag key
        -   aws:eks:cluster-name
        -   user:eks:cluster-name
        -   eks:cluster-name
    -   Dynamic Tag key
        -   kubernetes.io/cluster/&lt;Cluster-Name&gt;: shared/owned
        -   alpha.eksctl.io/cluster-name: &lt;Cluster-Name&gt;

## Result

The cost allocation for the selected Kubernetes cluster is enabled and you can view the Kubernetes spend.

