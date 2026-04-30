---
title: Create asset contact relationships
description: Assign an asset to a customer contact who is responsible for managing that asset.Users with the system administrator role can assign a primary contact to an asset.Users with the system administrator role can assign a contact to an asset.Limit access to asset information to the assigned contacts by enabling the associated property.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create asset contact relationships

Assign an asset to a customer contact who is responsible for managing that asset.

Account and partner contacts can see all of the assets related to an account. To limit access to an asset, you can create an asset contact relationship and assign the asset to one or more contacts. Then you can enable the associated property to restrict access to the asset information to the assigned contacts.

The system administrator can add a primary contact to an asset by selecting a user in the **Primary Contact** field on the Asset form. This field references the Contacts table and is filtered by the asset’s account.

The system administrator can also create relationships with additional contacts from the **Asset Contacts** related list on the Asset form. When you create an asset contact relationship, you can select contacts from:

-   The account that the asset belongs to.
-   The partner of the account that the asset belongs to.
-   Any contacts added to these accounts using contact relationships.

After adding contacts to an asset, enable the related property to limit access. When enabled, the following access is limited from the customer portal:

-   When a user clicks **My Assets**, the list shows only those assets for which the user is a contact.
-   When a user clicks **Create Case**, the **Asset** field on the Create Case form shows only those assets for which the user is a contact.

## Assign a primary contact to an asset

Users with the system administrator role can assign a primary contact to an asset.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Assets**.

2.  Click the desired asset.

3.  Select a **Primary Contact**.

    This field references the Contacts \[customer\_contact\] table and is filtered by the account selected in the **Account** field.

4.  Click **Update**.

    The contact is added to the **Asset Contacts** related list on the asset form.


## Assign a contact to an asset

Users with the system administrator role can assign a contact to an asset.

### Before you begin

Role required: admin

### About this task

Users with the sn\_customerservice.customer\_admin can also assign a contact to an asset from the Customer Service Portal.

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Assets**.

2.  Select the desired asset.

3.  From the **Asset Contacts** related list, select **New**.

    When you select **New**, a new Asset Contact form is displayed with the **Asset** field filled in.

4.  Select a **Contact** from the list of available contacts within the asset's account.

5.  Select the **Order** field to specify the sequence in which records are displayed, organized according to business preferences.

6.  Select **Submit**.

    The contact is added to the **Asset Contacts** related list.


## Enable the asset contact relationship property

Limit access to asset information to the assigned contacts by enabling the associated property.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Properties**.

2.  Set the **Restrict Assets based on Contacts assigned to the assets** property to **true**.

3.  Click **Save**.


