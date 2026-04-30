---
title: Configure data validation using the Data Validation Assist table
description: Create field and record level validations in the Data validation assist table.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data capture and validation, Set up the account onboarding playbook, Configuring account onboarding, Account onboarding, Customer Success Management]
---

# Configure data validation using the Data Validation Assist table

Create field and record level validations in the Data validation assist table.

## Before you begin

Role required: admin

## About this task

Several pre-defined validations are available with the base system. When data is imported during the account onboarding process, these validations are used to validate the data. But you can define additional validations based on your requirement.

## Procedure

1.  Navigate to **All** &gt; **Account Lifecycle Events** &gt; **Data Validation Assist Support** &gt; **Data Validation Assist** table.

2.  Click **New** to open the Data Validation Assist record.

3.  Select the Validation type which can be Field level or Record level.

4.  For Field level validation type, you can select one of the following Validation sub types:

    -   Reference: Select the Reference table, Reference table field, Staging table, and Staging table field. Specify the reference fields in the staging table. A reference field stores a reference to a field on another table. When you define a reference field, a relationship is created between the two tables.
    -   Choice: Select the Target table, Target table field, Staging table, and Staging table field. Used to validate if the value specified in the Excel is present.
    -   Date: Select the date format, Staging table, and Staging table field.
    -   Datetime: Select the date and time format, Staging table, and Staging table field.
    -   Boolean: Select the Staging table and Staging table field. Checks for a true or false result.
    -   String character limits: Specify the Max length, Staging table, and Staging table field. Used to validate if the string length does not exceed the limit specified.
    -   Integer or decimal: Specify the Staging table and Staging table field. Used to validate if the field is an integer or a decimal number.
5.  Select the **Mandatory** check box to specify if a validation condition is mandatory.

6.  For Record level validation type, you can define custom scripts to validate the staging table records.

    The following is an example of a sample validation script.

    ```
    (function executeCondition( /* glide record */ stagingTableGr) {
        var obj = {
            validationPassed: true,
            message: ''
        }; /*      validationPassed : return true if validation passed else return false      message : populate error message if validationPassed is false else return empty string     */
        if (global.JSUtil.notNil(stagingTableGr.task) && global.JSUtil.notNil(stagingTableGr.u_company)) {
            if (stagingTableGr.task.company.name != stagingTableGr.u_company) {
                obj.validationPassed = false;
                obj.message = 'The Account is not matching with the Case Account.';
            }
        }
        return obj;
    })(stagingTableGr);
    ```

7.  Click **Submit** to create a new validation assist table.


