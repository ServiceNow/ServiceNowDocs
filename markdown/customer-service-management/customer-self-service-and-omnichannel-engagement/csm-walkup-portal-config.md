---
title: Configure the Walk-up Experience portal
description: Create engaging walk-up center service portals featuring your logo, portal theme, desired catalog, links to a knowledge base and social community, and more.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# Configure the Walk-up Experience portal

Create engaging walk-up center service portals featuring your logo, portal theme, desired catalog, links to a knowledge base and social community, and more.

## Before you begin

Role required: admin or sn\_walkup.walkup\_admin

Walk-up Experience includes a complete base-system **Walk-up Portal** with theme. The **Walk-up Portal** pages are meant to be used as built. You can create custom portal pages to meet your needs by copying the portal pages and associated widgets and making changes to the copies. You can configure both an online check-in portal and a physical check-in portal for your walk-up locations.

There are several ways to configure the Walk-up service portal:

-   **Service Portal** application: Modular user interface framework for quick and easy building and customization of application portals.
-   Service Portal Walk-up form: Requires CSS and HTML experience.

## Procedure

1.  To configure the Walk-up service portal using the **Service Portal** application, navigate to **Service Portal** &gt; **Service Portal Configuration**.

    The Service Portal configuration page opens.

2.  To customize the base-system walk-up portal with your unique branding, title, logo, theme colors, layout, properties, widgets, and more, or to create a new walk-up portal, refer to [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) for detailed information.

3.  Alternatively, to configure the Walk-up service portal using the Service Portal Walk-up form, navigate to **CSM Walk-up Experience** &gt; **Administration** &gt; **Portal Configurations**.

    The Service Portals list opens.

4.  In the Service Portals list, click Walk-up or search for it in the list header search box.

5.  Click the Form menu icon ![Form menu icon.](../../../common/image/Form_MenuIcon.png) and select **Configure** &gt; **Form Design**.

    The form designer opens.

6.  In the form designer header drop-down list select or search for any of the configurable walk-up forms to customize your portal appearance.

<table id="choicetable_egv_2gp_ldb"><tbody><tr><td id="d311403e156">

**Walk-up context \[wu\_context\]**

</td><td>

Configure an online check-in channel for users to join a walk-up queue before physically arriving at the walk-up location. Identifies a walk-up user and the description of the associated interaction.

</td></tr><tr><td id="d311403e165">

**Walk-up Location Queue \[wu\_location\_queue\]**

</td><td>

Configure the physical walk-up location interaction queue to manage and administer the service center. You can establish walk-up locations, set hours of operation, enable online check-in, determine assignment groups, associate stockrooms, as well as design the queue time display and position notification system.

</td></tr><tr><td id="d311403e174">

**Walk-up Reason \[wu\_m2m\_location\_queue\_reason\]**

</td><td>

Define various common reasons why a user needs walk-up support.

</td></tr><tr><td id="d311403e183">

**Walk-up Reason for Visit \[wu\_reason\]**

</td><td>

Specify the order in which reasons for a visit should be prioritized at a walk-up location.

</td></tr></tbody>
</table>    To modify form content to meet your portal requirements, refer to [Form configuration](https://www.servicenow.com/docs/access?context=basic-form-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for detailed information.


