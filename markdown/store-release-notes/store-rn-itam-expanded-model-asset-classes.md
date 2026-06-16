---
title: Expanded Model and Asset Classes release notes
description: Version history for the Expanded Model and Asset Classes application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-expanded-model-asset-classes.html
release: store
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# Expanded Model and Asset Classes release notes

Version history for the Expanded Model and Asset Classes application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.16.1 - May 2026**

    In this version, an issue has been resolved where the Activity log displayed only the new value of a field \(such as State\) after an update, without showing the previous value or the change history.

-   **Version 2.16.0 - March 2026**
    -   New tables added:
        -   CMDB Asset CI Model Interoperability Configuration, where asset/CI and product model interoperability is defined.
        -   CMDB Model Interoperability Type, which contains the list of interoperability types that can be selected when defining the relationships between assets/Cis and product models.
    -   Changed: The existing Model Compatibility table now includes an optional reference to the CMDB Model Interoperability Type.
    -   Fixed: Editing the Parent field on the Asset record is now restricted.
-   **Version 2.15.0 - December 2025**

    New: The Investigative service model is added to classify investigative cases by offense type, such as fraud, assault, or cybercrime, based on standardized taxonomies like the FBI’s NIBRS offense codes. This model is purpose-built for investigative case classifications. It aids in routing, reporting, and analytics, and supports both national standards and local agency needs.

-   **Version 2.14.0 - November 2025**
    -   What's New
        -   1. Introduced new Multimedia production equipment model categories. These model categories improve visibility, tracking, and management of complex assets used by broadcasters, studios, and production houses.
            -   Multimedia Production Equipment
            -   Media Control and Routing Equipment
            -   Contribution Equipment
            -   Audio Production Equipment
            -   Video Production Equipment
            -   Video Playout Equipment
            -   Video Precision Monitor
            -   Signal Processor and Amplifier
            -   Broadcast Sync Generator
            -   Teleprompter
            -   Production Camera
            -   Stage and Studio Lighting
        -   2. Created the new Multimedia Production Equipment Model \(sn\_ent\_mm\_prod\_equip\_model\) class and Multimedia Production Equipment Asset \(sn\_ent\_mm\_prod\_equip\_asset\) class.
-   **Version 2.13.0 - September 2025**
    -   New:
        -   System and Smart Card Model \(sn\_ent\_system\_smart\_card\_model\) extends Enterprise Model \(sn\_ent\_model\)
        -   Payment Card Model \(sn\_ent\_payment\_card\_model\) extends System and Smart Card Model \(sn\_ent\_system\_smart\_card\_model\)
        -   System and Smart Card Asset \(sn\_ent\_system\_smart\_card\_asset\) extends Enterprise Asset \(sn\_ent\_asset\)
    -   Fixed: The ability to remove non-required model components from complex models.
-   **Version 2.12.0 - August 2025**
    -   New:
        -   Added a new CI class \(cmdb\_ci\_good\) to the "Enterprise" model category.
        -   Added the Classifications reference column to the Product Model \(cmdb\_model\) table.
        -   In the model category table, new associations have been made:
            -   New CI classes, including Fuse Alarm Panel \(cmdb\_ci\_fuse\_alarm\_panel\), Power Panel \(cmdb\_ci\_power\_panel\), Rectifier \(cmdb\_ci\_rectifier\), Transformer \(cmdb\_ci\_transformer\), Switchgear \(cmdb\_ci\_switchgear\), Circuit Breaker \(cmdb\_ci\_circuit\_breaker\), Inverter, Maintenance Bypass Panel \(cmdb\_ci\_maintenance\_bypass\_panel\), and Remote Power Panel \(cmdb\_ci\_remote\_power\_panel\).These classes are associated with the asset class Facility asset \[sn\_ent\_facility\_asset\] and the parent category \[Facilities\]. New CI classes including Rack Rail \(cmdb\_ci\_rack\_rail\), Wire Manager \(cmdb\_ci\_wire\_manager\), and Rack PDU \(cmdb\_ci\_rack\_pdu\) with the asset class Hardware \[alm\_hardware\] and the parent category \[Hardware\]. All these records will be added when the CMDB CI Class app is installed.
            -   Seeded the Classification table with a subset of UNSPSC codes.
            -   Added new CI Classes for Enterprise Model categories that were missing CI classes: Added performance columns on the new KPI table - sn\_ent.
    -   Updated:
        -   The asset table list view with the most useful columns.
        -   Asset unique identifiers can now be enforced using IRE rules with additional validations in asset forms.
        -   Admin users can set unique identifiers for assets, such as asset tags, serial numbers, and/or MAC addresses, using IRE rules for each model category.
        -   Customers are now able to enforce the uniqueness of serial numbers and MAC addresses for each manufacturer.
        -   Unique asset identifiers are enforced across all asset entry points: manual asset creation, asset onboarding, asset receiving, ASN, and bulk import.
    -   Removed:
        -   Moved the failure likelihood and the failure impact columns from the enterprise model to the cmdb\_model.
        -   Moved the failure likelihood and the failure impact columns from the enterprise asset table to alm\_asset.
