---
title: Sample payload for Citrix software install records
description: A sample payload for the Citrix publisher pack that populates the Software Installation \[cmdb\_sam\_sw\_\_install\] table with software install records from third-party discovery sources.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Sample payload for Citrix software install records

A sample payload for the Citrix publisher pack that populates the Software Installation \[cmdb\_sam\_sw\_\_install\] table with software install records from third-party discovery sources.

The Citrix publisher pack supports two products: virtual applications and virtual desktop. For these products, Citrix supports concurrent licensing and user/device licensing.

**Note:** For information on license metrics, see [Software License Metrics](../concept/c_SAMLicenseMetrics.md)

The IRE API relies on two CI identifier rules for creating Citrix software install records. The Citrix License server \[cmdb\_ci\_appl\_license\_server\] identifier populates the CAL entries and the Citrix Delivery Controller \[cmdb\_ci\_appl\_delivery\_controler\] identifier creates the software install records.

The CAL entries are used during reconciliation to compare against the purchased rights in entitlements to get the correct license position for Citrix products​. The Citrix License server identifier provides information on the samp\_concurrent\_license\_consumption and the samp\_user\_device\_license\_consumption tables. Based on your licensing entitlements, you need to populate either of these two tables.

Send a payload to populate the samp\_concurrent\_license\_consumption or the samp\_user\_device\_license\_consumption table. Ensure that you mention the key attributes for the tables in the payload:

-   samp\_concurrent\_license\_consumption: product\_code and number
-   samp\_user\_device\_license\_consumption: product\_code, consumer, and consumer\_type

**Note:** The two tables are passed in one payload since both are related entries of the parent CI table, cmdb\_ci\_appl\_license\_server. In the payload, specify the relationship between the tables and the CI parent table.

Once you send the payload, entries are created in the samp\_concurrent\_license\_consumption and the samp\_user\_device\_license\_consumption tables. Now execute the scheduled job, SAM- Create Citrix CAL entries, to update the Client Access \[samp\_sw\_client\_access\] table. Client access records are created for each product with user/device count. ​

**Note:** Ensure that you configure the schedule job, SAM- Create Citrix CAL entries to execute after processing the payload successfully.

Using the Citrix Delivery Controller \[cmdb\_ci\_appl\_delivery\_controler\] identifier, send a payload to populate all the 7 Citrix tables. Make sure that you mention the key attributes for the 7 tables in the payload.

**Note:** Click **Related Entries** in the Citrix Delivery Controller identifier to look up the key attributes \(**Criterion attributes**\) for the Citrix tables.

Once the entries are created in the tables, execute the scheduled job, SAM- Create Citrix Software installs. The Citrix sofware install records are created in the Software Installation \[cmdb\_sam\_sw\_install\] table.

```
{ 'items': [{'className':'cmdb_ci_appl_license_server',
              'related': [
                          {
                          'className':'samp_concurrent_license_consumption',
                            'values':{
                             'product_code':'MW2ZPSE0001',
                             'in_use_count':511,
                             'overdraft':11,
                             'pooled_available':0,
                             'total_count':500
                              }
                          },
                          {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                             'product_code':'XDT_PLT_CCS',
                             'consumer':'consumer1',
                             'consumer_type':'user'
                             
                              }
                          },
                           {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                             'product_code':'XDT_PLT_CCS',
                             'consumer':'Device1',
                             'consumer_type':'device'
                              }
                          },
                           {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                            'product_code':'XDT_PLT_CCS',
                             'consumer':'consumer2',
                             'consumer_type':'user'
                              }
                          },
                           {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                            'product_code':'XDT_PLT_CCS',
                             'consumer':'consumer3',
                             'consumer_type':'user'
                              }
                          },
                          {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                            'product_code':'XDT_PLT_CCS',
                             'consumer':'consumer4',
                             'consumer_type':'user'
                              }
                          },
                          {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                            'product_code':'MW2ZPSE0001',
                             'consumer':'consumer5',
                             'consumer_type':'user'
                              }
                          },
                           {
                           'className':'samp_user_device_license_consumption',
                            'values':{
                             'product_code':'MW2ZPSE0001',
                             'consumer':'Device1',
                             'consumer_type':'device'
                              }
                          }
                        ],
              'values': {
                  'name': 'ACME License Server 2',
                  'tcp_port': 22,
                   'install_directory': 'Documents'
                  }
              },
              {
                'className':'cmdb_ci_win_server',
                'values': {'name':'samlabvm450'}
                      }
              ],
              'relations':[{
                   'type':'Runs on::Runs',
                   'parent':0,
                   'child':1
                 }]
            }
```

**Parent Topic:**[Software Asset Management references](references.md)

