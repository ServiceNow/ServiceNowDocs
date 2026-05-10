---
title: GlideApplicationProperty - Scoped, Global
description: The GlideApplicationProperty API provides methods to get and set application property values for a specific domain.Returns the value for the specified application property and domain sys\_id.Stores the specified value in the specified application property for the specified domain, or the current session domain if not specified.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideApplicationProperty - Scoped, Global

The GlideApplicationProperty API provides methods to get and set application property values for a specific domain.

Application properties enable service providers to customize application functionality based on the domain. Instead of only having a single system property \(System Property \[sys\_properties\] table\) that defines the functionality for all domains and users, application properties can be implemented to define functionality for specific domains.

To access this API you must activate the Domain Support - Domain Extensions Installer \(com.glide.domain.msp\_extensions.installer\) plugin.

For additional information on domain-specific application properties, see [Domain-separated application properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/ds-application-properties.md).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideApplicationProperty - getValue\(String name, String domainSysId\)

Returns the value for the specified application property and domain sys\_id.

The list of available application properties is located in the Application Properties \[sys\_application\_property\] and Application Property Values \[sys\_application\_property\_value\] tables.

**Note:** If the specified domain is a child domain, and there is not an application property for the child domain, the method returns the parent domain application property, if available.

<table id="table_qzq_b2c_llb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the application property to return.**Note:** If the application is not global, you must prefix the name of the sys\_application\_property with the application's scope.

</td></tr><tr><td>

domainSysId

</td><td>

String

</td><td>

Optional. Sys\_id of the domain associated with the application property.Default: Session domain

</td></tr></tbody>
</table><table id="table_rzq_b2c_llb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Value of the specified application property for the specified domain. If **domainSysId** is not passed in the call, then returns the session domain.If the specified application property doesn't exist, returns the same-name system property value.

 If the user does not have access rights to the specified domain, throws an exception and no value is returned.

</td></tr></tbody>
</table>This example shows how to create a new application property and override its value for ACME and Cisco domains.

```
var MY_APP_PROP_NAME = 'my-app-prop';
var ACME_DOMAIN_ID = 'c90d4b084a362312013398f051272c0d';
var CISCO_DOMAIN_ID = 'c90f91924a362312001bdefae0f35d68';

// create a new app_config entry:
var now_GR = new GlideRecord('sys_application_property');
now_GR.name = MY_APP_PROP_NAME; 
now_GR.default_value = 'my-app-prop-default_value'; 
now_GR.insert();

// Override the value for ACME domain, catch exception if user can't access the specified domain
try {
  GlideApplicationProperty.setValue(MY_APP_PROP_NAME, 'prop-value-ACME', ACME_DOMAIN_ID);
  gs.info('Value for ACME domain: ' + GlideApplicationProperty.getValue(MY_APP_PROP_NAME, ACME_DOMAIN_ID));
} catch (ex) {
  gs.info('Exception: ' + ex);
}

// Override the value for Cisco domain -- assuming that the current session domain is Cisco. Notice that we don't pass domain-id explicitly
session.setDomainID(CISCO_DOMAIN_ID); // NOTE: this API is not available from non-global scope (use domain-picker to switch to Cisco)
gs.info('Domain: ' + session.getCurrentDomainID());
GlideApplicationProperty.setValue(MY_APP_PROP_NAME, 'prop-value-Cisco');
gs.info('Value for current session (Cisco) domain: ' + GlideApplicationProperty.getValue(MY_APP_PROP_NAME));

```

Output:

```
*** Script: Value for ACME domain: prop-value-ACME
*** Script: Domain: c90f91924a362312001bdefae0f35d68
*** Script: Value for current session (Cisco) domain: prop-value-Cisco
```

## GlideApplicationProperty - setValue\(String name, String value, String domainSysId\)

Stores the specified value in the specified application property for the specified domain, or the current session domain if not specified.

The following are guidelines for using this method:

-   The application property is not created if its name contains one of the following strings:
    -   glide.properties.blacklist
    -   glide.properties.no\_db\_override
    -   glide.properties.safe\_overrides
    -   glide.properties.maint\_write\_roles
-   The application property is not created if there is an existing system property with the same name, and the system property is marked as private.
-   The application property is not created if there is an existing system property and the application property does not reference it.
-   The name of the application property in the sys\_application\_property table is prefixed with the application's scope if it is not global.
-   This method cannot be called from a different scope.

<table id="table_qzq_b2c_llb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the application property to save.**Note:** If the application is not global, you must prefix the name of the sys\_application\_property with the application's scope.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Value to store in the specified application property.

</td></tr><tr><td>

domainSysId

</td><td>

String

</td><td>

Optional. Sys\_id of the domain associated with the application property.Default: Current session domain

</td></tr></tbody>
</table><table id="table_vpy_dlc_llb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the save operation was successful.Valid values:

-   true: Value was successfully saved.
-   false: An error occurred and the application property was not created/updated.

 If the user does not have access rights to the specified domain, throws an exception and no value is returned.

</td></tr></tbody>
</table>This example shows how to create a new application property and override its value for ACME and Cisco domains.

```
var MY_APP_PROP_NAME = 'my-app-prop';
var ACME_DOMAIN_ID = 'c90d4b084a362312013398f051272c0d';
var CISCO_DOMAIN_ID = 'c90f91924a362312001bdefae0f35d68';

// create a new app_config entry:
var now_GR = new GlideRecord('sys_application_property');
now_GR.name = MY_APP_PROP_NAME; 
now_GR.default_value = 'my-app-prop-default_value'; 
now_GR.insert();

// Override the value for ACME domain, catch exception if user can't access the specified domain
try {
  GlideApplicationProperty.setValue(MY_APP_PROP_NAME, 'prop-value-ACME', ACME_DOMAIN_ID);
  gs.info('Value for ACME domain: ' + GlideApplicationProperty.getValue(MY_APP_PROP_NAME, ACME_DOMAIN_ID));
} catch (ex) {
  gs.info('Exception: ' + ex);
}

// Override the value for Cisco domain -- assuming that the current session domain is Cisco. Notice that we don't pass domain-id explicitly
session.setDomainID(CISCO_DOMAIN_ID); // NOTE: this API is not available from non-global scope (use domain-picker to switch to Cisco)
gs.info('Domain: ' + session.getCurrentDomainID());
GlideApplicationProperty.setValue(MY_APP_PROP_NAME, 'prop-value-Cisco');
gs.info('Value for current session (Cisco) domain: ' + GlideApplicationProperty.getValue(MY_APP_PROP_NAME));

```

Output:

```
*** Script: Value for ACME domain: prop-value-ACME
*** Script: Domain: c90f91924a362312001bdefae0f35d68
*** Script: Value for current session (Cisco) domain: prop-value-Cisco
```

