---
title: Configuring HR Service Delivery integration with Oracle Cloud HCM
description: Set up Oracle HCM for HR Service Delivery to pull worker data from Oracle HCM into a ServiceNow instance. View worker profiles from Oracle HCM Cloud in ServiceNow HR Service Delivery.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery integration with Oracle Cloud HCM, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configuring HR Service Delivery integration with Oracle Cloud HCM

Set up Oracle HCM for HR Service Delivery to pull worker data from Oracle HCM into a ServiceNow instance. View worker profiles from Oracle HCM Cloud in ServiceNow HR Service Delivery.

## Before you begin

-   Role required: None
-   Activate HR Service Delivery integration with Oracle Cloud HCM that automatically activates Enterprise Service Management Integrations Framework and Oracle HCM Cloud spoke.

    **Note:** If you are upgrading from HR Service Delivery integration with Oracle Cloud HCM V 1.0.1 to a later version, follow the instructions in this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0997699).


## Procedure

1.  Install update sets.

    For more information, see [update sets in supporting links in ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/6008b56b1b20281050d621b5ec4bcbdd/1.0.2).

2.  Allow RCAs manually in the Utah release.

    This step is not required if you have already upgraded to Enterprise Service Management Integrations Framework 3.3.8 version.

    Allow the Restricted Caller Access records with Status = **Requested** and Source Scope = **Enterprise Service Management Integrations Framework**.

3.  For better performance, index the employee number field in HR Profile table and index coalesce fields in [transform maps](../reference/oracle-hcm-transform-maps.md).

    For more information, see [create a table index](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

4.  Set up Oracle HCM spoke.

    For more information, see set up [Oracle HCM Cloud spoke](https://www.servicenow.com/docs/access?context=setup-oracle-hcm&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

5.  Configure integration source properties for HR Service Delivery integration with Oracle Cloud HCM

    For more information, see [Configure properties](../reference/oracle-hcm-properties.md).

6.  Activate and run the scheduled flow that synchronizes Worker profile information between Oracle HCM and ServiceNow HR Service Delivery periodically.

    For more information, see[Activate schedule flows](../task/setup-the-job.md).


