---
title: General guidelines for using CMDB Identification
description: Review the following general guidelines for using CMDB Identification effectively.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Identification rules, Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# General guidelines for using CMDB Identification

Review the following general guidelines for using CMDB Identification effectively.

## Identification rules

An independent identification rule identifies a CI based on the CI's attributes, independently of other CIs.

A dependent identification rule identifies a CI by its dependent CIs and the relationships of the identified CI with those dependent CIs. Identification with a dependent identification rule is based on the dependent CIs and the relationships and qualifiers between the identified CI and its dependent CIs. Identification then requires more time than with an independent identification rule and is prone to some identification errors. Usage of dependent rules should therefore be minimized.

CI modeling determines which type of identification rules are required for proper CI identification.

Create identification rules using the following order of importance:

1.  Independent identification rules — It is always preferable to create independent identification rules rather than dependent identification rules. When you model a CI, define the CI with a complete set of attributes that lend themselves to independent identification, eliminating the need to use additional CIs for identification.
2.  Dependent identification rules — If it is necessary to create dependent identification rules, then define a single level of dependency. Two is the maximum number of dependency levels that is supported.
3.  Avoid creating lookup identifier entries. The use of lookup identifier entry is highly discouraged as it can reduce performance. If unavoidable, ensure to first review class definitions and consider updates that allow usage of independent identification rules.
4.  Limit the number of identifier entries within an identification rule, ideally to 1. A second identifier entry can further reduce performance, as will each additional identifier entry.
5.  Create strong identification rules in which the strongest identifier entries and related entries are set with the highest priority.
6.  Ensure that the identification rule is at the class level that it needs to be.

## Payload

Create the payload using the following order of importance:

1.  Payload size — Limit the number of CIs per payload to 500.
2.  Avoid duplicate entries in the payload.

    Example: If an identification rule has a criterion attribute for the **name** field, then the following payload has duplicate items resulting in failure:

    ```
    var payload = {
        items: [{
            className:'cmdb_ci_linux_server',
            values: {
                name:'Win Server 200',
                ram:'2048'
            }},
    {
            className:'cmdb_ci_linux_server',
            values: {
                name:'Win Server 200',
                ram:'4096'
            }}]
    };
    ```

3.  Do not pass system data such as the following in the payload.

    ```
    var payload = {
        items: [{
            className:'cmdb_ci_linux_server',
            values: {
                name:'Win Server 200',
                sys_domain:'global',
                sys_domain_path:'xyz',
                sys_updated_on:'2017-06-15 16:25:11',
                sys_mod_count:23,
            }}]
    };
    ```

4.  Provide the minimum necessary set of criterion attributes for each payload item, according to what is specified in the corresponding identification rules.
5.  When matching CIs, use CIs’ sysIds if available. If provided, IRE can use the sysId to directly locate a CI without requiring any criterion attributes from the identification rule. In this case, IRE does not use the sysId in the matching process.
    -   Example: Independent CI that needs to be updated — sysId is available.

        ```
        var payload = {
            items: [{
                className:'cmdb_ci_linux_server',
                values: {
                    sys_id:'194876usytrr65378098',
                    ram:'2048',
                }}]
        };
        ```

    -   Example: Dependent CI that needs to be inserted. Tomcat War CI depends on Tomcat CI, and Tomcat CI depends on Linux Server CI. SysIds for the Tomcat and the Linux CIs are available.

        ```
        var payload = {
                items: [{
                    className:'cmdb_ci_app_server_tomcat_war’, 
                    values: {
                        name:'war1',
                        short_description:'my description'            }
                }, {
                    className:'cmdb_ci_app_server_tomcat',
                    values: {
                        sys_id:'194876usytrr65378098'
                    }
                }, {
                    className:'cmdb_ci_linux_server',
                    values: {
                        sys_id:'09876tysueyt6345lakiu'
                    }
                }],
                relations: [{
                            parent:1,
                            child:0,
                            type: 'Contains::Contained by’}, {
                                parent:1,
                                child:2,
                                type:'Runs on::Runs'}
                            ]
                        };
        ```

    -   Example: Dependent CI that needs to be updated — sysId is available.

        ```
        var payload = {
                items: [{
                    className:'cmdb_ci_app_server_tomcat_war', 
                    values: {
                        sys_id:'039387euey637465sytet',
                        short_description:'my description new'            }
                }]
                        };
        ```

6.  When inserting many CIs, all of which depend on the same CI, you should serialize your API calls. Otherwise, attempting to concurrently process many CIs can clog the system, significantly degrading overall system performance.

**Parent Topic:**[Identification rules](c_IdentificationRules.md)

**Related topics**  


[Create a CI identification rule](../task/t_CreateCIIdentificationRule.md)

[Create an identification inclusion rule](../task/create-id-inclusion-rule.md)

