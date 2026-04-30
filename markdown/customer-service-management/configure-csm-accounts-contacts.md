---
title: Configure accounts and contacts
description: An account is a supported external customer and a contact is a user who is an employee of an account.Use Customer Service Management guided setup to import existing accounts and contacts.An account code is a unique identifier for an account, while an account path establishes the account hierarchy.After importing customer account information, update the com.snc.cs\_base.last.generated.code.tree.path property with the correct account code value.An account is a supported external customer. Use the Customer Service Management application to create account records.An account can have multiple addresses, such as a main address as well as shipping and billing addresses.A contact is a user who is an employee of an account. Use the Customer Service Management application to create contact records.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure accounts and contacts

An account is a supported external customer and a contact is a user who is an employee of an account.

## Before you begin

Role required: admin

## About this task

There are two types of accounts: customer accounts and partner accounts. The **Customer** and **Partner** fields on the Account form denote the account type. An account can be a customer account, a partner account, or both.

A partner is a supported external customer that sells to and supports other customers. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

**Note:** After importing customer account data, you must also [set the account code system property](configure-csm-accounts-contacts.md#).

An account can have multiple contacts but a contact can be associated with only one account. A contact can have one or more associated assets and service contracts. A contact can also have a user ID and can log in to the customer portal.

**Note:** A contact is a user in the system. If you create a contact, that person is also added to the User table \(sys\_user\).

## Procedure

-   You can import existing accounts and contacts using guided setup.

-   You can create new accounts and contacts using the Customer Service Management application.


## Import accounts and contacts with guided setup

Use Customer Service Management guided setup to import existing accounts and contacts.

### Before you begin

Role required: admin

### About this task

After importing customer account data, you must also [set the account code system property](configure-csm-accounts-contacts.md#).

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and click **Get Started**.

2.  In the Foundation Data category, click **Get Started**.

3.  Click one of the following:

    -   **Import Accounts**
    -   **Import Contacts**
4.  Upload data from an external data source into an import set.

5.  Create a transform map.

6.  Execute the transform map to transfer the data.

7.  Verify that the data records are imported into the target table.


### Account codes and account paths

An account code is a unique identifier for an account, while an account path establishes the account hierarchy.

#### Account codes

An account code is a unique key that identifies an account in a ServiceNow instance. This code is stored in the **Account Code** field on the Account form.

An account code must be unique. Attempting to insert a new record with previously existing account code in the Account \[customer\_account\] table, the value for the code results in the following error:

`java.sql.BatchUpdateException: Duplicate entry for key account_path`

#### Account paths

An account path establishes the hierarchy among different accounts. This path is stored in the **Account Path** on the Account form.

An account path is a combination of the account codes for each account in the hierarchy. For example, let's use the following accounts to demonstrate account paths.![Account hierarchy example with three levels of parent and child companies](../image/csm-config-workspace-account-hierarchy-example.png)

<table id="table_mxm_dst_jyb"><thead><tr><th>

Account

</th><th>

Account Code

</th><th>

Account Path

</th></tr></thead><tbody><tr><td>

Boxeo

</td><td>

~~~~1

</td><td>

~~~~1

 Boxeo is the parent company. The account path for Boxeo is the same as the account code, which indicates that it’s the first element in the hierarchy.

</td></tr><tr><td>

Boxeo USA

</td><td>

~~~~2

</td><td>

~~~~1/~~~~2

 Boxeo USA is a child company of Boxeo. The structure of the account path is interpreted as Boxeo/Boxeo USA.

</td></tr><tr><td>

Boxeo EMEA

</td><td>

~~~~3

</td><td>

~~~~1/~~~~3

 Boxeo EMEA is also a child company of Boxeo and the structure of the account path is interpreted as Boxeo/Boxeo EMEA.

</td></tr><tr><td>

Boxeo France

</td><td>

~~~~5

</td><td>

~~~~1/~~~~3/~~~~5

 Boxeo France is a child company of Boxeo EMEA. The structure of this account path is interpreted as Boxeo/Boxeo EMEA/Boxeo France.

</td></tr></tbody>
</table>#### Importing account records

If you create your account records by importing the data from some source system through a transform map, make sure you execute the business rules. The Account Path is added, updated, and deleted based on the insertion, updating, and deletion of records in the Account \[customer\_account\] table through the business rules. If the business rules are not executed, it can result in empty account paths, which can then result in data access issues.

**Note:** If you do not execute the business rules during import, run the script in the **Update account path** business rule for the newly imported records to set the account paths correctly.

### Set the account code property

After importing customer account information, update the **com.snc.cs\_base.last.generated.code.tree.path** property with the correct account code value.

#### Before you begin

Role required: admin

#### About this task

The **com.snc.cs\_base.last.generated.code.tree.path** system property stores the **Account Code** value for the most recently created customer account in the Account \(customer\_account\) table.

When you create a new customer account record, the system uses this property to determine a unique account code value for the account. The property is then updated with this latest assigned value so that the next account code value can be set as a unique value for the next account record insert.

The value of the **com.snc.cs\_base.last.generated.code.tree.path** property must match the value of the Account Code field for the last inserted customer account record. When you create customer account records by importing data from other sources or instances, these values can get out of sync. If these values do not match, the system generates an error upon creation of the next new record in the Account table:

`java.sql.BatchUpdateException: Duplicate entry for key account_path`

Use the steps below to fix this error.

#### Procedure

1.  Determine the account code for the last created account.

2.  Navigate to the System Property \[sys\_properties\] table.

3.  Set the **com.snc.cs\_base.last.generated.code.tree.path** property to the value determined in step 1.


## Create customer accounts

An account is a supported external customer. Use the Customer Service Management application to create account records.

### Before you begin

Role required: sn\_customerservice\_manager or admin

### About this task

There are two types of accounts: customer accounts and partner accounts. The **Customer** and **Partner** fields on the Account form denote the account type. An account can be a customer account, a partner account, or both.

A partner is a supported external customer that sells to and supports other customers. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** and click one of the following actions:

    -   To create a customer account, click **Accounts**.
    -   To create a partner account, click **Partners**.
2.  Click **New** and fill in the fields on the [Account form](../reference/customer-service-account-form.md).

    When a new customer account record is created, the system uses the **com.snc.cs\_base.last.generated.code.tree.path** system property to determine a unique account code value for the account. The property is then updated with this latest assigned value so that the next account code value can be set as a unique value for the next account record insert.

    **Note:** If this property is reset to the original value, the system attempts to create new accounts with account codes that are already in use, which can result in an invalid insert.

3.  Click **Submit**.


### Create additional account addresses

An account can have multiple addresses, such as a main address as well as shipping and billing addresses.

#### Before you begin

Role required: sn\_customerservice\_manager or admin

#### About this task

The main address for an account is stored in fields on the [Account form](../reference/customer-service-account-form.md). Shipping and billing addresses for an account are created and stored in the **Addresses** related list. An account can have multiple shipping and billing addresses.

#### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Accounts**.

2.  Click the number of the desired account.

3.  In the **Addresses** related list, click **New**.

4.  Fill in the fields on the Location form.

5.  Select an address type, either **Billing** or **Shipping**.

6.  Enable the **Primary** field.

    If you have multiple billing or shipping addresses, use this field to designate one as the primary address.

7.  Click **Submit**.


## Create customer contacts

A contact is a user who is an employee of an account. Use the Customer Service Management application to create contact records.

### Before you begin

Role required: sn\_customerservice\_manager or admin

### About this task

An account can have multiple contacts but a contact can be associated with only one account. A contact can have one or more associated assets and service contracts. A contact can also have a user ID and can log in to the customer portal.

**Note:** A contact is a user in the system. If you create a contact, that person is also added to the User table \(sys\_user\).

### Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Contacts**.

2.  Click **New** and fill in the fields on the Contact form.

3.  Enter the contact information, such as the name, email address, and phone number.

4.  Enter the name of the contact's company in the **Account** field.

5.  Select the **Timezone**.

6.  Select a **Language**.

7.  Select a **Notification** setting.

8.  Click **Submit**.

    After a registration request is approved, the customer contact receives an email with a user ID and temporary password. When logging in for the first time, the contact is asked to change the password.


