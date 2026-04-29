---
title: MID Server ISecuredConfigProvider interface
description: Use the methods in this interface to create custom providers that manage secured parameter values in the MID Server config.xml file.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID Server configuration file security, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server ISecuredConfigProvider interface

Use the methods in this interface to create custom providers that manage secured parameter values in the MID Server **config.xml** file.

**Note:** These methods are contained in the **snc-automation-api.jar** file, located in the MID Server installation folder.

## initialize

This method initializes the provider with additional configuration parameters and does not return a value.

<table id="table_uhs_1k4_jbb"><tbody><tr><td>

```
void intialize(java.util.Properties properties,
               IMidServerEncrypter encrypter)
        throws java.lang.Exception
```

</td></tr></tbody>
</table>|Parameters|Description|
|----------|-----------|
|properties|Initialization properties.|
|encrypter|Encrypter to use if the provider is encryption based.|

<table id="table_m3r_hk4_jbb"><tbody><tr><td>

`java.lang.Exception`

</td></tr></tbody>
</table>## isParameterValueSecured

This method checks to see if the parameter value has been secured or not. This method returns a **boolean** type value.

<table id="table_vh2_zk4_jbb"><tbody><tr><td>

`boolean isParameterValueSecured(java.lang.String paramValue)`

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|paramValue|The parameter value.|

<table id="table_zc5_5l4_jbb"><tbody><tr><td>

The parameter returns **true** if the parameter value is secured.

</td></tr></tbody>
</table>## secureParameterValue

This method secures the parameter value if it has not been secured. This method returns a **string** type value.

<table id="table_uqj_pm4_jbb"><tbody><tr><td>

```
java.lang.String secureParameterValue(java.lang.String unsecuredParameterValue)
                               throws java.lang.Exception
```

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|unsecuredParameterValue|The unsecured parameter value.|

<table id="table_uc4_5m4_jbb"><tbody><tr><td>

This method returns the unsecuired parameter value.

</td></tr></tbody>
</table><table id="table_wd3_xm4_jbb"><tbody><tr><td>

`java.lang.Exception`

</td></tr></tbody>
</table>## unsecuredParameterValue

This method returns the unsecured value of the parameter. This method returns a **string** type value.

<table id="table_s1w_dn4_jbb"><tbody><tr><td>

```
java.lang.String unsecuredParameterValue(java.lang.String parameterName)
                                  throws java.lang.Exception
```

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|parameterName|The parameter name.|

<table id="table_x1q_jn4_jbb"><tbody><tr><td>

This parameter returns the unsecured value.

</td></tr></tbody>
</table><table id="table_ntg_ln4_jbb"><tbody><tr><td>

`java.lang.Exception`

</td></tr></tbody>
</table>**Parent Topic:**[MID Server configuration file security](mid-server-encrypter-api.md)

