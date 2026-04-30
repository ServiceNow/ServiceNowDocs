---
title: Customize system properties for EcoVadis integration
description: You can optionally customize the default values of the sn\_ecovadis.token\_uri and sn\_ecovadis.score\_uri system properties. These properties manage tokens and access risk scores from EcoVadis when using Third-party Risk Management.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [TPRM with EcoVadis, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Customize system properties for EcoVadis integration

You can optionally customize the default values of the sn\_ecovadis.token\_uri and sn\_ecovadis.score\_uri system properties. These properties manage tokens and access risk scores from EcoVadis when using Third-party Risk Management.

## Before you begin

Create an EcoVadis connection and configuration. For more information, see [Create an EcoVadis connection and configuration](tprm-config-connection-ecovadis.md).

Role required: admin

## Procedure

1.  Select **All** and in the navigation filter ![](../../../reuse/icons/product-icons/filter-outline-24.svg) enter `sys_properties.list`.

2.  Navigate to the sn\_ecovadis.token\_uri or sn\_ecovadis.score\_uri properties.

3.  Select the property that you want and update the **Value**.

    Additional properties that can be customized include:

    -   sn\_ecovadis.app\_scope\_sys\_id: The sys id of EcoVadis for Third-party Risk Management Application.
    -   sn\_ecovadis.connection\_credential\_alias\_sys\_id: The sys id of connection and credentials alias configured in EcoVadis.
    -   sn\_ecovadis.ecovadis\_provider\_service: The sys id of the EcoVadis provider service.
4.  Select **Update**.

    The Vendor Risk Management integration with EcoVadis application \[com.sn\_app\_grc\_ecovadis\] is updated and ready for use.


**Parent Topic:**[Integrating EcoVadis with Third-party Risk Management](../concept/tprm-integrating-ecovadis.md)