-   **Version 2.10.1 - March 2025**
    -   New:
        -   Created a new table, the AI System Component Product Model \(cmdb\_ai\_system\_component\_product\_model\), extending the Software Component Model \(cmdb\_sw\_component\_model\) table.
        -   Developed a new fix script to deprecate the tables for upgrade customers. Added new fields for Model Card and Dataset Card on the alm\_ai\_model\_digital\_asset and alm\_ai\_dataset\_digital\_asset.
    -   Removed:
        -   Removed the cmdb\_software\_component\_product\_model and cmdb\_ai\_system\_product\_model tables.
        -   Removed the Documentation field from both the AI model product model and the AI dataset product model.
-   **Version 2.10.0 - February 2025**

    Updated product and asset models to build enterprise AI inventories that include AI systems \(AI use cases\), AI models, datasets, prompts, and their relationships.

-   **Version 2.8.1 - January 2025**
    -   Fixed the following errors in the firmware model UI and firmware normalization:
        -   Added default views for the firmware UI.
        -   Updated the display name calculation for firmware discovery models.
-   **Version 2.9.0 - December 2024**

    New: Added product and asset models to build an Enterprise AI inventory that includes AI systems \(AI use cases\), AI models, datasets, and prompts and their relationships.

-   **Version 2.8.0 - November 2024**
    -   New:
        -   Added the Firmware model \(sn\_ent\_firmware\_model\) table as an extension of the Software component model table.
        -   Added the Discovered firmware model \(sn\_ent\_discov\_firmware\_model\) table as an extension of the Discovered SW component model table.
        -   Added the Firmware installation \(cmdb\_firmware\_install\) table as an extension of the Software component model table.
        -   Added the Firmware model normalization \(sn\_itam\_firmware\_model\_norm\) table.
    -   Fixed: The classification reference field should show the tree picker.
-   **Version 2.7.0 - August 2024**
    -   New:
        -   Added the following model categories:
            -   Universal Customer Premises Equipment
            -   Session Border Controller \(SBC\)
            -   Network
    -   Changed: Updated Network model category as a parent to existing TNI model categories.
    -   Fixed:
        -   Report view ACLs
        -   Table ACL Bypass via GlideRecord Encoded Query
-   **Version 2.6.0 - June 2024**
    -   New:
        -   Added the following model categories:
            -   Patient Monitoring
            -   Patient Implant
            -   Surgical Instrument
            -   Clinical Device
            -   Lab Equipment
            -   Diagnostic Imaging
            -   Therapeutic Device
            -   Dental Equipment
            -   Operational Equipment
-   **Version 2.5.0 - May 2024**
    -   New:
        -   Added the new Social benefit model \(sn\_ent\_social\_benefit\_model\) table as an extension of the Service model \(cmdb\_service\_product\_model\) table.
        -   Added the new API and Managed API model categories.
    -   Fixed:
        -   Model component business rule by adding the missing filter condition in which the parent status is In Production.
        -   Security ACLs.
