---
title: Commands installed with CMDB Application CLI and API
description: Commands and command groups available to the ServiceNow CLI when the app-cmdb-api-cli plugin is installed.
locale: en-US
release: zurich
product: ServiceNow CLI
classification: servicenow-cli
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 17
breadcrumb: [ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Commands installed with CMDB Application CLI and API

Commands and command groups available to the ServiceNow CLI when the app-cmdb-api-cli plugin is installed.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

To script critical operations which support automation across the enterprise, you can leverage APIs or run command line operations that the CMDB Application CLI and API store app provide instead of using the user interface. The CMDB Application CLI and API store app provides a robust framework which consolidates all the APIs that are related to application services and the command lines that let you access the interface to those APIs.

CMDB Application CLI and API commands enable the following tasks:

-   Registering and creating an application service and establishing upstream relationships
-   Getting details of a given application service and its upstream relationships
-   Connecting higher level constructs such as business applications and business service offerings
-   Populating an application service with a given population type
-   Changing the state of an application service

For the REST API solution, see [SG Services API](https://www.servicenow.com/docs/access?context=sg_services-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Convert Application Service

Converts a manual or empty type application service to a calculated application service. During conversion, the application service record moves into the \[cmdb\_ci\_service\_calculated\] table with the newly assigned class.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service convert --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service convert --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_lhc_n2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

levels

</td><td>

Number of levels to include in the conversion.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service.Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service convert --data '{"name":"Test Register","environment":"Test","version":"1.0","levels":8}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service convert --data "{"name":"Test Register","environment":"Test","version":"1.0","levels":8}"
    ```

-   **Return value**

    ```
    {
      "result": {
      "status": "success"
      }
    }
    ```


## Create Application Service Relationship

Constructs upstream relations such as business applications, business service offerings, and other application services. Running this command creates a relationship, taking input with a single parent and a corresponding child object.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service create-relationship --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service create-relationship --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_ty2_q2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child

</td><td>

Information identifying the child application service with which to create a relationship. The child is located in the Service Instance \[cmdb\_ci\_service\_auto\] table.A dynamic CI group can be added as a child but cannot be parent.

 Data type: Object

 ```
"child": {
  "<IRE field name>": "String",
  "number": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

child.&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the child application service. For example, name or version.Data type: String

</td></tr><tr><td>

child.number

</td><td>

Unique number that identifies the child application service.Data type: String

</td></tr><tr><td>

child.sys\_id

</td><td>

Sys\_id of the child application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].Data type: String

</td></tr><tr><td>

parent

</td><td>

Details identifying the parent application service with which to create a relationship.Data type: Object

 ```
"parent": {
  "<IRE field name>": "String",
  "number": "String",
  "sys_id": "String",
  "class_name": "String"
}
```

</td></tr><tr><td>

parent.&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version.Data type: String

</td></tr><tr><td>

parent.number

</td><td>

Unique number that identifies the application service.Data type: String

</td></tr><tr><td>

parent.sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].Data type: String

</td></tr><tr><td>

parent.class\_name

</td><td>

Name of the class that contains the application service.The parent class name should be from one of the following tables:

-   cmdb\_ci\_service\_auto
-   cmdb\_ci\_service\_discovered
-   cmdb\_ci\_service\_by\_tags
-   cmdb\_ci\_service\_calculated
-   service\_offering
-   cmdb\_ci\_business\_app
 Default: cmdb\_ci\_service\_auto

 Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service create-relationship --data '{"child":{"name":"wdfsdf","environment":"Test","version":"1.0"},"parent":{"sys_id":"abcdefg","name":"business App1","class_name":"service_offering"}}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service create-relationship --data "{"child":{"name":"wdfsdf","environment":"Test","version":"1.0"},"parent":{"sys_id":"abcdefg","name":"business App1","class_name":"service_offering"}}"
    ```

-   **Return value**

    ```
    {
      "result": {
      "status": "success"
      }
    }
    ```


## Delete Application Service

Deletes an application service.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service delete --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service delete --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_icm_q2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service delete --data '{"name":"Test Register","environment":"Test","version":"1.0"}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service delete --data "{"name":"Test Register","environment":"Test","version":"1.0"}"
    ```

-   **Return value**

    ```
    {
      "result": {
      "status": "success"
      }
    }
    ```


## Delete Application Service Relationship

Deletes an application service upstream relationship.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service delete-relationship --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service delete-relationship --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_mwt_q2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child

</td><td>

Information describing the child relationship to be deleted from the service application.Data type: Object

 ```
"child": {
  "<IRE field name>": "String",
  "number": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

child.&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the child application service. For example, name or version.Data type: String

</td></tr><tr><td>

child.number

</td><td>

Unique number that identifies the child application service.Data type: String

</td></tr><tr><td>

child.sys\_id

</td><td>

Sys\_id of the child application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].Data type: String

</td></tr><tr><td>

parent

</td><td>

Details identifying the parent application service from which to remove a relationship.Data type: Object

 ```
"parent": {
  "<IRE field name>": "String",
  "number": "String",
  "sys_id": "String",
  "class_name": "String"
}
```

</td></tr><tr><td>

parent.&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version.Data type: String

</td></tr><tr><td>

parent.number

</td><td>

Unique number that identifies the application service.Data type: String

</td></tr><tr><td>

parent.sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr><tr><td>

parent.class\_name

</td><td>

Name of the class that contains the application service.The parent class name should be from one of the following tables:

-   cmdb\_ci\_service\_auto
-   cmdb\_ci\_service\_discovered
-   cmdb\_ci\_service\_by\_tags
-   cmdb\_ci\_service\_calculated
-   service\_offering
-   cmdb\_ci\_business\_app
 Default: cmdb\_ci\_service\_auto

 Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service delete-relationship --data '{"child":{"name":"Test Register","environment":"Test","version":"1.0"},"parent":{"name":"business Service Offering1","class_name":"service_offering"}}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service delete-relationship --data "{"child":{"name":"Test Register","environment":"Test","version":"1.0"},"parent":{"name":"business Service Offering1","class_name":"service_offering"}}"
    ```

-   **Return value**

    ```
    {
      "result": {
      "status": "success"
      }
    }
    ```


## Find Application Service

Finds the details of a given application service and its upstream relationships.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin – This role provides unlimited viewing of application services.

    app\_service\_user – This role only provides viewing application services in Operational status.

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service find --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service find --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_wb1_r2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service find --data '{"name" : "Test App Service1"}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service find --data "{"name" : "Test App Service1"}"
    ```

-   **Return value**

    ```
    {
      "result": {
        "aliases": null,
        "asset": null,
        "asset_tag": null,
        "assigned": "",
        "assigned_to": null,
        "assignment_group": null,
        "attestation_score": null,
        "attested": "0",
        "attested_by": null,
        "attested_date": "",
        "attributes": null,
        "bucket": null,
        "business_contact": null,
        "business_need": null,
        "business_relation_manager": null,
        "business_unit": null,
        "busines_criticality": "4 - not critical",
        "can_print": "0",
        "category": null,
        "change_control": null,
        "checked_in": "",
        "checked_out": "",
        "checkout": null,
        "comments": null,
        "company": null,
        "compatibility_dependencies": null,
        "consumer_type": "internal",
        "correlation_id": null,
        "cost": null,
        "cost_cc": "USD",
        "cost_center": null,
        "delivery_date": "",
        "delivery_manager": null,
        "department": null,
        "discovery_source": "Manual Entry",
        "dns_domain": null,
        "due": "",
        "due_in": null,
        "duplicate_of": null,
        "end_date": "",
        "environment": null,
        "fault_count": "0",
        "first_discovered": "2021-07-19 20:09:48",
        "fqdn": null,
        "gl_account": null,
        "hide_from_dashboard": "0",
        "install_date": "",
        "install_status": "1",
        "invoice_number": null,
        "ip_address": null,
        "justification": null,
        "last_discovered": "2021-07-19 20:09:48",
        "last_review_date": "",
        "layer": null,
        "lease_id": null,
        "life_cycle_stage": null,
        "life_cycle_stage_status": null,
        "location": null,
        "mac_address": null,
        "maintenance_schedule": null,
        "managed_by": null,
        "managed_by_group": null,
        "manufacturer": null,
        "model_id": null,
        "model_number": null,
        "monitor": "0",
        "monitoring_requirements": null,
        "name": "Test App Service1",
        "number": "SNSVC0001014",
        "operational_status": "2",
        "order_date": "",
        "owned_by": null,
        "parent": null,
        "portfolio_status": "pipeline",
        "po_number": null,
        "prerequisites": null,
        "price_model": "per_unit",
        "price_unit": null,
        "published_ref": null,
        "purchase_date": "",
        "schedule": null,
        "serial_number": null,
        "service_classification": "Application Service",
        "service_level_requirement": null,
        "service_owner_delegate": null,
        "service_status": "requirements",
        "severity": null,
        "short_description": null,
        "skip_sync": "0",
        "sla": null,
        "spm_service_portfolio": null,
        "spm_taxonomy_node": null,
        "stakeholders": null,
        "start_date": "",
        "state": null,
        "subcategory": null,
        "supported_by": null,
        "support_group": null,
        "sys_class_name": "cmdb_ci_service_auto",
        "sys_class_path": "/!!/!7/!(",
        "sys_created_by": "admin",
        "sys_created_on": "2021-07-19 20:09:48",
        "sys_domain": "global",
        "sys_domain_path": "/",
        "sys_id": "a2f0618040697410f87713b656474255",
        "sys_mod_count": "0",
        "sys_updated_by": "admin",
        "sys_updated_on": "2021-07-19 20:09:48",
        "unit_description": null,
        "unverified": "0",
        "used_for": "Production",
        "user_group": null,
        "vendor": null,
        "version": null,
        "view_service": "61e1cb757f23220002d31ccebefa9120",
        "warranty_expiration": "",
        "relationships": [
          {
            "name": "Test Biz App1",
            "sys_id": "0250a94040697410f87713b656474250",
            "number": "APM0001001",
            "class_name": "cmdb_ci_business_app",
            "relationship": "Consumes::Consumed by"
          },
          {
            "name": "Tech Service Offering1",
            "sys_id": "98d0ed4040697410f87713b6564742ef",
            "number": "BSN0001005",
            "class_name": "service_offering",
            "relationship": "Contains::Contained by"
          }
        ]
      }
    }
    ```


## Populate Application Service

Populates an application service with a service population method.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service populate --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service populate --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_acn_r2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

population\_method

</td><td>

Required. Identifies the population method and its accompanying property to identify the content for population.Only one accompanying object is valid per type.

 Data type: Object

</td></tr><tr><td>

population\_method.group\_id

</td><td>

Group ID of the CMDB group configured with the cmdb\_group population type.Data type: "String"

 ```
"population_method": {
  "group_id": "String",
  "type": "cmdb_group"
}
```

 Associated population type: cmdb\_group

</td></tr><tr><td>

population\_method.levels

</td><td>

Number of levels to use in building the service. If the level value is not provided, the system checks the sys\_property for the value. If svc.manual.convert.levels.default\_value is not populated, a default value of 3 is used.Data type: Number

 ```
"population_method": {
  "levels": Number,
  "type": "dynamic_service"
}
```

 Associated population type: dynamic\_service

 Default: 3 if no level value is set for the sys\_property

</td></tr><tr><td>

population\_method.service\_candidate

</td><td>

Unique identifier of the service candidate.

 Data type: String

 ```
"population_method": {
  "service_candidate": "String",
  "type": "tag_based_service_family"
}
```

 Associated population type: tag\_based\_service\_family

</td></tr><tr><td>

population\_method.service\_relations

</td><td>

List of objects containing hierarchy data for the CIs within the application service. All CIs form pairs with a parent and child CI. The top-level CI, referred to as the entry point of an application service, does not have a parent CI.Data type: Array

 ```
"population_method": {

  "service_relations":[
     {
      "child": "String",
      "parent": "String"
     }
  ],

  "type": "service_hierarchy"   
}
```

 Associated population type: service\_hierarchy

</td></tr><tr><td>

population\_method.service\_relations.child

</td><td>

Name of a child CI related to the CI.Data type: String

</td></tr><tr><td>

population\_method.service\_relations.parent

</td><td>

Name of a parent CI related to the CI.Data type: String

</td></tr><tr><td>

population\_method.tags

</td><td>

List of objects containing tags to associate with the CI. This information is located in the Key Values \[cmdb\_key\_value\] table.Data type: Array

 ```
"population_method": {

  "tags": [
     {
      "tag": "String",
      "value": "String"
     }
  ],

  "type": "tag_list"  
}
```

 Associated population type: tag\_list

</td></tr><tr><td>

population\_method.tags.tag

</td><td>

Tag name.Data type: String

</td></tr><tr><td>

population\_method.tags.value

</td><td>

Tag value.Data type: String

</td></tr><tr><td>

population\_method.type

</td><td>

Required. Population type to add to the application service.Data type: Object

 Valid values:

-   cmdb\_group
-   service\_hierarchy
-   dynamic\_service
-   tag\_list
-   tag\_based\_service\_family


</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service populate --data '{"name":"Test Register","environment":"Test","version":"1.0","population_method":{"group_id":"String","type":"cmdb_group"}}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service populate --data "{"name":"Test Register","environment":"Test","version":"1.0","population_method":{"group_id":"String","type":"cmdb_group"}}"
    ```

-   **Return value**

    ```
    {
      "result": {
      "status": "success"
      }
    }
    ```


## Register Application Service

Creates an application service, tags and constructs upstream relationships such as business applications, business service offerings, and other application services.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service register --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service register --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_mrr_r2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version. Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. Data type: String

</td></tr><tr><td>

relationships

</td><td>

Upstream relationships categorized by type.Data type: Object

 ```
"relationships": {
 "business_app": [Array],
 "business_service_offering": [Array],
 "parent_app_service": [Array],
 "technical_service_offering": [Array]
}
```

 Maximum number of relationships is 25.

</td></tr><tr><td>

relationships.business\_app

</td><td>

List of objects representing Business Application relationship types. These values can be defined using one of the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id
 Data type: Array

</td></tr><tr><td>

relationships.business\_service\_offering

</td><td>

List of objects representing Business Service Offering relationship types. These values can be defined using the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id
 Data type: Array

</td></tr><tr><td>

relationships.parent\_app\_service

</td><td>

List of objects representing Application Service relationship types. These values can be defined using the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id
 Data type: Array

</td></tr><tr><td>

relationships.technical\_service\_offering

</td><td>

List of objects representing technology management offering \(formerly technical service offering\)relationship types. These values can be defined using the following items as key-value pairs.

-   &lt;IRE field name&gt;
-   number
-   sys\_id
 Data type: Array

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\] table. Data type: String

