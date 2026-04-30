---
title: Expanded Model and Asset Classes Store application
description: The Expanded Model and Asset Classes Store application adds enterprise model classes, service model child classes, API model categories, and enterprise asset classes that extend out-of-the-box model and asset classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, identifier entries, and dependent relationships.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Expanded Model and Asset Classes Store application

The Expanded Model and Asset Classes Store application adds enterprise model classes, service model child classes,API model categories, and enterprise asset classes that extend out-of-the-box model and asset classes within the Configuration Management Database \(CMDB\) class hierarchy. These extensions include class descriptions, identification rules, identifier entries, and dependent relationships.

**Note:** This application is compatible with the Rome and later family releases.

For more information on the CMDB, see [Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

In addition to extending CMDB model and asset classes, the Expanded Model and Asset Classes application creates model categories that associate model and asset classes with CMDB configuration item \(CI\) classes. The Enterprise Asset Management application uses these classes and model categories to create asset and model records that can be used to track and manage enterprise assets. Discovery tools, such as the ServiceNow® Discovery application, can also use these classes and model categories to create asset and model records for discovered CIs. See [Model categories](model-hierarchy.md) for more information on model categories.

The Expanded Model and Asset Classes application also adds the API and Managed API model categories, which allow the Configuration Management Database \(CMDB\) application to create and associate application models with API and Managed API CMDB CI classes. API CMDB CI classes provide classifications for APIs \(application programming interfaces\), which are sets of definitions and protocols that enable computer programs to communicate with each other. Managed API CMDB CI classes provide classifications for APIs that are discovered through gateways or management services, such as Amazon API Gateway. By associating application models with these CMDB CI classes, the Configuration Management Database \(CMDB\) application can create version-agnostic representations of your APIs. These representations can then provide a more holistic view of each API during reporting and analysis. For more information on API and Managed API CMDB CI classes, see [API extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-api&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Enterprise model classes added by the application

The Expanded Model and Asset Classes application adds the Enterprise good model \[sn\_ent\_model\] class, Firmware model \[sn\_ent\_firmware\_model\] class, and Discovered firmware model \[sn\_ent\_discov\_firmware\_model\] class, which extends the base Product model \[cmdb\_model\] class. The Enterprise good model \[sn\_ent\_model\] class includes classifications for various enterprise model types, which are categorized into the following industry-based child classes:![Enterprise good model classes hierarchy.](../image/enterprise-model-classes-hierarchy.png)

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

</td></tr></tbody>
</table>## Firmware model and Discovered firmware model classes

The Expanded Model and Asset Classes application adds the Firmware model \[sn\_ent\_firmware\_model\] and Discovered firmware model \[sn\_ent\_discov\_firmware\_model\] classes. These firmware model class tables extend the tables that the CMDB CI Data Foundation application installs.

The Firmware installation \[cmdb\_firmware\_install\] table added with the CMDB CI class model application stores the installation records based on the firmware embedded into assets. Based on the records in the Firmware installation table, the Discovered firmware model and Firmware model tables store the details of the firmware.

## Enterprise asset classes added by the application

The Expanded Model and Asset Classes application adds the Enterprise asset \[sn\_ent\_asset\] class, which extends the Base asset \[alm\_base\] class. The Enterprise asset \[sn\_ent\_asset\] class includes classifications for various enterprise asset types, which are categorized into the following industry-based child classes:![Enterprise asset classes hierarchy.](../image/enterprise-asset-classes-hierarchy.png)

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

</td></tr></tbody>
</table>## Service model classes added by the application

The Expanded Model and Asset Classes application adds the following child classes to the base Service model \[cmdb\_service\_product\_model\] class. These child classes provide classifications for various service model types.

<table id="table_zvh_kvn_xyb"><thead><tr><th>

Service model child class

</th><th>

Role required for read access

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card service model\[sn\_ent\_card\_service\_model\]

</td><td>

sn\_ent.card\_service\_model\_viewer

</td><td>

Classifies service models that are based on card offerings from banks and financial institutions, such as credit cards and gift cards.

</td></tr><tr><td>

Deposit model\[sn\_ent\_deposit\_account\_model\]

</td><td>

sn\_ent.deposit\_account\_model\_viewer

</td><td>

Classifies service models that are based on deposit accounts offered by banks and financial institutions, such as savings and checking accounts.

</td></tr><tr><td>

Loan model\[sn\_ent\_loan\_account\_model\]

</td><td>

sn\_ent.loan\_account\_model\_viewer

</td><td>

Classifies service models that are based on loan options offered by banks and financial institutions, such as personal loans and mortgage loans.

</td></tr><tr><td>

Line of credit model\[sn\_ent\_line\_of\_credit\_model\]

</td><td>

sn\_ent.line\_of\_credit\_model\_viewer

</td><td>

Classifies service models that are based on lines of credit offered by banks and financial institutions, such as overdrafts on savings and checking accounts.

</td></tr><tr><td>

Financial service model\[sn\_ent\_financial\_services\_model\]

</td><td>

sn\_ent.financial\_services\_model\_viewer

</td><td>

Classifies service models that are based on financial services offered by banks and financial institutions, such as safe lockers and wire services.

</td></tr><tr><td>

Investment model\[sn\_ent\_investment\_model\]

</td><td>

sn\_ent.investment\_model\_viewer

</td><td>

Classifies service models that are based on wealth management options offered by banks and financial institutions, such as mutual funds and retirement planning.

</td></tr><tr><td>

Personal lines insurance product model\[sn\_ent\_b2c\_ins\_policy\_model\]

</td><td>

sn\_ent.b2c\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on personal lines insurance policies offered by insurance carriers, such as coverage and payment plans for personal auto insurance.

</td></tr><tr><td>

Commercial lines insurance product model\[sn\_ent\_b2b\_ins\_policy\_model\]

</td><td>

sn\_ent.b2b\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on commercial lines insurance policies offered by insurance carriers, such as coverage and payment plans for commercial property insurance.

</td></tr><tr><td>

Group life insurance product model\[sn\_ent\_group\_life\_ins\_policy\_model\]

</td><td>

sn\_ent.group\_life\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on group life insurance policies offered by insurance carriers, such as coverage and payment plans for group term life insurance.

</td></tr><tr><td>

Individual life product model\[sn\_ent\_indiv\_life\_ins\_policy\_model\]

</td><td>

sn\_ent.indiv\_life\_ins\_policy\_model\_viewer

</td><td>

Classifies service models that are based on individual life insurance policies offered by insurance carriers, such as coverage and payment plans for individual whole life insurance.

</td></tr><tr><td>

Medical insurance model \[sn\_ent\_medical\_insurance\_model\]

</td><td>

sn\_ent\_medical\_insurance\_model\_viewer

</td><td>

Classifies medical insurance models, including health insurance plans and government insurance programs such as Medicare or Medicaid.

</td></tr><tr><td>

Social benefit model\[sn\_ent\_social\_benefit\_model\]

</td><td>

sn\_ent.social\_benefit\_model\_viewer

</td><td>

Classifies service models that are based on social insurance programs and means-tested assistance programs, such as social security and the Supplemental Nutrition Assistance Program \(SNAP\).

</td></tr></tbody>
</table>## Contract model classes added by this application

<table id="table_y2z_wrg_zyb"><thead><tr><th>

Contract model class

</th><th>

Role required for read access

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Permit model\[sn\_ent\_permit\_model\]

</td><td>

contract\_manager

</td><td>

The Permit model is an extension of the Contract model table and is used to model licenses and permits that have been issued and entitles the recipients to perform certain activities or make use of specific resources.

</td></tr></tbody>
</table>## Requesting the Expanded Model and Asset Classes application

You must request the Expanded Model and Asset Classes application from the ServiceNow Store.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all available applications and for information about submitting requests to the Store. For cumulative release notes information for all released applications, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

1.  From a web browser, go to the [ServiceNow Store](https://store.servicenow.com/).
2.  Log in using your HI credentials.
3.  In the search bar, enter `Expanded Model and Asset Classes` and then click **Search**.
4.  Select the result called **Expanded Model and Asset Classes**.
5.  On the Expanded Model and Asset Classes page, click **Request Install**.

    The ServiceNow Request for App Installation - Expanded Model and Asset Classes dialog box opens.

6.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Instance Name|Name of the instance on which you want to install the application. After you enter the instance name, click **Validate Instance** to verify that the instance exists.|
    |Reason for request|Reason for requesting the application.|

7.  Click **Request**.
8.  Click **Close**.

If your request is approved, you will receive an email with detailed instructions on how to install the application. You can then install the application according to the instructions in the email.

## Verifying successful application installation

After you request and install the Expanded Model and Asset Classes application, verify that all enterprise model and asset classes have been added to the CMDB class hierarchy successfully.

1.  From your ServiceNow instance, navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
2.  Click **Hierarchy** to display the CI Classes list, where you can view all classes within the CMDB class hierarchy.
3.  Verify that all enterprise model and asset classes have been added to the list.
4.  \(Optional\) Select a class to verify the corresponding class description, identification rules, identifier entries, and dependent relationships.

**Warning:** Uninstalling the Expanded Model and Asset Classes application may compromise the integrity of the Enterprise Asset Management application, resulting in unexpected behavior.

