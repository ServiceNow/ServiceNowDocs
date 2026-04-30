---
title: Inventory Tracker template
description: Build an application in App Engine Studio \(AES\) using the Inventory Tracker template to track the status of inventory and assets.The following tables, experiences, automated workflows, and roles are included in the Inventory Tracker template for App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Available templates, Create your app using an application template, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Inventory Tracker template

Build an application in App Engine Studio \(AES\) using the Inventory Tracker template to track the status of inventory and assets.

To use the Inventory Tracker template, install this application from the ServiceNow Store.

![Inventory Tracker template](../image/template-inventory-tracker.png)

An inventory tracker app enables your business and teams to easily track what they have, where it is, and who has it. Anytime, anywhere, and on any device. If your company needs to track the stock of items, this app can be used as a stock management tool or inventory tracker at home or in a warehouse.

This app covers three inventory use cases: consumables, loaners, and discontinued. Employees can request items via mobile app or web portal from any warehouse. Inventory managers can set reorder levels and will be automatically notified if an item is low on stock. Discontinued items with outstanding stock can still be requested but will not prompt inventory managers for reorder. Inventory managers can create items manually or by uploading a spreadsheet.

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Inventory Tracker template contents

The following tables, experiences, automated workflows, and roles are included in the Inventory Tracker template for App Engine Studio \(AES\).

### Tables in the Inventory Tracker app template

<table id="table_tgn_tvb_n4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inventory Control Table\[inventory\_ x\_&lt;company-code&gt;\_&lt;my\_inventory\_tracker\_app&gt;\_inventory\_control\]

</td><td>

Track the stock of items used by your business. For example, item name, manufacturer, image, category, and location.

</td></tr><tr><td>

Inventory Request Table\[x\_&lt;company-code&gt;\_&lt;my\_inventory\_tracker\_app&gt;\_inventory\_request\]

</td><td>

Track inventory requests submitted by employees. For example, the name and department of the requester, stock location, count, requested date, and return date.

</td></tr><tr><td>

Stock Location Table\[x\_&lt;company-code&gt;\_&lt;my\_inventory\_tracker\_app&gt;\_stock\_location\]

</td><td>

Track the location of stocked items. For example, name, address, and inventory manager.

</td></tr></tbody>
</table>### Experiences in the Inventory Tracker app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Inventory Control \| Portal|Form|Form for admins and managers to add inventory items, view stock quantity, and add stock locations.|
|Inventory request \| Workspace|Form|Form for employees to submit and manage inventory requests.|
|Inventory Control \| Default view|Form|Form for admins and managers to manage inventory items, view stock quantity, and manage stock locations.|
|*App name* \| Portal|Portal|Portal where all users can manage inventory requests and tracking.|
|Inventory request \| Default view|Form|Form for admins and managers to inventory items, view stock quantity, stock locations, and add notes.|
|Inventory request \| Portal|Form|Form for admins and managers to request inventory items.|
|*App name* \| Workspace|Workspace|Workspace to manage all Inventory tracker app configuration.|
|Stock Location \| Workspace|Form|Form for inventory managers to add stock names, addresses, and descriptions.|
|Stock Location \| Default view|Form|Form for inventory managers to add stock name, address, description, and department.|
|Inventory Control \| Workspace|Form|Form for admins and managers to manage inventory items, view stock quantity, and stock locations.|
|Inventory Tracker App|Form|Form for employees to view inventory list, see stock quantities, request items, and check the status of their requests using their organization's iOS or Android app.|