</td></tr><tr><td>

tags

</td><td>

List of objects containing tag definitions as key-value pairs.```
"tags": [
 {
  "key": "String",
  "value": "String"
 }]
```

 Data type: Array

</td></tr><tr><td>

tags.key

</td><td>

Tag category name.Data type: String

</td></tr><tr><td>

tags.value

</td><td>

Tag value.Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service register --data '{"name":"Test Register","environment":"Test","version":"1.0","number":" SNSVC0001014","relationships":{"business_application":[{"sys_id":"0250a94040697410f87713b656474250"},{"number":"APM0001002"},{"name":"Test Biz App1"}],"business_service_offering":[{"sys_id":"ed32e98040697410f87713b656474259"}],"technical_service_offering":[{"sys_id":"80e12d8040697410f87713b65647421c"},{"number":"BSN0001005"},{"name":"Tech Service Offering2"}],"parent_app_service":[{"sys_id":"a2f0618040697410f87713b656474255"}]},"tags":[{"key":"key1","value":"value1"},{"key":"key2","value":"value2"}]}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service register --data "{"name":"Test Register","environment":"Test","version":"1.0","number":" SNSVC0001014","relationships":{"business_application":[{"sys_id":"0250a94040697410f87713b656474250"},{"number":"APM0001002"},{"name":"Test Biz App1"}],"business_service_offering":[{"sys_id":"ed32e98040697410f87713b656474259"}],"technical_service_offering":[{"sys_id":"80e12d8040697410f87713b65647421c"},{"number":"BSN0001005"},{"name":"Tech Service Offering2"}],"parent_app_service":[{"sys_id":"a2f0618040697410f87713b656474255"}]},"tags":[{"key":"key1","value":"value1"},{"key":"key2","value":"value2"}]}"
    ```

-   **Return value**

    ```
    {
      "result": {
        "app_service": {
          "sys_id": "99b2a54040697410f87713b6564742ad",
          "name": "Test Register",
          "number": "SNSVC0001014"
        },
        "message": "Service registered successfully",
        "status": "INSERT"
      }
    }
    ```


## Update Application Service

Updates an existing application service provided and creates tags for the given application service.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service update --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service update --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_vyz_r2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;fields or tags to update&gt;

</td><td>

Use key-value pairs to identify each field or tag to be updated.Only basic information can be updated, no upstream relationships can be updated.

 Data type: String

</td></tr><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service update --data '{"name": "Test Register", "version": "2.0"}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service update --data "{"name": "Test Register", "version": "2.0"}"
    ```

