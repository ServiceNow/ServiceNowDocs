---
title: Transformation script variables
description: Multiple variables can be used to define explicit mapping relationships in a transform map script.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Transform maps, Import sets, Imports, Data and Automation]
---

# Transformation script variables

Multiple variables can be used to define explicit mapping relationships in a transform map script.

-   **Variable name: source**

    **Type:** GlideRecord object

    **Description:** Contains the import source record currently being transformed. Specify a specific field from the source record as an object property.

    **Example:**

    ```
    var x = source.incident_state;
    ```

-   **Variable name: target**

    **Type:** GlideRecord object

    **Description:** Contains the import target record currently being inserted. Specify a specific field from the target record as an object property.

    **Example:**

    ```
    target.incident_state = "active";
    ```

-   **Variable name: map**

    **Type:** GlideRecord object

    **Description:** Contains the transformation map record currently being used for the transformation process. Specify a specific field from the transform map record with one of these properties.

    -   name
    -   sys\_id
    -   source\_table
    -   target\_table
    -   order
    **Example:**

    ```
    var x = map.order;
    ```

-   **Variable name: log**

    **Type:** Function

    **Description:** Log information about the current import process. Each log level has its own method.

    **Example:**

    ```
    log.info("This is an information message"); 
    log.warn("This is a warning message");
    log.error("This is an error message");
    ```

-   **Variable name: action**

    **Type:** Function

    **Description:** Specify the transformation action occurring on the target record. This value can be either "insert" or "update".

    **Example:**

    ```
    if(action =="insert"){
        ignore = true;
    }
    ```

-   **Variable name: ignore**

    **Type:** Boolean

    **Description:** When set to true, skips or aborts the current import action. In onStart scripts, this variable aborts the entire transformation process. In onBefore scripts, this variable only skips the current row being transformed.

    **Example:**

    ```
    (function runTransformScript(source, map, log, target /*undefined onStart*/ ) {
        var transformCheck = new TransformCheck(source, map, log, target);
        var isMappingValid = transformCheck.validateMapping();
        if (!isMappingValid) {
            ignore = true;
        }
    })(source, map, log, target);
    ```

-   **Variable name: error**

    **Type:** Boolean

    **Description:** When set to true, aborts the current import action and logs an error message in the Import Set Log.

    **Example:**

    ```
    if(source.name=="no_transform"){
      error = true;
    }
    ```

-   **Variable name: error\_message**

    **Type:** String \(output message\)

    **Description:** When an error occurs, adds the specified error message to SOAP response.

    **Example:**

    ```
    if(source.name=="no_transform"){
      error = true;
      error_message = "Source is not intended for transformation";
    }
    ```

-   **Variable name: status\_message**

    **Type:** String \(output message\)

    **Description:** Adds the specified status message to SOAP response.

    **Example:**

    ```
    if(action =="insert"){
        status_message = "Inserting record";
    }
    ```


