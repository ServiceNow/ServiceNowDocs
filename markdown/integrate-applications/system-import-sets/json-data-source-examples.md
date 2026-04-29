---
title: JSON file import examples
description: These examples demonstrate how to import various types of JSON data and the necessary path for each row. JSON files that you import should follow these guidelines.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [File type data sources, Data sources, Import sets, Imports, Workflow Data Fabric]
---

# JSON file import examples

These examples demonstrate how to import various types of JSON data and the necessary path for each row. JSON files that you import should follow these guidelines.

For step-by-step instructions on creating a File type data source see, [Create a File type data source](../task/create-file-type-data-source.md).

-   For JSON arrays, the path for each row must specify the array root element twice, such as `/incidents/incidents`.
-   JSON files should follow [RFC-4627](https://www.ietf.org/rfc/rfc4627.txt). For example, a single comma should separate a value from the following name. Names within an object should be unique.
-   Predicates such as `@element`, `[index]`, or `text()`, as well as Axis such as children, siblings, or ancestors are not supported.

## Simple array

-   Path for each row: `/incidents/incidents`
-   Result: 2 records

In this example, the path for each row includes the array root node `/incidents` twice. This is necessary when importing an array.

```
{  
   "source":"HI",
   "incidents":[  
      {  
         "number":"INC0000001",
         "short_description":"Can't read email"
      },
      {  
         "number":"INC0000002",
         "short_description":"Error loading XML file"
      }
   ]
}

```

## Array in 2nd level

-   Path for each row: `/problems/data/data`
-   Result: 3 records

In this example, the path for each row includes the array root node `/data` twice.

```
{  
   "problems":{  
      "id":"0",
      "data":[  
         {  
            "number":"PRBTEST001",
            "short_description":"testsd1"
         },
         {  
            "number":"PRBTEST002",
            "short_description":"testsd2"
         },
         {  
            "number":"PRBTEST003",
            "short_description":"testsd3"
         }
      ]
   }
}

```

## Nested array

-   Path for each row: `/problems/problems/data/data`
-   Result: 3 records

In this example, the path for each row includes the root nodes for both arrays twice, `/problems` and `/data`.

```
{  
   "problems": [  
         {
      "id":0,
      "data":[  
            {  
               "number":"PRBTEST001",
               "short_description":"testsd1"
            },
            {  
               "number":"PRBTEST002",
               "short_description":"testsd2"
            },
            {  
               "number":"PRBTEST003",
               "short_description":"testsd3"
            }
          ]
       }
    ]	
}

```

## Supporting child \(nested\) arrays

By default, import does not support child \(nested\) arrays. You can enable support by unchecking the **Discard Arrays** check box in the Data Source view. The following table describes different behaviors when enabling and disabling child array support.

```
{ 
  "response":{
    "docs":[ 
      { 
        "id":"id_val",
        "childrenArray":[1,2,3],
        "anotherArray":[{"key1":"value1"}, {"key1": "value2"}],
        "elementWithArray":{"childrenArray":[1,2,3]}
      }
    ]
  }
}

```

<table id="table_apx_ct1_lhb"><thead><tr><th>

Path

</th><th>

Discard Arrays Enabled

</th><th>

Discard Arrays Disabled

</th></tr></thead><tbody><tr><td>

/response/docs/docs

</td><td>

Creates one record with the following columns and values:-   Id : id\_val
-   elementWithArray : \{\}

Any arrays found in a record, such as childrenArray or anotherArray, are not created as columns in the import table.

</td><td>

Creates one record with the following columns and values:

-   Id : id\_val
-   childrenArray : \[1, 2, 3\]
-   anotherArray : \[\{"key1" : "value1"\}, \{"key1" : "value2"\}\]
-   elementWithArray : \{"childrenArray" : \[1, 2, 3\]\}

</td></tr><tr><td>

/response/docs/docs/anotherArray/anotherArray

</td><td>

Creates two records, each with one column: key1.

</td><td>

Creates two records, each with one column: key1.

</td></tr><tr><td>

/response/docs/docs/childrenArray/childrenArray

</td><td>

Does not work and returns a **Path should always refer JSON Objects** error because the values in the array are not in a key-value structure.

</td><td>

Does not work and returns a **Path should always refer JSON Objects** error because the values in the array are not in a key-value structure.

</td></tr></tbody>
</table>## Orphan array

-   Path for each row: `//`
-   Result: 2 records

```
[  
   {  
      "number":"PRBTEST001",
      "short_description":"testsd1"
   },
   {  
      "number":"PRBTEST002",
      "short_description":"testsd2"
   }
]

```

## Multiple elements instead of an array

-   Path for each row: `/problems/problem`
-   Result: 3 records

**Important:** This format is not recommended. JSON files should follow RFC-4627, which states that names within an object should be unique. Use JSON arrays instead.

```
{  
   "problems":{  
      "title":"2 problems",
      "problem":{  
         "number":"PRBTEST001",
         "short_description":"testsd1"
      },
      "problem":{  
         "number":"PRBTEST002",
         "short_description":"testsd2"
      }
   },
   "problems":{  
      "title":"1 problem",
      "problem":{  
         "number":"PRBTEST005",
         "short_description":"testsd5"
      }
   }
}

```

