---
title: Create a script for a transform definition
description: Create the script at any time during the configuration of a definition.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Default Transform Definitions, Field normalization and transformation, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a script for a transform definition

Create the script at any time during the configuration of a definition.

## About this task

The script can perform a transform action without using a variable, but the action of the definition will be the same for all fields. Variables create more flexibility for the definition, enabling an administrator to use the same definition in different ways in different places. If a variable is defined, the script must reference the variable using the correct format.

There are three arguments in the script:

-   Variables: Contains the variables using the format variables.&lt;variable name&gt;.
-   Value: Contains the un-transformed value
-   Parameters: Special objects that set debug messages.

All position parameters \(such as Starting position and Ending position\) have three modes that apply to all the transform types that use this variable.

<table id="table_mvr_c1d_dr"><tbody><tr><td>

Positive positions

</td><td>

If the position is expressed as a positive integer, the platform calculates the starting position beginning from the left side of the field value. For example, in the string ABCDE, a position of 3 places the starting point of the action after C.

</td></tr><tr><td>

Negative positions

</td><td>

If the position is expressed as a negative integer, the platform calculates the position beginning from the right side of the field value. For example, in the string ABCDE, a position of -3 places the starting point of the action before C.

</td></tr><tr><td>

Regex

</td><td>

If the position value starts with /regex/, everything after that is a regular expression that is used to calculate the starting position. For example, in the string ABCDE, a position of /regex/B.\*D places the starting point of the action after C \(B and all the characters between B and D\).

</td></tr></tbody>
</table>## Procedure

1.  Open the **Odd/Even** record in the Transform Definitions module.

2.  Enter the following script to pass values with the odd\_even variable.

    ```
    function(variables, value, parameters) {
    	var odd = ('odd' == variables.odd_even);
    	var val = value - 0;
    	var val_odd = ((val & 1) == 1);
    	if (odd != val_odd)
    		val++;
    	return '' + val;
    	}
    ```

    The script references the variable in the form variables.odd\_even.

    ![Column named referenced in variable](../image/ColumnNameReferencedInVariable.png)

3.  Update the record to complete the configuration.

    The Odd/Even transform definition is now ready to use in a field transformation.


**Parent Topic:**[Default Transform Definitions](../reference/r_DefsIncludedWFieldTransformation.md)

