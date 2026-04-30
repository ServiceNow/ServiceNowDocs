---
title: Populate record producer data and redirect users
description: You can enter data for all records created by the record producer, and redirect an end user to a particular page after the record producer is submitted.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Record Producer, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Populate record producer data and redirect users

You can enter data for all records created by the record producer, and redirect an end user to a particular page after the record producer is submitted.

To enter data with a record producer, use any combination of the following methods:

-   Create a variable on the record producer with the same name as the field in the target record. For example, a variable named caller\_id on a **Create a New Incident** record producer populates the `caller_id` field on the new incident record. Use a [variable type that corresponds to the field type](../reference/r_CreatingVariablesForFieldTypes.md).
-   Define a [template](https://www.servicenow.com/docs/access?context=c_Templates&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) to assign a static field value for all records created by the record producer.
-   Define a script that uses any variable or server-side objects and functions to assign values.
    -   Use `current.*FIELD_NAME*` to reference fields on the record being created.
    -   Use `producer.*VARIABLE_NAME*` to reference values entered by the end user.
    -   Use [RP.getParameterValue](https://www.servicenow.com/docs/access?context=RenderProperties-Scoped-API&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) to return specified parameter values passed on the URL. The RP stands for Render Properties, not Record Producer.

## Redirect after submitting a record producer

To redirect an end user to a particular page after the record producer is submitted, define the redirect link in the **Script** field using any of the following:

-   `producer.redirect`: Enables the redirect behavior within the Platform UI.
-   `producer.portal_redirect`: Enables the redirect behavior within Service Portal.

For example, the following code redirects users to their homepage after the record producer is submitted:

-   Within the Platform UI:

    ```
    producer.redirect="home.do";
    ```

-   Within Service Portal:

    ```
    producer.portal_redirect = "sp?id=sc_home"
    ```


The following code gives the id of the record producer:

```
RP.getParameterValue('sysparm_id')
```

**Parent Topic:**[Record Producer](c_RecordProducer.md)

**Related topics**  


[Create a record producer](../task/t_DefRecProdInSCat.md)

[Create record producers from tables](../task/t_CreatingRecordProducersFromTables.md)

