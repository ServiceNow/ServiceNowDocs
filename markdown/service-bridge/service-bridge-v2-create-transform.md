---
title: Create a transform in Service Exchange
description: As a provider or a consumer, create a transform in Service Exchange to integrate tasks between connected instances.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Create a transform in Service Exchange

As a provider or a consumer, create a transform in Service Exchange to integrate tasks between connected instances.

## Before you begin

Role required: admin

## About this task

The following steps describe the transform process for providers. Consumers can navigate to **All** &gt; **Service Exchange Consumer** &gt; **Transforms** and follow the same process.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **Transforms**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_r2f_zkw_d5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated number for the transform record.

</td></tr><tr><td>

Company

</td><td>

Consumer name for whom this transform is applicable.

</td></tr><tr><td>

All Companies

</td><td>

If this is selected, the transform runs for all companies except those with the same company level transform.

 Use this field to create a default transform definition that can be applied to all companies. The All companies field eliminates the need to define a specific transform for each customer account even when they have similar requirements. You can use the default definition to transform specific fields across all companies simultaneously.

 The global transform is applied only to companies that match the configuration and do not have a specific transform already defined. If a company specific transform for the same configuration already exists, this will override the global transform.

</td></tr><tr><td>

Type

</td><td>

-   **Simple**: Used when the field has a known and stable choice list on each instance. A related list of transform lines is created to match the inbound and outbound values.
-   **Advanced**: Used for complex criteria that requires a script to determine the new value.
-   **Virtual Inbound**: Used to transform a virtual inbound field. Requires a script to determine the new value.
-   **Virtual Outbound**: Used to transform a virtual outbound field. Requires a script to determine the new value.


</td></tr><tr><td>

Inbound

</td><td>

Option that enables an inbound transformation for this transform. This option is available only if you select the Type as Simple or Advanced.

</td></tr><tr><td>

Outbound

</td><td>

Option that enables an outbound transformation for this transform. This option is available only if you select the Type as Simple or Advanced.

</td></tr><tr><td>

Provider table

</td><td>

Option that designates the provider's task table. For example, Case.

</td></tr><tr><td>

Consumer table

</td><td>

Option that designates the consumer's task table. For example, Incident.

</td></tr><tr><td>

Provider field

</td><td>

Option that designates the provider's field. For example, State. This field is available only if you select the Type as Simple or Advanced.

</td></tr><tr><td>

Consumer field

</td><td>

Option that designates the consumer's field. For example, **State**. This field is available only if you select the Type as Simple or Advanced.

</td></tr><tr><td>

Virtual field

</td><td>

When Type field is set to **Virtual Inbound** or **Virtual Outbound**, this field is available to reference the virtual field this transform should populate.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  Select one of the following:

    1.  **Simple:** Click **New** in the Transform lines related list, and fill in the fields on the form.

        |Field|Description|
        |-----|-----------|
        |Provider label|Option that designates the provider's choice label. For example, Open.|
        |Provider value|Option that designates the provider's choice value. For example, 10.|
        |Customer label|Option that designates the customer's choice label. For example, Progress.|
        |Customer value|Option that designates the customer's choice value. For example, 2.|

        **Note:** You can generate transform mappings between provider and consumer tables automatically using the Transform Mapping Assist feature. For more information, see [Automate transforms with Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-transform-maps&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).

    2.  **Advanced**: Use a script to define the outbound and inbound labels and values as shown in the following example:

        ```
        output.value=input.value;
        output.label=input.label;
        
        var ci=new GlideRecord('cmdb_ci');
        
        if(direction=='inbound'){
           if(ci.get('correlation_id',input.value)){
              output.value=ci.sys_id+";
              output.label=ci.getDisplayValue();
              }
        }
        if (direction=='outbound'){
          if(ci.get(input.value)){
             if(ci.correlation_id){
                output.value=ci.correlation_id+";
                output.label=input.label;
               }
            }
        }
              
        
        ```

    3.  **Virtual Inbound**: Use a script to determine the inbound label and value as shown in the following example:

        ```
        var inputArr = input.value.split(',');
        var outputValues = [];
        var outputLabels = [];
        for (i in inputArr) {
            getInstanceID(inputArr[i]);
        }
        output.value = outputValues+'';
        output.label = outputLabels+'';
        
        function getInstanceID(name) {
            var gr = new GlideRecord('cmdb_ci_server');
            if (gr.get('name', name)) {
                outputValues.push(gr.sys_id+'');
                outputLabels.push(name);
            }
        }
        ```

    4.  **Virtual Outbound**: Use a script to determine the outbound label and value as shown in the following example:

        ```
        /*
         ** The 'input' object contains the original value and label
         ** 'direction' contains an 'inbound' or 'outbound' value to determine transform direction
         ** 'object_data' contains the Remote Task GlideRecord
         ** It is required to set the variables 'output.value' and 'output.label' with your script.
         */
        output.value = 'condev,conprod';
        output.label = 'condev,conprod';
        ```

6.  Click **Submit**.

7.  On the transform form, click **Activate**.


## Result

A transform record is created on your ServiceNow® instance. Any Remote Task's inbound or outbound fields that match a transform will automatically use them. To learn more, see [Create a remote task definition in Service Exchange for Providers](service-bridge-v2-create-remote-tasks-defs.md).

