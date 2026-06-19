---
title: Enterprise model and asset classes
description: The Enterprise Asset Management application supports enterprise model and asset classes that extend base classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, and dependent relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes.html
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 5
breadcrumb: [Enterprise Asset Management data model, Explore, Enterprise Asset Management, IT Asset Management]
---

# Enterprise model and asset classes

The Enterprise Asset Management application supports enterprise model and asset classes that extend base classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, and dependent relationships.

To access enterprise model and asset classes in the Enterprise Asset Management application, you must install the Expanded Model and Asset Classes application from the ServiceNow® Store. For more information on this application, see [Expanded Model and Asset Classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/enterprise-model-asset-classes-app.md).

Enterprise model and asset classes form the structural backbone of the Enterprise Asset Management data model. These classes are organized into class hierarchies, in which child classes extend their parent classes and inherit all parent attributes. The Enterprise Asset Management application establishes relationships between enterprise model classes and enterprise asset classes through model categories. For more information on model categories, see [Model categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/model-hierarchy.md).

## Supported enterprise model classes

The Enterprise Asset Management application supports the Enterprise good model \[sn\_ent\_model\] class, Firmware model \[sn\_ent\_firmware\_model\] class, and Discovered firmware model \[sn\_ent\_discov\_firmware\_model\] class, which extend the base Product model \[cmdb\_model\] class. The Enterprise good model \[sn\_ent\_model\] class is the primary model class for enterprise assets in the Enterprise Asset Management application. It is also the parent class of the following industry-specific enterprise model child classes:\[Omitted image "enterprise-model-classes-hierarchy.png"\] Alt text: Enterprise good model classes hierarchy.

<table id="table_o2v_sy5_25b"><thead><tr><th>

Enterprise good model child class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Medical model\[sn\_ent\_medical\_model\]

</td><td>

Classifies medical-based enterprise models, such as ER Medical Cart Kit and ECG Electrodes.

</td></tr><tr><td>

Medical device model\[sn\_ent\_medical\_device\_model\]

</td><td>

Classifies medical device-based enterprise models, such as Blood Pressure Monitor and MRI Patient Table.**Note:** When you upgrade to version 1.2.0 or later of the Expanded Model and Asset Classes application, the application automatically runs the `Update medical device category` fix script to associate the Medical Device model \[sn\_ent\_medical\_device\_model\] class with the existing Medical device model category. However, you may need to manually reclassify existing enterprise models under the Medical device model category from the Medical model \[sn\_ent\_medical\_model\] class to the Medical Device model \[sn\_ent\_medical\_device\_model\] class. Refer to [KB1182183](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB1182183) for detailed instructions.

Product Instance Identifier \(PID\) which is a unique and common identifier that links the asset, CI, and IBI classes is generated for the assets of Medical Device model category. PID is generated based on the PID configurations applicable for the Medical Device model category.

The Product Instance Identifier Configurations \[product\_instance\_identifier\_configuration\] table stores the PID configurations. By default, the following configurations are available:

-   **PID - Serial number** that includes a parameter defined based on the Serial number field of the Asset \[alm\_asset\] table.
-   **PID - Parent** that includes parameters defined based on the Parent and Model Component ID fields of the Asset \[alm\_asset\] table.

When many PID configurations are associated with the Medical Device model category, the configuration with the highest priority is considered first during the generation of the PID. The PID - Serial number configuration is mostly given the highest priority.

</td></tr><tr><td>

Medical drug model\[sn\_ent\_drug\_model\]

</td><td>

Classifies medical drug-based enterprise models, such as Amoxicillin and Prilosec.

</td></tr><tr><td>

Facility model \[sn\_ent\_facility\_model\]

</td><td>

Classifies facility-based enterprise models, such as HVAC Split System and Wire Shelf.

</td></tr><tr><td>

Transportation model \[sn\_ent\_transportation\_model\]

</td><td>

Classifies transportation-based enterprise models, such as Disc Brake Rotor Front and Fuel Cell Car.

</td></tr><tr><td>

Industrial model \[sn\_ent\_industrial\_model\]

</td><td>

Classifies industrial-based enterprise models, such as CNC Milling Machine and Laser Cutting Machine.

</td></tr><tr><td>

Retail model \[sn\_ent\_retail\_model\]

</td><td>

Classifies retail-based enterprise models, such as Retail Counter Scale and 80mm Thermal Receipt Printer.

</td></tr><tr><td>

Tactical equipment model \[sn\_ent\_tactical\_model\]

</td><td>

