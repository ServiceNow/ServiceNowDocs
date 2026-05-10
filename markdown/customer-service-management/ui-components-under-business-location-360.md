---
title: Business Location 360 components
description: Customer service agents can resolve reported business location issues by using different components on the Business Location 360 page in the Customer Service Management \(CSM\) application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Using Business Location 360, Manage cases, Use, Customer Service Management]
---

# Business Location 360 components

Customer service agents can resolve reported business location issues by using different components on the Business Location 360 page in the Customer Service Management \(CSM\) application.

## Components on the Business Location 360 page

The following list of components are on the Business Location 360 page:

-   Location information
-   Point of contact
-   Products installed
-   Services offered
-   All staff
-   Key performance indicators \(KPIs\)
    -   Number of P1 cases
    -   Number of cases by priority
    -   Service level agreements \(SLAs\) breached
-   Task tab
    -   **Cases**
    -   **Work orders**
-   Customer tab
    -   **Customers**
    -   **Accounts**
    -   **Households**

**Note:** You can customize these components according to your requirements by using the Business Location 360 template. The Business Location 360 template enables agents to get a comprehensive view that includes the crucial contextual information that they need for resolving reported issues. Your administrator can customize the Business Location 360 template to add the data sources, show the additional information, or represent the entities like stores, government agencies, healthcare organizations, automotive dealerships, or departments.

## Location information

The location information component displays the location information details for the record​. The following example shows a location information component that displays the name and type of the location, the address, email, phone number, and the manager's name.

![Location information such as the location address, phone number, manager's name, and so on.](../image/location-information.png "Location information component")

The **Email** and **Phone** links are clickable. When you select these links, the information is copied to the clipboard.

**Note:** If your administrator hasn't enabled Computer Telephony Integration \(CTI\), your contact numbers are copied to the clipboard instead of calling the numbers directly​. For more information about integrating Computer Telephony Integration \(CTI\), see [Computer Telephony Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_ComputerTelephonyIntegration.md).

On the location information link, navigate to the business location hierarchy view page​ by selecting the view hierarchy icon ![view hierarchy icon.](../image/hierarchy.png).

The following example shows a business location parent-child hierarchy with multiple nodes.

![Business location parent-child hierarchy with multiple nodes.](../image/business-location-hierarchy.png "Business Location Hierarchy page")

You can use this page to visualize the parent-child hierarchy structure, search for business locations, and perform different contextual actions on the nodes. You can also perform the following different contextual actions on the node:

-   Set the node as a home or parent node.
-   View the location details.
-   Create a case from the node.

You can get the location details of the node that you select. Also, if there’s a black dot on any node, it signifies a business location issue.

**Note:** The business location hierarchy page displays a maximum of 250 nodes. You can use the search functionality to find the node that you’re looking for.

## Point of contact

The point of contact component displays the primary points of contact that are available at a business location. The following example shows that the point of contact component can display the different points of contact at a business location.

![Different points of contact at a business location.](../image/point-of-contact.png "Point of contact component")

Selecting **View all** takes you to the Business Location member page where you can get the details of all the points of contact at a business location.

**Note:** By default, only three users are displayed.

## Products installed

The products installed component displays the information about the install base items at a business location. For example, you can see the install base name, product model name, and the status on this component. The following example shows the products installed component that provides information about the listed install bases at a business location.

**Note:** You can access this component only after your administrator activates the Customer Service Install Base Management plugin \(com.snc.install\_base\).

![Information about the listed install bases at a business location.](../image/products-installed.png "Products installed component")

If the listed products display **Issue reported** in the highlighted text, it indicates that there’s an active case reported for that install base item. The products within this component are sorted in the following order:

-   Install base items with a recently reported case.
-   Recently deployed install base items.

You can view the product details or create a case by selecting the Overflow icon ![Overflow icon.](../image/OverflowIcon.png).

Selecting **View all** takes you to the **Products installed** page where you can get the details of all the products installed at a business location.

**Note:** By default, only three products are displayed.

## Services offered

The services offered component displays the list of services that are offered at a business location. The following example shows the Services offered component that provides information about the list of all service names and the types that are available at a business location.

![List of services that are offered at a business location.](../image/services-offered.png "Services offered component")

**Note:** By default, only three services are displayed and these services are sorted in the ascending order.

## All staff

The all staff component displays the list of the staff members who are working at a business location and includes both the internal and external staff members. The following example shows the All staff component.

![List of staff available at a business location with the user name and responsibility.](../image/all-staff.png "All staff component")

Selecting **View all** takes you to the **All staff** page where you can get the details of all the staff members that are available at a business location.

**Note:** By default, only three staff members are displayed and these services are sorted in the ascending order of user name.

## KPIs

The KPI components are performance analytic indicators that display multiple types of information that are related to a case such as the following KPIs that are shipped out of the base system:

-   Number of P1 cases
-   Number of cases by priority
-   SLAs breached

The following example shows a list of the different KPIs. The list includes the number of P1 cases, the number of cases by priority, and the SLAs that were breached.

![List of different KPIs that includes the number of P1 cases, the number of cases by priority, and the SLAs that were breached.](../image/bl360-KPIs.png "KPIs component")

These KPIs are filtered to show the current business location-related details. Your administrator can customize these KPIs according to your location's requirements by using the [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md).

## Task tab

The task tab component displays the following cases and work- order tabs where you can see the cases and work orders that are associated with a business location​:

-   **Cases** tab. Displays the active cases that have a requesting service organization as the current business location order by the date that the case was last updated​. The account, consumer, and household fields are empty.
-   **Work orders** tab. Displays the work orders that have the service organization as the current business location. For this type of work order, the household field is empty and the state field isn’t completed. the state field is completed with errors, or the state field is closed.

The following example shows a list of the cases that are associated with a business location.

![List of cases that are associated with a business location.](../image/bl360-task-tab.png "Task tab component")

**Note:** A maximum of five records are displayed per page.

## Customer tab

The customer tab component displays the list of consumers, accounts, and households that are associated with a business location:

-   **Consumers** tab. Displays all the consumers or a filtered list of consumers. This information is based on the supported consumers that are associated with the business location.
-   **Accounts** tab. Displays all the accounts or a filtered list of accounts. This information is based on the supported accounts that are associated with the business location​.
-   **Households** tab. Displays all the households or a filtered list of households. This information is based on the supported households that are associated with the business location​.

    **Note:** You can access this component only after the Customer Household Data Model plugin \(com.snc.household\) is activated.

-   **Internal Business Locations** tab. Displays all the internal business locations or a filtered list of internal business locations. This information is based on the supported internal business locations that are associated with the business location​.
-   **External Business Locations** tab. Displays all the external business locations or a filtered list of external business locations. This information is based on the supported external business locations that are associated with the business location​.

The following example shows a list of the consumers that are associated with a business location.

![List of consumers associated with a business location.](../image/bl360-consumer-tab.png "Customer tab component")

**Note:** A maximum of 10 records are displayed per page.

**Related topics**  


[Using Business Location 360](using-the-business-location-360.md)

[Access Business Location 360 as a customer service agent](../task/access-business-location-360-as-agents.md)

[Access Business Location 360 as a customer service manager](../task/access-business-location-360-as-csm-managers.md)

[Access Business Location 360 as a location service agent](../task/access-bl-360-as-loc-serv-agent.md)