-   **Return value**

    ```
    {
      "result": {
        "sys_id": "99b2a54040697410f87713b6564742ad",
        "name": "Test Register",
        "number": "SNSVC0001014",
        "version": "2.0"
      }
    }
    ```


## Update Application Service State

Changes the application service lifecycle state to activate, deactivate, or retire.

Command group:

-   Parent group: service-graph
-   Child group: app-service

-   **Roles required**

    app\_service\_admin

    If using a service mapping related service, the user must have the required roles for that service mapping related service.

-   **Command structure for Mac OS**

    ```
    snc service-graph app-service update-state --data '{JSON}'
    ```

-   **Command structure for Windows OS**

    ```
    snc service-graph app-service update-state --data "{JSON}"
    ```

-   **Arguments**

    This command passes a JSON object using the **data** parameter.

    The following properties for identifying a CI take precedence as follows:

    1.  sys\_id – If sys\_id, the system only uses the sys\_id and ignores any additional values.
    2.  number – If provided without the sys\_id, the system only uses the number and ignores any additional values.
    3.  &lt;IRE field name&gt; – The system only uses these values if the sys\_id or number are not provided.
<table id="table_xrh_s2d_3qb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;IRE field name&gt;

</td><td>

One or more IRE fields identifying the application service. For example, name or version.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service.Data type: String