Classifies tactical equipment-based enterprise models, such as K19 Plate Carrier and Triple Mag Pouch.

</td></tr><tr><td>

Construction model \[sn\_ent\_construction\_model\]

</td><td>

Classifies construction-based enterprise models, such as Excavator and Hex Breaker Hammer Kit.

</td></tr><tr><td>

Wearable model\[sn\_ent\_wearable\_model\]

</td><td>

Classifies wearable asset-based enterprise models, such as N95 Respirator and High-vis Safety Vest.

</td></tr><tr><td>

Multimedia production equipment model\[sn\_ent\_mm\_prod\_equip\_model\]

</td><td>

Classifies multimedia production equipment-based enterprise models, such as Production Camera and Modular Broadcast Console.

</td></tr><tr><td>

System and smart card model\[sn\_ent\_system\_smart\_card\_model\]

</td><td>

Classifies system card- and smart card-based enterprise models, such as Smart Card and Magnetic Stripe Card.

</td></tr><tr><td>

Payment card model\[sn\_ent\_payment\_card\_model\]

</td><td>

Classifies payment card-based enterprise models, such as Debit Card and Credit Card.

</td></tr></tbody>
</table>**Important:** Starting with the Zurich release, the Classification \(classification\) column of the Enterprise good model \[sn\_ent\_model\] table has been deprecated and renamed as Classification \(deprecated\). Data from the deprecated column is now available in the Classification \(classification\_code\) column of the Product model \[cmdb\_model\] table.

**Note:** The Enterprise Asset Management application does not classify consumable models through the Consumable model \[cmdb\_consumable\_product\_model\] class that is available in the base CMDB class hierarchy. Instead, you can manually designate any enterprise model in any model category as consumable by setting the **Model type** field to **Consumable** on the corresponding enterprise model record.

## Supported enterprise asset classes

The Enterprise Asset Management application supports the Enterprise asset \[sn\_ent\_asset\] class, which extends the Base asset \[alm\_base\] class. The Enterprise asset \[sn\_ent\_asset\] class is the parent class of the following industry-specific enterprise asset child classes:\[Omitted image "enterprise-asset-classes-hierarchy.png"\] Alt text: Enterprise asset classes hierarchy.

<table id="table_kw5_dfv_25b"><thead><tr><th>

Enterprise asset child class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Medical asset \[sn\_ent\_medical\_asset\]

</td><td>

Classifies medical-based enterprise assets, such as hospital beds and X-ray machines.

</td></tr><tr><td>

Facility asset \[sn\_ent\_facility\_asset\]

</td><td>

Classifies facility-based enterprise assets, such as coffee makers and HVAC systems.

</td></tr><tr><td>

Transportation asset \[sn\_ent\_transportation\_asset\]

</td><td>

Classifies transportation-based enterprise assets, such as airplanes and brake pads.

</td></tr><tr><td>

Industrial asset \[sn\_ent\_industrial\_asset\]

</td><td>

Classifies industrial-based enterprise assets, such as forklifts and casting machines.

</td></tr><tr><td>

Retail asset \[sn\_ent\_retail\_asset\]

</td><td>

Classifies retail-based enterprise assets, such as display cases and clothing racks.

</td></tr><tr><td>

Tactical equipment asset \[sn\_ent\_tactical\_asset\]

</td><td>

Classifies tactical equipment-based enterprise assets, such as hydration carriers and tactical plate carriers.

</td></tr><tr><td>

Construction asset \[sn\_ent\_construction\_asset\]

</td><td>

Classifies construction-based enterprise assets, such as sledgehammers and hand saws.

</td></tr><tr><td>

Wearable asset \[sn\_ent\_wearable\_asset\]

</td><td>

Classifies wearable enterprise assets, such as helmets and uniforms.

</td></tr><tr><td>

Multimedia production equipment asset\[sn\_ent\_mm\_prod\_equip\_asset\]

</td><td>

Classifies multimedia production equipment, such as video mixers and broadcast sync generators.

</td></tr><tr><td>

System and smart card asset\[sn\_ent\_sys\_smart\_card\_asset\]

</td><td>

Classifies system cards and smart cards, such as magnetic stripe cards.

</td></tr></tbody>
</table>**Note:** The Linear asset \[sn\_eam\_linear\_asset\] class is the parent class of the Linear segment \[sn\_eam\_linear\_segment\] class, which classifies specific sections of a linear asset. For more information on linear assets and linear asset segments, see [Linear assets in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/using-linear-assets.md).

**Parent Topic:**[Enterprise Asset Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/eam-data-model.md)

