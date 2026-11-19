---
title: ETL Definition quick start guide
description: Learn how to set up and use an ETL definition to import data into ServiceNow tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/system-import-sets/etl-definition-quick-start.html
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 4
breadcrumb: [Robust Import Set Transformers, Import sets, Imports, Workflow Data Fabric]
---

# ETL Definition quick start guide

Learn how to set up and use an ETL definition to import data into ServiceNow tables.

## Before you begin

Role required: admin

For this quick start guide, we're going to import data in the following JSON file to ServiceNow target tables. This JSON file contains hierarchical data for a school, classes, students and subjects. Save the following content to a JSON file.

```

[{ 
   "name": "schoolA", 
   "classes": [ 
   { 
    "name": "classA", 
    "students": [ 
    {"name": "studentA", "subjects": [{"name": "subjectA", "marks": 80}, 
     {"name": "subjectB", "marks": 90},{"name": "subjectC", "marks": 100}]}, 
    {"name": "studentB", "subjects": [{"name": "subjectA", "marks": 75}, 
     {"name": "subjectB", "marks": 85}, {"name": "subjectC", "marks": 95}]}
   ] 
  },{ 
   "name": "classB", 
   "students": [ 
   {"name": "studentC", "subjects": [{"name": "subjectA", "marks": 60}, 
    {"name": "subjectB", "marks": 70}, {"name": "subjectC", "marks": 80}]}, 
   {"name": "studentD", "subjects": [{"name": "subjectA", "marks": 55}, 
    {"name": "subjectB", "marks": 65}, {"name": "subjectC", "marks": 75}]} 
   ] 
  } 
 ] 
}]
```

## Procedure

1.  Create a data source and load data.

    1.  Create a data source with a **Format** of **JSON**, and the **Path for each row** as `//`.

    2.  Check the **Data in single column** option.

    3.  Save the data source.

    4.  Attach the above JSON file to the data source.

    5.  Select **Load All Records** to load records to the import set table.

        \[Omitted image "data-source-school.png"\] Alt text: JSON Data Source form for the School Import.

    6.  Open the import set row created.

        The record should be saved to a single JSON column.

        \[Omitted image "school-import-row.png"\] Alt text: The import set row with the record saved as a single JSON column.

2.  Create the target table structure to import data.

    1.  In this example, we have a school with multiple classes, each class has multiple students, and each student has multiple subjects.

    2.  Create a table structure to reflect these relationships.

    3.  `School -> name : string`.

    4.  `Class -> name : string , school : reference to school`.

    5.  `Student -> name : string, class : reference to class`.

    6.  `Subject -> name : string, mark : integer, student : reference to student`.

3.  Create an ETL Definition to map the JSON record data to target tables.

    1.  Go to **System Import Sets** &gt; **ETL Definition**.

    2.  Select **New**.

    3.  Enter a name and save the record.

        \[Omitted image "etl-definition-school.png"\] Alt text: Record of ETL definition named school definition.

4.  Create entities.

    1.  Under the ETL Entities tab, select **New**.

    2.  Set the **Name** as `Import Set` and save.

    3.  Add import set entity fields for all the leaf values of the JSON.

        The field/path is the path from the root of the JSON and we mark arrays with \[\*\].

        \[Omitted image "etl-entity-import.png"\] Alt text: The Import Set ETL Entity form.

    4.  Go to ETL Definition and under ETL Entities, select **New**.

    5.  Set the **Name** as `School`.

    6.  Set the **Table** as the school table created in step 2.

    7.  Set the **Path** as `school`.

    8.  Save the Entity.

    9.  Select **Generate fields** under Related Links.

        This should generate the **Name** field. Set the **Coalesce** to **true**.

        \[Omitted image "etl-entity-school.png"\] Alt text: ETL Entity for School.

    10. Go to ETL Definition and under ETL Entities, select **New**.

    11. Set the **Table** as the class table created in step 2.

    12. Set the **Path** as `class[*]`.

        Using \[\*\] makes it an entity with multiple rows.

    13. Select **Generate fields** under Related Links.

    14. Since **School** in the ETL Entity fields is a reference field, modify the **Field/Path** to `school.name` and set **Coalesce** to **true** for the **Name** field because name is unique.

        \[Omitted image "etl-entity-class.png"\] Alt text: ETL Entity for Class.

    15. Add Entities to Student and Subject as well.

        For Subject, set **Coalesce** to **true** for both the **Name** and **Student** fields.

        \[Omitted image "etl-entity-student.png"\] Alt text: ETL Entity for Student.

        \[Omitted image "etl-entity-subject.png"\] Alt text: ETL Entity for Subject.

5.  Add RTE Entity Mappings.

    1.  Go to RTE Entity Mappings and select **New**.

    2.  Set the **Name** to `Import Set to school`.

    3.  Set the **Source Entity** to **Import Set**.

    4.  Set the **Target Entity** to **School**.

    5.  Keep the **Order** as **100**.

    6.  Under RTE Field Mappings, select **New**.

    7.  For the **Source Field**, select **School name**.

        You can only select the Entity fields from the source entity.

    8.  For the **Target Field**, select **Name**.

        You can only select the Entity fields from the target entity.

        \[Omitted image "rte-entity-mapping-school.png"\] Alt text: RTE Entity Mapping for Import set to school.

    9.  Go to ETL Definition and under RTE Entity Mappings select **New**.

    10. Set the **Name** to `Import set to class`.

    11. Select **Source Entity** to **Import Set**.

    12. Select **Target Entity** to **Class**.

    13. Set **Order** to **200**.

    14. Add the RTE Field Mappings to map **Name** and **School name**.

        The school **Target Field** should map to the **School name** of the import set. The system does the school look up using this value and sets the correct school reference.

        \[Omitted image "rte-entity-mapping-class.png"\] Alt text: RTE Entity Mapping for Import set to class.

    15. Add mappings for Student and Subject as well.

        \[Omitted image "rte-entity-mapping-student.png"\] Alt text: RTE Entity Mapping for Import set to student.

        \[Omitted image "rte-entity-mapping-subject.png"\] Alt text: RTE Entity Mapping for Import set to subject.

6.  Create a Robust Import Set Transformer record and run the import.

    1.  Go to the Data source created in step 1.

    2.  Select the Robust Transformer tab and select **New**.

    3.  Set a **Name**.

    4.  Set the **Transformer definition** to the ETL Definition we created earlier.

    5.  Set **Verbose**.

        Selecting **Verbose** is not required, but enables you to debug the configuration. Switch this off before moving to production because it can negatively impact the performance.

        \[Omitted image "robust-import-set-transformer.png"\] Alt text: Robust Import Set Transformer for School Transformer.

    6.  Select **Submit**.

        \[Omitted image "data-source-transformer.png"\] Alt text: Data Source for School Import.

    7.  Select **Load All Records**.

    8.  Select **Run Robust Transform**.

    9.  Select **Transform**.

    10. Go to the import set.

    11. Select the Import Set Rows tab and open the import set row record.

    12. If the configuration works correctly, it should show the import set row record with all the records inserted.

        \[Omitted image "import-set-records.png"\] Alt text: School import.