-   **Version 2.4.0 - February 2024**
    -   New:
        -   The topology model table was added as an extension of the product model.
        -   The network topology model table was added as an extension of the topology model.
        -   New cable model tables were added as extensions from the enterprise good model table.
        -   New strand model tables were added as extensions from the enterprise good model table.
        -   For the medical device model category, is\_product\_instance is set to true by default.
        -   For the medical device model category, If the product\_instance\_identifier\_configuration table is available then serial number, parent asset and model\_component\_id records will be created.
    -   Fixed: Report view ACLs.
-   **Version 2.3.1 - January 2024**

    Fixed: Add security\_attribute as UserIsAuthenticated for Empty ACLs.

-   **Version 2.3.0 - November 2023**
    -   New:
        -   Added a new model table:
            -   The permit model table was added as an extension of the base contract model table.
            -   New service model tables were added as extensions from the base service model table. Extensions include medical insurance service tables among other service tables.
    -   Fixed:
        -   Allow technician to view model classification field on asset form view.
        -   Report view ACLs.
-   **Version 2.2.0 - August 2023**
    -   Changed:
        -   Business rule condition for importing model components.
        -   Moved the CRUD operation validation in the "Prevent changing model component" business rule for bypassing "model component in production check" while inserting model components in bulk imports.
        -   Classification validations:
            -   Added a reference qualifier to parent classifications so that they are filtered based on the source.
            -   The source is auto-populated based on the parent classification.
            -   The code/description is mandatory for creating classifications.
            -   Fixed the display name calculation.
        -   Validate categories based on parent and children codes in classification.
        -   Allow the addition of non-required components to in-production.
        -   Deactivated the UI policy that sets a new asset to the default BUILD state.
-   **Version 2.1.0 - May 2023**
    -   New:
        -   Added new model classes for Drug, Vaccination, and Medication
        -   Added new role: sn\_ent.classification\_manager
        -   Added new fields on sn\_ent\_model\_classification
            -   Parent
            -   Model categories
            -   Classification \(display\_name\)
            -   Path \(internal hidden field\)
        -   Added new ACLs on sn\_ent\_model\_classification
            -   Read for model\_manager and sn\_ent.classification\_manager
            -   Write for sn\_ent.classification\_manager
            -   Create for sn\_ent.classification\_manager
        -   Added new ACLs on sn\_ent\_model\_classification\_source
            -   Read for sn\_ent.classification\_manager
            -   Write for sn\_ent.classification\_manager
            -   Create for sn\_ent.classification\_manager
-   **Version 2.0.2 - March 2023**

    Fixed: Include the model number in the model display name.

-   **Version 2.0.1 - March 2023**

    Fixed: On the Model form, the Model classification pop-up should be accessed for sn\_eam.enterprise\_asset\_manager

-   **Version 2.0.0 - February 2023**
    -   New: Added Enterprise asset class attributes to be tracked in the activity log.
    -   Changed:
        -   Changed the sn\_ent\_asset form to read-only for assets with unknown models.
        -   Moved the model component from the sn\_eam to sn\_ent scope.
        -   Added a default view for enterprise model tables.
        -   Added a BR on sn\_ent\_asset to check if the asset class, model class, and model category are matching.
    -   Fixed: Fixed an issue where the creation of a new OT CI resulted in the "Selected model is not in Production" error message.
-   **Version 1.2.3 - January 2023**
    -   Fixed:
        -   Not allowing the model to select multiple model categories for ent models.
        -   Model component association with child asset to identify specific model component moved to sn\_ent.
        -   Adding model components for the consumable enterprise model is not allowed when only sn\_ent is installed without sn\_eam.
        -   Allow unknown model to be referenced via CI sync for ent assets.
-   **Version 1.2.2 - November 2022**
    -   New:
        -   New Product Model class Medical Device model \[sn\_ent\_medical\_device\_model\] added as an extension of Medical model \[sn\_ent\_medical\_model\].
        -   Add allow\_alt\_maintenance column with data type as boolean to sn\_ent\_model table.

**Parent Topic:**[ServiceNow Store - IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itam-highlight.md)

