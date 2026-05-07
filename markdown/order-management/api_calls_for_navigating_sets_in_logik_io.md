---
title: API calls for navigating sets in ServiceNow CPQ
description: Understand how to use sets in a headless environment using API calls.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [API overview and resources, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# API calls for navigating sets in ServiceNow CPQ

Understand how to use sets in a headless environment using API calls.

## Setup

The following set and fields were created for this example:

-   Field: Example set field 1
    -   Picklist with options A, B, C
    -   Field variable: exampleSetField1
-   Field: Example set field 2
    -   Boolean
    -   Field variable: exampleSetField2
-   Set: Example set
    -   Contains Fields exampleSetField1 and exampleSetField2
    -   Variable name: exampleSet \(therefore, size field is set.exampleSet.size\)

![Example set](../images/cpq-apis-example-set-field-1.png)

## Row identifier and row index

Every time a set is expanded to include a new row, the new row has a row identifier and a row index assigned to it. These are how you change the set.

-   The row identifier starts at 1 and increases incrementally by 1. This number is used to add or remove rows from the set.
-   The row index starts at 0 and increases incrementally by 1. This number is used to adjust values of Fields in the set.

After every API call that changes the set, the rows are organized. Due to the reorganization, the row index and row identifiers are reassigned. This is explained in greater detail in the examples below.

## Changing the set size

There are two ways to change the number of rows in a set: by sending a single number, and by sending specific values for the row identifiers.

The first way to change the number of rows in a set is to send a single number \(the number of rows\) as the value of the size variable in the API call. This method offers less control, but is useful if you know the total number of rows in the set you want to build. In the following example, the number 6 is set as the value of the size and it creates row identifiers 1-6. To edit the fields in these rows, you would use the row index numbers of 0-5.

![API](../images/cpq-apis-change-set-size-1.png)

The second way to edit the size of the array is to send values in the placeholder for each row of the array. This is useful for adjusting the rows of the array with precision. Depending on what values are added to the API call and their order, a combination of the following three changes will occur:

-   If the API call references a value that is not among the current row identifiers, it will create a new row in the position of the new value.
-   If the API call does not reference any value that is among the current row identifiers, the row will be deleted from the array.
-   If the API call references a value that is among the current row identifiers, it will put that array row in the position of the row identifier in the API call.

Previously, the size of ExampleSet was set to 6, which resulted in the row identifiers \[“1”, “2”,”3”,”4”,”5”,”6”\].

Now, the following API call is sent to the same environment:

![Script](../images/cpq-apis-send-row-identifier.png)

When this call is sent, the following occurs:

-   No row identifier is called “Newrow1”. Therefore, a new row \( with the fields in the row set to defaults\) is inserted before any known row identifiers. \(This is the first change listed above.\)
-   A row identifier is called “5”. In the API call, it is in the second position \(after NewRow1\). Therefore, it will move to the second row position. \(This is the second change listed above.\)
-   No row identifier is called “7”. Therefore, a new blank row is inserted in position 3. \(First change.\)
-   The row identifiers “1”, “2”, “3”, “4”, and “6” are not referenced in the API call. Therefore, they are deleted. \(Third change listed above.\)

When all changes from the API call are complete, the row identifiers are reset.

![Script](../images/cpq-apis-row-identifiers-reset.png)

The following table shows this in greater detail, including the index values, which will be discussed in the next section.

<table id="table_k2t_l4x_2hc"><thead><tr><th>

Size field new identifier

</th><th>

Value sent in API call

</th><th>

Old row identifier

</th><th>

New index

</th><th>

Old index

</th></tr></thead><tbody><tr><td>

1

</td><td>

Newrow1

</td><td>

Did not exist

</td><td>

0

</td><td>

Did not exist

</td></tr><tr><td>

2

</td><td>

5

</td><td>

5

</td><td>

1

</td><td>

4

</td></tr><tr><td>

3

</td><td>

7

</td><td>

Did not exist

</td><td>

2

</td><td>

Did not exist

</td></tr><tr><td>

\{deleted rows\}

</td><td>

1,2,3,4 and 6 were not sent in API call defining size

</td><td>

1,2,3,4 and 6

</td><td>

Deleted

</td><td>

0,1,2,3 and 5

</td></tr></tbody>
</table>Important details to note:

-   After this API call, the row with row identifier 5 \(and index 4\) now has the row identifier 2 \(and an index of 1\) that need to be used for all future API calls.
-   Once a row is deleted from the array, it is deleted completely. So a new API call that references row identifier 6 would be referencing a new row. All earlier data and changes to fields in row identifier 6 are no longer relevant and cannot be referenced.
-   This is helpful for changing the order of rows.

One final note: If the API patch call "variableName": "set.exampleSet.size", "value": \["Newrow1", "5", "7"\] is sent more than once, the three old rows are deleted and three new rows are created. This would lose the data that was previously in 5.

## Changing set fields

The next step is to define values for the fields in the set. Assume that the following call occurs after the first size API patch sets the size to six rows. To change Example Set Field 1 and Example Set Field 2 for several rows, the following code would be added to the fields section of an API call:

```
{{
            "set": "exampleSet",
            "index": 0,
            "variableName": "ExampleSetField1",
            "value": "A"
        },
        {
            "set": "exampleSet",
            "index": 4,
            "variableName": "ExampleSetField1",
            "value": "B"
        },
{
            "set": "exampleSet",
            "index": 4,
            "variableName": "ExampleSetField2",
            "value": "True"
        },
{
            "set": "exampleSet",
            "index": 5,
            "variableName": "ExampleSetField1",
            "value": "C"
        },
```

This would result in the following:

<table id="table_l2t_l4x_2hc"><tbody><tr><td>

Row Identifier

</td><td>

1

</td><td>

2

</td><td>

3

</td><td>

4

</td><td>

5

</td><td>

6

</td></tr><tr><td>

Index

</td><td>

0

</td><td>

1

</td><td>

2

</td><td>

3

</td><td>

4

</td><td>

5

</td></tr><tr><td>

example SetField 1

</td><td>

A

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

B

</td><td>

C

</td></tr><tr><td>

example SetField 2

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

True

</td><td>

 

</td></tr></tbody>
</table>If the second size API patch from above is sent, the following would result:

<table id="table_m2t_l4x_2hc"><tbody><tr><td>

Size Field New Identifier

</td><td>

1

</td><td>

2

</td><td>

3

</td></tr><tr><td>

Size Field Old Identifier

</td><td>

\{new row, see above\}

</td><td>

5

</td><td>

\{new row, see above\}

</td></tr><tr><td>

Old Index

</td><td>

\{new row\}

</td><td>

4

</td><td>

\{new row\}

</td></tr><tr><td>

New Index

</td><td>

0

</td><td>

1

</td><td>

2

</td></tr><tr><td>

exampleSetField 1

</td><td>

 

</td><td>

B

</td><td>

 

</td></tr><tr><td>

exampleSetField 2

</td><td>

 

</td><td>

True

</td><td>

 

</td></tr></tbody>
</table>