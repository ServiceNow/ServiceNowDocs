---
title: Robust Import Set Transformers
description: Use robust import set transformers instead of transform maps if you want to extract, transform, and load data to one or more target tables.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Import sets, Imports, Workflow Data Fabric]
---

# Robust Import Set Transformers

Use robust import set transformers instead of transform maps if you want to extract, transform, and load data to one or more target tables.

## Robust import set transformers versus transform maps

Transform maps define the mapping from imported data stored in a staging table to a single target table in the ServiceNow AI Platform. Transform maps also insert data into target tables, performing both transform and processing functions. You can define multiple table mappings with multiple transform maps.

The Robust Transform Engine \(RTE\) and the robust import set transformer separate the transform and processing functions, providing a more flexible alternative to transform maps. The robust import set transformer allows you to extract data from a source table into an intermediary data structure. You can transform the data as desired and then load that data to one or more target tables. Records are processed as batches to enhance performance.

With transform maps, if you want data from the source table to go to three different target tables, you must create three separate transform maps. Each transform map parses the data separately, which results in three separate read operations. By contrast, the robust import set transformer requires only a single read operation to prepare the data for three target tables. The robust import set transformer is more efficient, especially when dealing with multiple target tables.

## Extract Transform Load \(ETL\)

When you use the robust import set transformer, Extract Transform Load \(ETL\) functionality transfers imported data to target tables. You define how the data is extracted, transformed, and loaded to one or more target tables. You can use ETL definitions to do the following:

-   Define entities \(an abstraction similar to tables\).
-   Define entity fields \(an abstraction similar to table fields\).
-   Define mapping between entities, and optionally designate whether a specific mapping should be ignored during data integration.
-   Define entity field mappings.
-   Define entity operations.

For an overview of ETL definitions, see [Extract Transform Load \(ETL\) definition overview](etl-definition-overview.md). For a step-by-step guide on how to create ETL definitions, see [Create Extract Transform Load \(ETL\) definitions](../task/create-etl-definitions.md).

As of the Paris release, ETL definitions also support nested data structures such as the following when the **Data source** has JSON/XML payloads in a single column.

```
{
   "records":[
      {
         "network":{
            "location":"San Diego",
            "computers":[
               {
                  "id":"C100",
                  "os":"Mac",
                  "disks":[
                     {
                        "size":"200GB",
                        "type":"SSD"
                     },
                     {
                        "size":"1TB",
                        "type":"Magnetic"
                     },
                     {
                        "size":"1TB",
                        "type":"Magnetic"
                     }
                  ]
               },
               {
                  "id":"C200",
                  "os":"Windows",
                  "disks":[
                     {
                        "size":"5TB",
                        "type":"Magnetic"
                     }
                  ]
               }
            ]
         }
      }
   ]
}
```

**Related topics**  


[Create a robust import set transformer](../task/create-robust-import-set-transformer.md)

[Create robust transform definitions](../task/create-robust-transform-definitions.md)

[Create Extract Transform Load \(ETL\) definitions](../task/create-etl-definitions.md)

