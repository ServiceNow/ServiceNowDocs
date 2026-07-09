---
title: Combined Industrial Process Manager release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Industrial Process Manager from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-industrialprocessmanager-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Industrial Process Manager release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Industrial Process Manager from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Industrial Process Manager release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Industrial Process Manager to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The Industrial Process Manager application now has a dependency with the Operational Technology Service Management applications, which include Operational Technology Incident Management and Operational Technology Change Management. To install Industrial Process Manager on your instance, one of the following SKUs is required:

-   Operational Technology Visibility SKU
-   Operational Technology Service Management SKU
-   Any custom SKU that entitles Industrial Process Manager

</td></tr><tr><td>

Xanadu

</td><td>

The Industrial Process Manager application now has a dependency with the Operational Technology Service Management applications, which include Operational Technology Incident Management and Operational Technology Change Management. To install Industrial Process Manager on your instance, one of the following SKUs is required:

-   Operational Technology Visibility SKU
-   Operational Technology Service Management SKU
-   Any custom SKU that entitles Industrial Process Manager

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Industrial Process Manager.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Add OT devices to an equipment model entity by IP address](https://www.servicenow.com/docs/access?context=view-ot-assets-equipment-model-entity&family=washingtondc&ft:locale=en-US)**

When you manually add OT devices to the Mapped OT Devices related list in the Equipment Model Manager on the Industrial Workspace, you can add an OT device by its IP address.

-   **[Update the entity name or parent of an equipment model entity](https://www.servicenow.com/docs/access?context=update-the-name-or-parent-equipment-model-entity&family=washingtondc&ft:locale=en-US)**

Update the **Entity name** or **Parent** fields in an equipment model entity record as needed to help keep your equipment model information up to date.

-   **[Modifying the parent of an equipment model entity](https://www.servicenow.com/docs/access?context=managing-equipment-models-after-data-import&family=washingtondc&ft:locale=en-US)**

Update the parent in one or more equipment model entity records after creating an equipment model entity.

-   **[Additional AMAZING roles to access and edit OT subnet-mapping records](https://www.servicenow.com/docs/access?context=components-installed-with-industrial-process-manager&family=washingtondc&ft:locale=en-US)**

Control which users have access to and can edit OT subnet-mapping records by assigning the Amazing Reader \(sn\_ot\_amazing\_read\), Amazing Writer \(sn\_ot\_amazing\_write\), and Amazing Admin \(sn\_ot\_amazing\_admin\) roles.

-   **[Automatically assigns all OT control modules to equipment model entities based on the Owns::Owned by relationship \(sn\_otsm.subnet\_mapping.auto\_assign\_ot\_control\_modules\) system property](https://www.servicenow.com/docs/access?context=system-properties-used-by-automated-mapping-feature&family=washingtondc&ft:locale=en-US)**

Enable automatic assignments of OT control modules to equipment model entities based on the owns::owned by relationship the OT control module has with an OT control system \(or extended class\) device.

-   **[User Criteria security model](https://www.servicenow.com/docs/access?context=create-user-criteria-for-equipment-model-entity-site-users&family=washingtondc&ft:locale=en-US)**

Create and assign user criteria to control the view and edit the user access to your sites and equipment model entities with the new User Criteria security model. If you want to migrate from the site user configuration to the User Criteria security model, the ISAEntitySiteUser script was updated to query the ISA User Criteria table and calls the User Criteria API for all existing public APIs.

**Note:** If your ISA Equipment Model application version is prior to 1.0.12, you can still use the site user configuration available for the ISA Equipment Model.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Capture the mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&family=xanadu&ft:locale=en-US)**

Organize your OT device data efficiently by adding the primary equipment model entity for your OT devices. You can also automatically update the primary equipment model entity for your existing devices.

-   **[Use the Unified Map experience in the Industrial Workspace](https://www.servicenow.com/docs/access?context=unified-maps-experience-iw&family=xanadu&ft:locale=en-US)**

View the relationships between OT devices and other CIs with the Unified Map experience. You can also view related items, such as OT incidents and change requests.

-   **[Map discovery detected devices using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature](https://www.servicenow.com/docs/access?context=automatedly-map-all-ot-assets&family=xanadu&ft:locale=en-US)**

Map Discovery detected devices that have an IP address on their Network Adapter record using the AMAZING feature.

-   **[Add OT devices to an equipment model entity by IP address](https://www.servicenow.com/docs/access?context=view-ot-assets-equipment-model-entity&family=xanadu&ft:locale=en-US)**

When you manually add OT devices to the Mapped OT Devices related list in the Equipment Model Manager on the Industrial Workspace, you can add an OT device by its IP address.

-   **[Update entity name or parent entity](https://www.servicenow.com/docs/access?context=update-the-name-or-parent-equipment-model-entity&family=xanadu&ft:locale=en-US)**

Update the **Entity name** or **Parent** fields in an equipment model entity record as needed to help keep your equipment model information up to date.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Set the operational status for equipment model entity sites](https://www.servicenow.com/docs/access?context=equipment-model-workspace&family=yokohama&ft:locale=en-US)**

Set equipment model entity sites to not in use in the Industrial Workspace by selecting the **Not in use** value for the **Operational Status** field.

-   **[Filter out Not in use and Retired equipment model entities from view](https://www.servicenow.com/docs/access?context=filter-out-non-operational-equipment-model-entities&family=yokohama&ft:locale=en-US)**

Filter out **Not in use** and **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value for a site.

-   **[Add child equipment model entities to a Favorites view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&family=yokohama&ft:locale=en-US)**

Use the Favorite icon \(\[Omitted image "image.mark-as-favorite"\] Alt text:\) to add a child equipment model entity as a favorite in the Equipment Model Manager on the Industrial Workspace. You can then use the **Show Favorites** toggle to display them.

-   **[Assign Processing Order to sort equipment model entities in a site](https://www.servicenow.com/docs/access?context=view-child-entities-equipment-model-entity&family=yokohama&ft:locale=en-US)**

Use the **Processing Order** field to assign values to an equipment model entity that determines their functional importance in a site.

-   **[The Daily Activity tab in the Equipment Model view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=view-ot-eme-daily-summary&family=yokohama&ft:locale=en-US)**

View the list of previous day's activities on the **Daily Activity** tab of an OT device. The activities include adding an OT device and changing the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.

-   **[Capture the mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&family=yokohama&ft:locale=en-US)**

Organize your OT device data efficiently by adding the primary equipment model entity for your OT devices. You can also automatically update the primary equipment model entity for your existing devices.

-   **[Use the Unified Map experience in the Industrial Workspace](https://www.servicenow.com/docs/access?context=unified-maps-experience-iw&family=yokohama&ft:locale=en-US)**

View the relationships between OT devices and other CIs with the Unified Map experience. You can also view related items, such as OT incidents and change requests.

-   **[Map Discovery detected devices using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature](https://www.servicenow.com/docs/access?context=automatedly-map-all-ot-assets&family=yokohama&ft:locale=en-US)**

Map Discovery detected devices that have an IP address on their Network Adapter record using the AMAZING feature.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Discovered subnets supported by the AMAZING feature](https://www.servicenow.com/docs/access?context=automate-mappings-between-ot-assets-and-equipment-model-entity&family=zurich&ft:locale=en-US)**

Use the AMAZING feature, which uses discovered subnets, to identify OT devices and assign them to the correct equipment model entity during OT subnet mapping.

-   **[Map OT devices from the Equipment Model Manager](https://www.servicenow.com/docs/access?context=map-ot-devices-in-iw&family=zurich&ft:locale=en-US)**

Map OT devices to equipment model entities using the **Unmapped OT Devices** and the **All Devices** tabs in the Equipment Model Manager of the Industrial Workspace.

-   **[Generate a location hierarchy](https://www.servicenow.com/docs/access?context=create-location-hierarchy-isa&family=zurich&ft:locale=en-US)**

Generate a complete location hierarchy for an ISA equipment model entity tree when no locations exist to establish location references that match the ISA hierarchy.

-   **[Use the OT Network Map to visualize your OT network](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&family=zurich&ft:locale=en-US)**

Visualize your OT network, subnets, and device-to-device connections with the OT Network Map in the Industrial Workspace.

-   **[Set the operational status for equipment model entity sites](https://www.servicenow.com/docs/access?context=equipment-model-workspace&family=zurich&ft:locale=en-US)**

Set equipment model entity sites to not in use in the Industrial Workspace by selecting the **Not in use** value for the **Operational Status** field.

-   **[Filter out Not in use and Retired equipment model entities from view](https://www.servicenow.com/docs/access?context=filter-out-non-operational-equipment-model-entities&family=zurich&ft:locale=en-US)**

Filter out **Not in use** and **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value for a site.

-   **[Add child equipment model entities to a Favorites view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&family=zurich&ft:locale=en-US)**

Use the Favorite icon \(\[Omitted image "image.mark-as-favorite"\] Alt text:\) to add a child equipment model entity as a favorite in the Equipment Model Manager on the Industrial Workspace. You can then use the **Show Favorites** toggle to display them.

-   **[Assign Processing Order to sort equipment model entities in a site](https://www.servicenow.com/docs/access?context=view-child-entities-equipment-model-entity&family=zurich&ft:locale=en-US)**

Use the **Processing Order** field to assign values to an equipment model entity that determines their functional importance in a site.

-   **[The Daily Activity tab in the Equipment Model view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=view-ot-eme-daily-summary&family=zurich&ft:locale=en-US)**

View the list of previous day's activities on the **Daily Activity** tab of an OT device. The activities include adding an OT device and changing the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.


</td></tr><tr><td>

Australia

</td><td>

-   **[Discovered subnets supported by the AMAZING feature](https://www.servicenow.com/docs/access?context=automate-mappings-between-ot-assets-and-equipment-model-entity&family=australia&ft:locale=en-US)**

Use the AMAZING feature, which uses discovered subnets, to identify OT devices and assign them to the correct equipment model entity during OT subnet mapping.

-   **[Map OT devices from the Equipment Model Manager](https://www.servicenow.com/docs/access?context=map-ot-devices-in-iw&family=australia&ft:locale=en-US)**

Map OT devices to equipment model entities using the **Unmapped OT Devices** and the **All Devices** tabs in the Equipment Model Manager of the Industrial Workspace.

-   **[Generate a location hierarchy](https://www.servicenow.com/docs/access?context=create-location-hierarchy-isa&family=australia&ft:locale=en-US)**

Generate a complete location hierarchy for an ISA equipment model entity tree when no locations exist to establish location references that match the ISA hierarchy.

-   **[Use the OT Network Map to visualize your OT network](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&family=australia&ft:locale=en-US)**

Visualize your OT network, subnets, and device-to-device connections with the OT Network Map in the Industrial Workspace.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Industrial Process Manager features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Manage the Equipment Model section in the Industrial Process Manager Guided Setup](https://www.servicenow.com/docs/access?context=configuring-manufacturing-process-mgr&family=washingtondc&ft:locale=en-US)**

The Manage the equipment model section of the Industrial Process Manager Guided Setup has the following new enhancements:

    -   The Assign Users task was removed.
    -   The Create User Criteria for Site Users task was added.
    -   The Assign Site Users - Can Read task was added.
    -   The Assign Site Users - Can Edit task was added.
-   **[ISA Equipment Model enhancements](https://www.servicenow.com/docs/access?context=migrating-site-user-access-to-user-criteria-and-groups&family=washingtondc&ft:locale=en-US)**

When you upgrade to version 1.0.12 of the ISA Equipment Model, the migration from site user access to user criteria and groups begins automatically and the following changes are made:

    -   Improved site level access control to that uses user criteria to define read or write level user access to equipment model entity sites. With the additional assignment of OT viewer \(cmdb\_ot\_viewer\) or OT Editor \(cmdb\_ot\_editor\) roles, you can also have view or edit access to OT devices in the sites assigned accordingly.
    -   When you upgrade to version 1.0.12 of ISA Equipment Model, existing site user records are migrated to an improved access control model using user criteria to preserve the same access permissions. For each site with ISA Entity Site User records, the following changes occur.
        -   For users with viewer access:
            -   A new user criteria record is created and named **Read User Criteria for &lt;site name&gt; Site \[System Generated\]**
            -   A new user group with all site users from this site is created and named **Read Group for &lt;site name&gt; Site \[System Generated\]**
            -   A new record in the new Equipment Model Entity View Access table \(isa\_entity\_m2m\_user\_criteria\_can\_view\) is created with the new user criteria and user group.
        -   For users with editor access:
            -   A new user criteria record is created and named **Edit User Criteria for &lt;site name&gt; Site \[System Generated\]**
            -   A new user group with all site users from this site is created and named **Edit Group for &lt;site name&gt; Site \[System Generated\]**
            -   A new record in the new Equipment Model Entity Edit Access table \(isa\_entity\_m2m\_user\_criteria\_can\_edit\) is created with the new user criteria and user group.
    -   The Site User application menu and Site Users related list on the Equipment Model Entity record for a site is removed.
    -   All site user \(isa\_entity\_site\_user\) records are set to inactive.
    -   The **Site User – Can Read** and **Site User – Can Edit** application menu items are added to the ServiceNow AI Platform.
    -   The **Can Read Equipment Models** and **Can Edit Equipment Models** related lists are added to the Equipment Model Entity record for a site.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Viewing multiple records at once in the Equipment Model Manager](https://www.servicenow.com/docs/access?context=managing-equipment-models-after-data-import&family=yokohama&ft:locale=en-US)**

In the Equipment Model Manager of the Industrial Workspace, view multiple records and keep the record context available instead of only viewing one record at a time. When creating or opening multiple records, the records open in single row of tabs at the same level so you can navigate back to other opened records.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=zurich&ft:locale=en-US)**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Viewing multiple records at once in the Equipment Model Manager](https://www.servicenow.com/docs/access?context=managing-equipment-models-after-data-import&family=zurich&ft:locale=en-US)**

In the Equipment Model Manager of the Industrial Workspace, view multiple records and keep the record context available instead of only viewing one record at a time. When creating or opening multiple records, the records open in single row of tabs at the same level so you can navigate back to other opened records.


</td></tr><tr><td>

Australia

</td><td>

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Industrial Process Manager features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   The Site Users menu item that contained the ISA Entity Site Users \[isa\_entity\_site\_user\] table was removed from the Equipment Model - ISA module on the ServiceNow AI Platform.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Industrial Process Manager features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Industrial Process Manager.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

**Note:** Industrial Process Manager is automatically installed with Operational Technology Incident Management and Operational Technology Change Management.

</td></tr><tr><td>

Xanadu

</td><td>

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

**Note:** Industrial Process Manager is automatically installed with Operational Technology Incident Management and Operational Technology Change Management.

</td></tr><tr><td>

Yokohama

</td><td>

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Industrial Process Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Industrial Process Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Industrial Process Manager, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Industrial Process Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Industrial Process Manager we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Add Operational Technology \(OT\) devices to an equipment model entity by using the IP address.
-   Change the **Entity name** and **Parent** fields of an equipment model entity to keep your equipment model entity information up to date after you create it.
-   Modify the parent of one or more equipment model entities after the equipment model entity record is created.
-   Use the new Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) roles to control who has access to and can edit OT subnet-mapping records.
-   Control the view and edit the access to your sites and equipment model entities by using the new User Criteria security model.

 See [Manufacturing Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Organize your Operational Technology \(OT\) device data by capturing the mapped equipment model entity for an OT device.
-   View the relationships between devices and other configuration items \(CIs\) with the Unified Map experience in the Industrial Workspace.
-   Add Operational Technology \(OT\) devices to an equipment model entity by using the IP address.
-   Change the **Entity name** and **Parent** fields of an equipment model entity to keep your equipment model entity information up to date after you create it.

 See [Manufacturing Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Identify sites on your equipment model entity that aren't in use with a new **Operational Status** field value in the Industrial Workspace.
-   Filter out **Not in use** or **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value.
-   Sort equipment model entities for a Site using the new value **Processing Order**.
-   View the **Daily Activity** tab for a summarized version of the previous day's activities on Operational Technology \(OT\) devices.
-   Organize your OT device data by capturing the mapped equipment model entity for an OT device.
-   View the relationships between devices and other configuration items \(CIs\) with the Unified Map experience in the Industrial Workspace.

 See [Manufacturing Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   View both unmapped and all Operational Technology \(OT\) devices in separate tabs while mapping them to equipment model entities for an organized view of your OT devices.
-   Visualize your OT network using the OT Network Map.
-   Automatically create a location for equipment model entities to visualize your location hierarchy.
-   Use the updated Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature to uniquely identify OT devices during equipment model entity mapping.
-   Identify sites on your equipment model entity that aren't in use with a new **Operational Status** field value in the Industrial Workspace.
-   Filter out **Not in use** or **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value.
-   Sort equipment model entities for a Site using the new value **Processing Order**.
-   View the **Daily Activity** tab for a summarized version of the previous day's activities on the Operational Technology \(OT\) devices.

 See [Manufacturing Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   View both unmapped and all Operational Technology \(OT\) devices in separate tabs while mapping them to equipment model entities for an organized view of your OT devices.
-   Visualize your OT network using the OT Network Map.
-   Automatically create a location for equipment model entities to visualize your location hierarchy.
-   Use the updated Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature to uniquely identify OT devices during equipment model entity mapping.

 See for [Manufacturing Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&family=australia&ft:locale=en-US) more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

