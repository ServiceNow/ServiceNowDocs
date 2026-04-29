---
title: Dynamic variable support in record screens
description: Use the script screen field in record screens to display dynamic field values. The script runs to determine the field value before it displays in your form. The value returned by the script doesn't replace the database value. For example, you can display translated content for dynamic variables within an email.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Add screen fields to a record screen, Screen fields, Configure a details screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Dynamic variable support in record screens

Use the script screen field in record screens to display dynamic field values. The script runs to determine the field value before it displays in your form. The value returned by the script doesn't replace the database value. For example, you can display translated content for dynamic variables within an email.

**Note:** The script field for record screens is configured within the ServiceNow AI Platform and not in the Mobile App Builder, as is the case for the other screen fields within the record screen. For configuration steps, [Configure the script field for records screens](../task/record-screen-script-type-config.md).

## Use case

Employees can view their HR cases and tasks in their preferred language on mobile devices, even when descriptions include personalized information from other fields. Using the script screen field in record screens, you can display these translated dynamic values in the mobile app. This provides the option for employees to see accurate translations of their HR cases, even when the descriptions contain personalized information.

## Items to note when using dynamic variable support

The following considerations must be met when configuring dynamic variables in the details screen.

-   In the **Type** field, select **Script**.
-   In the **Form field** field, select a field that contains the dynamic variable you want to use.

For full configuration instructions, see [Configure the script field for records screens](../task/record-screen-script-type-config.md).

## Working with the Execution Script field

Use the following script format to return values for display on the mobile app. The script must return a JSON object with two required properties. `Type` defines the content format \(in the example it's `HTML`\), and `Value` contains the actual content to display \(in the example it's `Hello`\).

```
var json = {
‘Type’: ‘HTML’,
‘Value’: “<p>Hello! </p>”
}

```

Consider the following when working with a JSON script:

-   The script must contain the properties `Type` and `Value`
-   The Type property can use the following options: Auto, Text, Percentage, Date, and HTML.
-   The `Type` in the JSON must be the same as the type selected from the field.
-   Date values must use this format: yyyy-MM-dd HH:mm:ss

## Examples

-   **Example 1: Displaying personalized case descriptions**

    Consider an HR case description field containing a variable that references the assigned user's first name:

    ```
    'Hi {current.assigned_to.first_name}, Unable to access the personal details section in payroll portal.'
    ```

    The script after this extracts the variable, retrieves the actual field value, and returns a personalized description:

    ```
    'Hi Beth, Unable to access the personal details section in payroll portal.'
    ```

    The script returns the updated text with Type set to 'Text'. For HTML content, set the Type to 'HTML'.

    ```
    (function generateScreenField(current) {
        //Type appropriate comment here, and begin script below 
        var description = current.description;
       var regex = /\$\{(.*?)\}/; 
       var match = description.match(regex); 
       var fieldName = match[1]; 
       var element = current.getElement(fieldName); 
       var fieldValue = element.getValue(); 
       var updatedDescription = description.replace(regex, fieldValue); 
       var json = { 
           'Type': 'Text', 
           'Value': updatedDescription 
       }; 
       return json; 
    })(current);
    
    ```

-   **Example 2: Calculating elapsed time as a percentage**

    The script calculates the percentage of time elapsed between start and end dates and displays it in a percentage field on the details screen.

    **Note:** The percentage value returns with a numeric value and without the % symbol. The symbol is handled by the field formatting.

    ```
    (function generateScreenField(current) {
        //Type appropriate comment here, and begin script below 
        //Logic to calculate percentage of time elapsed between start and end dates
        //Return percentage without % symbol
       var json = { 
           'Type': 'Percentage', 
           'Value': timeElapsedPercent 
       }; 
       return json; 
    })(current);
    
    ```

-   **Example 3: Calculating date values dynamically**

    This script calculates a date and displays it in a date field. The script runs when the field appears on the mobile app, calculates the date based on your logic, and returns it in the correct format.

    Date format requirements:

    -   Date only: yyyy-MM-dd \(example: 2025-01-29\)
    -   Date with time: yyyy-MM-dd HH:mm:ss \(example: 2025-01-29 14:30:00\)
    ```
    (function generateScreenField(current) {
        //Type appropriate comment here, and begin script below 
        //Logic to calculate value of the Date field
        //Return Date in the following format: yyyy-MM-dd (without Time)
        var json = { 
           'Type': 'Date', 
           'Value': calculatedDate
       };
    (or)
       //Return DateTime in the following format: yyyy-MM-dd HH:mm:ss (with time)
       var json = { 
           'Type': 'DateTime', 
           'Value': calculatedDate
       };
    
       return json; 
    })(current);
    
    ```


**Parent Topic:**[Add screen fields to a record screen](../task/sg-mobile-add-screen-field.md)

