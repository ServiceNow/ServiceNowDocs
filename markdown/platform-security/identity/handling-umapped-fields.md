---
title: Handling unmapped fields
description: You can handle unmapped fields in SCIM customization in different ways.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SCIM customization, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Handling unmapped fields

You can handle unmapped fields in SCIM customization in different ways.

During SCIM customization, the fields that are not part of the `sys_user` and `sys_user_group` tables can be mapped by performing the following functions.

## Customize SCIM \(Create or Update\)

You can create or update the SCIM Client.

-   The SCIM admin can add custom scripts in the **onBefore** and **onAfter** scripts for fields that are not mapped in ETL Definition or RTE.
-   The SCIM admin can override RTE Mappings by adding custom scripts in the **onBefore** and **onAfter** scripts.
-   You can invoke a scriptable API in the RTE **onBefore** or **onAfter** scripts to access incoming request and perform transformations on other tables, lists, and unmapped attributes.
-   You can use the **sn\_auth.SCIM2Util.getScimProviderCustomizationContext\(\)** method to provide the SCIM request context that contains the **scimResource** object. The **scimResource** in context represents the following in each operation:
    -   **POST**: The SCIM resource sent in the request payload.
    -   **PUT**: The current SCIM resource from database replaced with the SCIM resource sent in thee request payload.
    -   **PATCH**: The current SCIM resource from the database after performing the patch operations.

The following is an example of an **onAfter** script.

```
(function onAfter(source, target, importLog) {

    var ctx = sn_auth.SCIM2Util.getScimProviderCustomizationContext();
    gs.info("scim context ee: " + JSON.stringify(ctx.scimResource));

    var roles = ctx.scimResource.roles;
    if(roles) {
        var removingRolesGR = new GlideRecord("sys_user_has_role");
        removingRolesGR.addQuery("user", target.sys_user[0].sys_id);
        removingRolesGR.query();
        removingRolesGR.deleteMultiple();

    for (var i = 0; i < roles.length; i++) {
        var addingRolesGR = new GlideRecord("sys_user_has_role");
        addingRolesGR.setValue("user", target.sys_user[0].sys_id);
        addingRolesGR.setValue("role", roles[i].value);
        addingRolesGR.setValue("state", "active");
        addingRolesGR.insert();
        }
        }
        var customUserExtn = new global.SCIMProviderCustomization().getCustomExtensionUrn('User');
        var salary = ctx.scimResource[customUserExtn].salary;
        if (salary) {
            var gr = new GlideRecord("u_user_salary");
            gr.addQuery("user", target.sys_user[0].sys_id);
            gr.query();
            if (gr.next()) {
                gr.setValue("salary", salary);
                gs.info("scim update: " + gr.update());
            } else {
            gr.setValue("salary", salary);
            gr.setValue("user", target.sys_user[0].sys_id);
            gr.insert();
            }
           }

})(source, target, importLog);
```

## Customize SCIM response

For the GET API calls, any response back to the SCIM client can be customized using the script by extending the **SCIMProviderCustomization** script.

While extending the script, the author can override the **customizeUserResponse** and **customizeGroupResponse** methods to modify the responses for User and Group resources.

The **com.snc.integration.scim2.provider.customization.script.id** property enables the SCIM plugin to use the script that should be used for response customization.

The following is an example of extending the base script.

```
var SCIMCustomizationScript = Class.create();
SCIMCustomizationScript.prototype = Object.extendsObject(SCIMProviderCustomization, {
    initialize: function() {
        SCIMProviderCustomization.prototype.initialize.call(this);
    },
    customizeUserResponse: function(context) {
        try {
            var rolesGR = new GlideRecord("sys_user_has_role");
            rolesGR.addQuery("user", context.scimResource.id);
            rolesGR.query();
            var i = 0;
            context.scimResource.roles = [];
            while (rolesGR.next()) {
                context.scimResource.roles[i] = {
                    display: rolesGR.getElement('role.name').getValue(),
                    value: rolesGR.getElement('role.sys_id').getValue()
                };
                i++;
            }
            var userGR = new GlideRecord("u_user_salary");
            userGR.addQuery("user", context.scimResource.id);
            userGR.query();
            if (userGR.next()) {
                var salary = userGR.getValue("salary");
                if (salary) {
                    var customExtensionValue = SCIMProviderCustomization.prototype.getCustomExtensionNodeValue.call(this, "User", context);
                    customExtensionValue.salary = salary;
                    SCIMProviderCustomization.prototype.setCustomExtensionNodeValue.call(this, "User", context, customExtensionValue);
                }
            }
        } catch (ex) {
            gs.error("err: " + ex);
        }
        return context;
    },
    customizeGroupResponse: function(context) {
        return context;
    },
    type: 'SCIMCustomizationScript'
});
```

**Note:**

-   The parameter that the **customizeUserResponse** and **customizeGroupResponse** methods contain is a context object with one attribute called **scimResource**. This attribute has all the attributes of a user or group resource object.
-   A customized script include can only be created and viewed by the admin.
-   If a user or group resource is modified, then you must return the context back.
-   If there are no modification of any attribute in the resource object, then set the **com.snc.integration.scim2.provider.customization.script.id** to empty or return as null.
-   If certain attributes are persisted through the **onAfter** script, they must be populated with database values in the **scimResource** object inside the customized script. This action is required so that the system can do the following:
    -   To get the correct **scimResource** object in **onAfter** scripts during the PUT and PATCH operation.
    -   To include the attributes that persisted through the **onAfter** script in the response back to the client.

## Helper functions

The following are some of the helper functions for SCIM customization. These functions enable you to fetch or set different types of information.

|Function|Purpose|
|--------|-------|
|**SCIMProviderCustomization.prototype.getCustomExtensionUrn.call\(this, "User"\);**|Fetch the value of custom extension schema.|
|**SCIMProviderCustomization.prototype.getServiceNowExtensionUrn.call\(this, "User"\);**|Fetch the value of the ServiceNow extension schema.|
|**SCIMProviderCustomization.prototype.getCustomExtensionNodeValue.call\(this, "User", context\);**|Fetch the custom schema node from the response.|
|**SCIMProviderCustomization.prototype.getServiceNowExtensionNodeValue.call\(this, "User", context\);**|Fetch the ServiceNow schema node from the response|
|**SCIMProviderCustomization.prototype.setCustomExtensionNodeValue.call\(this, "User", context, customExtensionValue\);**|Set the custom schema node in the response.|

The following is an example of using the helper function:

```
var customExtensionUrn = 
SCIMProviderCustomization.prototype.getCustomExtensionUrn.call(this, "User"); 
var customExtensionValue = 
SCIMProviderCustomization.prototype.getCustomExtensionNodeValue.call(this, "User", context); 
customExtensionValue.age = "18";
SCIMProviderCustomization.prototype.setCustomExtensionNodeValue call(this, "User", context, customExtensionValue); 
```

**Note:** RTE supports setting data in tables other than the sys\_user and sys\_user\_group tables.

