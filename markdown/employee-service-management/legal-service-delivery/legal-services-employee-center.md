---
title: Legal services on the Employee Center portal
description: Employees can submit and track requests to get legal support or get information on legal services through the Employee Center portal.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Legal services on the Employee Center portal

Employees can submit and track requests to get legal support or get information on legal services through the Employee Center portal.

Legal Service Portal enables employees to submit legal requests to get services and support from the legal department only. Whereas ServiceNow® Employee Center provides a single and unified portal experience for employees to find information and request services across various departments, including Legal. Using the Content Taxonomy framework, you can modify the default Legal taxonomy to include your service-specific content types and child topics.

To enable legal services on the Employee Center portal, ensure you've the following ServiceNow applications and plugins installed:

-   Legal Service Delivery applications
-   Employee Center plugin \(sn\_ex\_sp\)
-   Employee Experience Taxonomy plugin \(sn\_ect\)

## Legal taxonomy on Employee Center

The base system taxonomy — Employee — is installed when you install the Employee Experience Taxonomy plugin. To provide legal services, the following Legal taxonomy structure is available by default under the Employee taxonomy:​

1.  **Contracts** – Contains Sales Contract Review, Third Party Contract Review, and NDA intake forms.​
2.  **Privacy and Data** – Contains the Privacy Impact Assessment intake form​.
3.  **Ethics and Compliance** – Contains the Conflict of Interest, Stock Preclearance, and Ethics Complaints​ intake forms, and a knowledge base article on Insider Trading Policy. When enabled, an ethics complaint can also be submitted through the Anonymous Report Center portal.
4.  **Browse all legal** – Contains General Legal Request, Marketing Content Review, Digital Forensics, and Subpoena intake forms.

## Enabling legal services on the Employee Center portal

Complete the following tasks to enable legal services on the Employee Center portal:

1.  To customize the base system taxonomy, duplicate the taxonomy and then make the required changes in the cloned taxonomy.

    For more information, see [Clone taxonomy for employee content](../../employee-center/task/clone-taxonomy-content.md).

2.  Create intake forms and knowledge base articles for legal services and support.

    For more information on creating a legal request intake form, see [intake forms for legal requests](../task/create-record-producer-legal-request.md); and for more information on creating a knowledge base article, see [knowledge base articles](https://www.servicenow.com/docs/access?context=create-knowledge-article&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

3.  Associate the content with a topic in the taxonomy.

    For more information, see [Associate connected content to a topic](../../employee-center/task/associate-content-to-topics.md).


## Approvals for legal items through Employee Center

Employee Center uses configurable approvals using Task Configuration for the approvers to view and approve various items. The approvers review the detailed information about the item that needs approval from the **My Tasks** tab in Employee Center. The Task Configuration can be set up for both task tables \(legal requests, legal matters, and practice area tables\) and non-task tables \(artifacts, matter templates, custodians and non-custodians, and external storage documents.\)

The following base system Task Configurations in the To-dos Configuration are available with Legal Service Delivery apps:

-   Legal Request Management
    -   Legal Requests
    -   Legal Request Attachments
    -   Legal Request External Documents
-   Legal Matter Management
    -   Legal Matters
    -   Legal Matter Attachments
    -   Legal Matter External Documents
    -   Legal Matter Tasks
    -   Legal Matter Artifacts
    -   Legal Matter Templates
-   Legal Digital Forensics
    -   Custodial data
    -   Non-Custodial data

**Note:** These new Task Configurations, which are mapped to tables of Legal Service Delivery apps, replace the existing To-dos Widget Mapping settings for the approvals via Employee Center. To use the existing mappings for approvals, you must disable the Task Configurations.

For more information about configurable approvals in the Employee Center and how to configure them, see [Approvals hub](../../employee-center/concept/approval-hub-intro.md).

**Parent Topic:**[Integration of Legal Service Delivery with ServiceNow applications](../../lsd-sn-legal-contracts/concept/snclc-integrate-lsd-lp.md)

**Related topics**  


[Setting up Employee Center](../../employee-center/concept/setup-emp-center.md)

[Unified taxonomy for Employee Center](../../employee-center/concept/config-taxonomy.md)

[Create a topic](../../employee-center/task/create-topics-for-taxonomy.md)

