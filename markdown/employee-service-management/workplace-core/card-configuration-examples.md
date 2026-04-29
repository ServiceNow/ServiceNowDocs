---
title: Card Configuration examples
description: Add buttons, fields, and sections to the workplace card configuration.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workplace Core references, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Card Configuration examples

Add buttons, fields, and sections to the workplace card configuration.

**Note:** The following examples are to customize the card configurations in Workplace Core. For more information about configuring the cards, see [Configure a workplace card](../task/configure-workplace-card.md).

## Customizing the card style

Navigate to **All** &gt; **Service Portal** &gt; **CSS**, then customize the `wsdConfigurableCard` record based on your preference. You can override the styles based on the type of card you want to customize. For example:

```css
/* Customizing the profile image size for the user card */
.wsdConfigurableUserCard {
    .profile-image {
        width: 100px;
        height: 100px;
        border-radius: 35px;
    }
}

```

## Adding a section

In the template \(macro\) XML code, add a `<div>` element where you want to create a section, then include other elements inside the `<div>`. For example:

```xml
<!-- The following section is to add a phone number -->
<div class="section support-section" ng-if="data.contact">
            <div class="section-label">
                <div class="label-text">{{ translations.space.supportSectionTitle }}</div>
            </div>
            <!-- The following link specifies the phone number fetched from the data -->
            <a href="tel:{{ data.phone }}" class="section-content section-content-text">
                {{ data.phone }}
            </a>
        </div>

        <!-- The following div inserts a divider between sections -->
        <div class="divider" ng-if="mustDisplayDivider()"></div>

        <!-- The following section is to add extra services -->
        <div class="section book-services-section" ng-if="data.link">
            <div class="section-label">
                <div class="label-text">{{ translations.space.bookServicesSectionTitle }}</div>
            </div>
            <!-- The following link specifies the services link fetched from the data -->
            <a href="{{ data.link }}" class="section-content section-content-link">
                {{ data.link }}
            </a>
        </div>
```

## Adding a button

Add the logic for the button in the `WSDConfigurableCardDataInjector` script include. Make sure to add the logic inside the `extendCardsData` method. For example:

```javascript
/* Adding functionality for a custom button */
extendCardsData: function(cards) {
    cards.forEach(function(card) {
        if (card.type === 'space') {
            card.data.actions.secondary.push({
                label: 'Custom Action',
                id: 'custom_action',
                action: 'custom_action',
                isDisabled: false,
                type: 'secondary'
            });
        }
    }
});
```

**Note:** Buttons are displayed in the `Primary action buttons` section of the card.

## Adding a field

In the template \(macro\) XML code, add a `<div>` element in the section that requires a new field, then add the logic to populate the field value in the `WSDConfigurableCardDataInjector` script include. For example:

```xml
<!-- Adding a new row with a new field -->
<div class="info-row" ng-if="data.usable_size_sq_meter">
<div class="info-icon">
<i class="fa fa-arrows-alt"></i>
</div>
<div class="info-text">{{ data.usable_size_sq_meter }}m square</div>
</div>
```

```javascript
/* Custom logic to populate the field value */
cards.forEach( function(card) {
    if (card.type ==='space') {
        var spaceGr.get(card.data.sysId)) {
            card.data.usable_size_sq_meter = spaceGr.getValue('usable_size_sq_meter');
        }
    }
});
```

## Adding custom logic for a card

You can add custom logic for a card in the `WSDConfigurableCardDataInjector` script include.

In the `extendCardsData` method, add the custom logic to provide data for the new section to the card. For example, to modify the card title based on a building name:

```javascript
extendCardsData: function(cards) {
    /* Modify card title based on the building display name */
    cards.forEach(function(card) {
        if (card.data.building && card.data.building.displayValue === 'HQ') {
        card.data.title = '[HQ] ' + card.data.title;
        }
    });
    return cards;
},
```

## Hiding an element

In the template \(macro\) XML code, delete the XML tag for the section that you want to remove, or surround it in a comment block. For example:

```xml
<!-- The following section is in a comment block, therefore hidden on the card -->
<!-- <div class="info-row" ng-if="data.usable_size_sq_meter">
<div class="info-icon">
<i class="fa fa-arrows-alt"></i>
</div>
<div class="info-text">{{ data.usable_size_sq_meter }}m square</div>
</div> -->
```

After hiding the element, make sure that you remove the custom logic, or surround it in a comment block. For example:

```javascript
/* The following method is in a comment block, therefore is not run on the card */
/* cards.forEach( function(card) {
    if (card.type ==='space') {
        var spaceGr.get(card.data.sysId)) {
            card.data.usable_size_sq_meter = spaceGr.getValue('usable_size_sq_meter');
        }
    }
}); */
```

**Parent Topic:**[Workplace Core references](../concept/wsd-references.md)

**Related topics**  


[Components installed with Workplace Core](components-installed-with-workplace-service-delivery.md)

[Properties installed with Workplace Core](properties-installed-with-workplace-service-delivery.md)

[Workplace Profile Location Assignment form](wsd-location-assignment-form.md)

[Workplace location assignment anomaly types](location-assignment-anomaly-types.md)

[Reserve a space form](reserve-space-form.md)