### Automated workflows in the Inventory Tracker app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Inventory Tracker Request Completed - Admin/Manager|Flow - record|Sends a notification when an inventory request has been completed.|
|Request Update as Submitted - Manager|Email|Notifies a manager that they have a new update on a requested item.|
|Item Out of Stock- Admin|Email|Informs an admin of items that are out of stock.|
|Return Date Updated - Manager|Email|Notifies manager of an updated return date.|
|Inventory Tracker Request Submitted - Manager|Flow - record|Notifies managers when an inventory request is submitted.|
|Inventory Tracker Inventory track Created - Admin|Flow - record|Notifies admins when an inventory track is created.|
|Stock Location Updated - Admin|Email|Informs an admin of updated stock location.|
|Inventory Tracker Checked Out - Employee|Flow - record|Notifies an employee when an item is checked out.|
|Request Overdue - Manager|Email|Informs a manager of an overdue request.|
|Item Returned - Manager|Email|Informs a manager of returned items.|
|Request Completed - Manager|Email|Informs a manager of a completed request.|
|Inventory Tracker Request Approved - Employee/Admin/Manager|Flow - record|Notifies employees, admins, and managers when an inventory request is approved.|
|Inventory Tracker Request Submitted - Employee|Flow - record|Notifies employees when their inventory request is submitted.|
|Checked Out - Employee|Email|Notifies employees of items that are checked out.|
|Inventory Tracker Out of Stock - employee|Flow - record|Notifies employees if an inventory item is out of stock.|
|Return Date Updated - Admin|Email|Informs an admin of an updated return date.|
|Request Canceled - Manager|Email|Notifies a manager when a request is cancelled.|
|Inventory Tracker Stock Location Updated - Admin|Flow - record|Notifies admins when a stock location is updated.|
|Item Out of Stock - Manager|Email|Notifies a manager when an item is out of stock.|
|Inventory Tracker Item Returned - Employee/ Manager|Flow - record|Notifies an employee or manager when an item is returned.|
|Inventory Tracker Inventory track updated- Admin|Flow - record|Notifies an admin when an inventory track is updated.|
|Item returned - Employee|Email|Notifies employees of returned items.|
|Request Denied - Admin|Email|Informs admins of denied requests.|
|Inventory Tracker Stock Location Created - Admin|Flow - record|Notifies an admin when a stock location is created.|
|Inventory Item Discontinued - Admin|Email|Notifies admins of discontinued items.|
|Request Approved - Manager|Email|Notifies managers of an approved request.|
|Inventory Item Updated - Admin|Email|Notifies admin of updated inventory item.|
|Inventory Tracker Inventory track Created - Admin|Flow - record|Notifies an admin when an inventory track is created.|
|Out of stock - Employee|Email|Notifies employees of items that are out of stock.|
|Inventory Tracker Request Denied - Admin|Flow - record|Notifies admins when an inventory request is denied.|
|Request Approved - Employee|Email|Notifies employees of approved requests.|
|Inventory Tracker Item Out of stock - Admin/Manager|Flow - record|Notifies admins and managers when an inventory item is out of stock.|
|Request Approved - Admin|Email|Notifies admins of an approved request.|
|Request submitted - Manager|Email|Notifies admins of a submitted request.|
|Request Overdue - Admin|Email|Notifies admins of an overdue request.|
|Request Denied - Manager|Email|Notifies managers of a denied request.|
|Stock Location Created - Admin|Email|Notifies admin when a stock location is created.|
|Overdue - Employee|Email|Notifies employee of overdue items.|
|Inventory Tracker Request Updated - Manager|Flow - record|Notifies managers when an inventory request is updated.|
|Request Denied - Employee|Email|Notifies employee of a denied request.|
|Inventory Tracker Inventory Discontinued - Admin|Flow - record|Sends a notification when an inventory item is discontinued.|
|Inventory tracker Return Date Changes - Admin/ Manager|Flow - record|Sends a notification to admin and manager when a return date changes.|
|Comments Added - Manager|Email|Notifies a manager about added comments.|
|Comments Added - Admin|Email|Notifies admins about added comments.|
|Inventory tracker Request Denied - Employee|Flow - record|Sends a notification to employees when their inventory request is denied.|
|Request Submitted - Employee|Email|Notifies employees when they submit a request.|
|Request created - Admin|Email|Notifies admins when a request is created.|
|Inventory Tracker Comments Added - Admin/Manager|Flow - record|Sends a notification to admins and managers when comments are added to inventory requests.|
|Request Canceled - Admin|Email|Notifies admins of a canceled request.|
|Inventory Tracker Request Overdue - Employee/Manager/Admin|Flow|Sends a notification to employees, managers, and admins if a request is overdue.|
|Inventory Item created - admin|Email|Notifies an admin when an inventory item is created.|
|Request Completed - Admin|Email|Notifies an admin when a request is completed.|
|Inventory tracker Request Cancelled - Admin/Manager|Flow - record|Sends a notification to admins and managers when an employee cancels an inventory request.|
|Inventory tracker Request Created - Admin|Flow - record|Sends a notification to admins when an inventory request is created.|

### Roles in the Inventory Tracker app template

<table id="table_ygl_1kt_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee\[x\_&lt;company-name&gt;\_ &lt;my\_inventory\_tracker\_app&gt;.employee\]

</td><td>

Employees can view inventory lists, check stock, request items, and check the status of their requests.

</td><td>

Create, Read \(own\), Update \(own\)

</td></tr><tr><td>

Admin\[x\_&lt;company-name&gt;\_ &lt;my\_inventory\_tracker\_app&gt;.admin\]

</td><td>

Admins can set up multiple inventory managers and stock locations.

</td><td>

Create, Read \(all\), Update \(all\), Delete

</td></tr><tr><td>

Inventory Manager\[x\_&lt;company-name&gt;\_ &lt;my\_inventory\_tracker\_app&gt;.inventory\_manager\]

</td><td>

Inventory managers can create inventory items, define the type of item, monitor inventory levels, and update vendor information.

</td><td>

Create, Read \(all\), Update \(all\)

</td></tr><tr><td>

Public\[x\_&lt;company-name&gt;\_ &lt;my\_inventory\_tracker\_app&gt;.public\]

</td><td>

Public users require no login to access features or functions with the public role.

</td><td>

Contains no roles.

</td></tr></tbody>
</table>