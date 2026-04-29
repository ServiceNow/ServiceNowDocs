---
title: AWS shapes support in the Enterprise Modeling and Visualization
description: Enterprise Modeling and Visualization supports Amazon Web Services \(AWS\) shape libraries for modeling cloud architectures. These shapes enable architects to design future-state cloud diagrams aligned with CMDB and CSDM standards.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Enterprise Modeling and Visualization in the EA Workspace, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# AWS shapes support in the Enterprise Modeling and Visualization

Enterprise Modeling and Visualization supports Amazon Web Services \(AWS\) shape libraries for modeling cloud architectures. These shapes enable architects to design future-state cloud diagrams aligned with CMDB and CSDM standards.

## AWS shapes mapping with ServiceNow Common Service Data Model \(CSDM\)

Mapping AWS shapes to ServiceNow CMDB and Common Service Data Model \(CSDM\) ensures:

-   Operationalization of cloud diagrams: AWS architecture diagrams in EA Workspace can directly link to CMDB records.
-   Governance and compliance: Aligns AWS resources with workflows for approvals and audits.
-   End-to-end traceability: Connects AWS infrastructure to business capabilities and applications in CSDM.

|AWS shape|CSDM mapped entity|
|---------|------------------|
|AWS Account|Cloud Service Account|
|Region or Availability Zone|AWS Datacenter|
|Amazon VPC|Network Service CI|
|EC2 Instance|Virtual Machine Instance|
|Auto Scaling Group|Compute Cluster CI|
|Amazon S3|Cloud Object Storage|
|RDS Instance|Cloud Database|
|Lambda Function|Cloud Function|
|API Gateway|Application Gateway CI|
|Security Group / NACL|Security Policy CI|

**Parent Topic:**[Exploring Enterprise Modeling and Visualization in the EA Workspace](eaw-modeling.md)

**Related topics**  


[Amazon Web Services \(AWS\) shapes](../../reference/eaw-reference/eaw-modeling-aws-shapes.md)

[Working with Amazon Web Services \(AWS\) shapes](eaw-work-with-aws-shapes.md)

[Create a diagram using AWS shapes](../../task/eaw-task/eaw-modeling-create-diagram-aws.md)

