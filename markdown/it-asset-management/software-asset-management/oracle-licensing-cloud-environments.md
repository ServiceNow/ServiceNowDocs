---
title: Oracle licensing in cloud environments
description: The Software Asset Management application supports licensing rules for Oracle Database and WebLogic Server \(Standard, Enterprise, and Suite Editions\) in cloud environments.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle licensing in cloud environments

The Software Asset Management application supports licensing rules for Oracle Database and WebLogic Server \(Standard, Enterprise, and Suite Editions\) in cloud environments.

**Important:** The Software Asset Management application supports Bring Your Own License \(BYOL\) for Oracle Database and WebLogic Server across hybrid infrastructures. With BYOL support, you can track licenses for your Oracle Database and WebLogic Server in both on-premise and public cloud environments. For more information about Oracle BYOL support, see [Bring your own license or subscription to the public cloud](byol-concepts.md).

When you install or run an Oracle Database or WebLogic Server in the cloud, you can license it using either the Named User Plus or Per Processor license metric. In addition, the WebLogic Server licensing support covers the entire WebLogic product family that includes the Standard, Enterprise, and Suite editions. For more information, refer to this knowledge base article [KB2630167](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2630167).

**Note:** For Oracle WebLogic applications version 12 or later, the software edition won't be discovered. For WebLogic applications, on the Software installation form, manually set the **Edition Override** field to Standard, Enterprise, or Suite.

-   The Named User Plus license metric licenses all users and physical devices that access an Oracle cloud database or WebLogic Server.
-   The Per Processor license metric licenses the virtual CPUs \(vCPUs\) on which you install or run an Oracle cloud database or WebLogic Server.

**Note:** The Oracle Processor Core Factor Table is not applicable in cloud environments.

## Amazon Web Services \(AWS\)

AWS is a cloud computing platform on which you can install and run Oracle databases and WebLogic servers. You can manage your Oracle databases on AWS using either Amazon Elastic Compute Cloud \(EC2\) or Amazon Relational Database Service \(RDS\). However, you can manage your Oracle WebLogic servers using only Amazon Elastic Compute Cloud \(EC2\). For more information on Amazon EC2, refer to the [Amazon Elastic Compute Cloud documentation](https://docs.aws.amazon.com/ec2/index.html). For more information on Amazon RDS, refer to the [Amazon Relational Database Service documentation](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html).

If you enable hyper-threading on your AWS virtual machine instance, the Software Asset Management application provides one Per Processor license for every two vCPUs on which you install or run an Oracle cloud Database or WebLogic Server. If you don’t enable hyper-threading, the Software Asset Management application provides one Per Processor license for every vCPU on which you install or run an Oracle cloud database or WebLogic Server.

For more information on Oracle databases and WebLogic servers in AWS, see [Oracle Database on the AWS Cloud: Quick Start Reference Deployment](https://docs.aws.amazon.com/quickstart/latest/oracle-database/welcome.html).

## Microsoft Azure

Microsoft Azure is a cloud computing platform on which you can create and run Oracle databases and WebLogic servers.

If you enable hyper-threading on your Microsoft Azure virtual machine instance, the Software Asset Management application provides one Per Processor license for every two vCPUs on which you install or run an Oracle cloud database or WebLogic Server. If you don’t enable hyper-threading, the Software Asset Management application provides one Per Processor license for every vCPU on which you install or run an Oracle cloud database or WebLogic Server.

For more information on Oracle databases and WebLogic servers in Microsoft Azure, see [Accelerate your cloud adoption with Microsoft and Oracle](https://azure.microsoft.com/en-us/solutions/oracle/#documentation).

**Parent Topic:**[Software Asset Management publisher pack for Oracle](oracle-publisher-pack.md)