</td></tr><tr><td>

state

</td><td>

Required. Lifecycle state of the application service. These values are updated in the Service Instance \[cmdb\_ci\_service\_auto\] table.Valid values:

-   ACTIVATE – Life cycle is operational and in use.
    -   operational\_status=Operational
    -   life\_cycle\_stage=Operational
    -   life\_cycle\_stage\_status=In Use
-   DEACTIVATE – Life cycle is not operational and is in the design stage.
    -   operational\_status=Non-Operational
    -   life\_cycle\_stage=Design
    -   life\_cycle\_stage\_status=Build
-   RETIRE – End of life.
    -   operational\_status=Retired
    -   life\_cycle\_stage=End Of Life
    -   life\_cycle\_stage\_status=Retired
 Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application service listed in the Service Instance \[cmdb\_ci\_service\_auto\].Data type: String

</td></tr></tbody>
</table>-   **Example on Mac OS**

    ```
    snc service-graph app-service update-state --data '{"name":"Test Register","environment":"Test","version":"1.0"}'
    ```

-   **Example on Windows OS**

    ```
    snc service-graph app-service update-state --data "{"name":"Test Register","environment":"Test","version":"1.0"}"
    ```

-   **Return value**

    ```
    {
      "result": {
      "status": "success"
      }
    }
    ```


**Parent Topic:**[ServiceNow CLI](../concept/servicenow-cli.md)

