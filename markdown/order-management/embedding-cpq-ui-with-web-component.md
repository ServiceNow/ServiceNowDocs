---
title: Embedding the CPQ UI with the CPQ Web Component
description: By using the CPQ Web Component, you can embed the Logik UI in a web page without using an iframe. Because the component's UI is compatible with themes, users can easily edit the look of the UI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Embedding the CPQ UI with the CPQ Web Component

By using the CPQ Web Component, you can embed the Logik UI in a web page without using an iframe. Because the component's UI is compatible with themes, users can easily edit the look of the UI.

The CPQ Web Component allows a user to embed the CPQ UI directly to a web page without an iframe. The UI of the Web Component is compatible with themes to allow users to easily edit the look of the UI.

To use the Web Component, you must have:

-   A configurable product associated to a deployed blueprint
-   A CPQ runtime token that includes the destination URL as the origin Website URL whitelisted in the GCP properties

Contextual information on the page \(such as a SKU in the page URL\) is accessible to the Web Component with minimal customization. The Web Component also:

-   Removes the need to use an iframe to embed Logik UI, avoiding security restrictions and issues inherent to iframes
-   Dispatches native HTML events that can be listened for anywhere on a page
-   Reduces integration complexity; for example, its Web component orchestrates API calls for UI display and configuration
-   Provides greater control over Logik on your site with access to the HTML directly on the page, more seamlessly integrating with the parent page
-   Is compatible with custom themes

## Embedding the CPQ Web Component

The Web Component can be added to any page where you can add HTML. The only required fields to initialize the Web Component are the URL, the runtime token, and the configurable product ID.

## Example

The following sample code includes comments to provide more details on how the Web Component works and provides examples for reference.

It includes minimal code that can be easily added to a container or embed components. A Product ID must be manually entered.

```
<script
  src="https://TENANT.SECTOR.logik.io/ui/wc-build/logik-wc.es.js"
  type="module"
  ></script>
  <logik-ui 
  runtime-token="RUNTIME_TOKEN"
  tenant-api-url="TENANT.SECTOR.logik.io"
  product-id="PRODUCT_ID"
  >
  </logik-ui>
```

The following sample code represents a full-page example. It lets the user easily pass multiple parameters and read a product ID from the page.

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Web Component Sandbox</title>
    <script
      type="module"
      src="https://renderdraw02.demo01.logik.io/ui/wc-build/logik-wc.es.js"
    ></script>
  </head>
  <body>
    <logik-ui></logik-ui>

    <script>
      // Type Definitions
      /**
       * @typedef {Object} BomProduct
       * @property {string} id - Product identifier
       * @property {number} price - Unit price of the product
       * @property {number} quantity - Quantity of the product
       * @property {('SALES'|'MANUFACTURING')} bomType - Type of BOM
       * @property {string} type - Product type (e.g., 'accessory')
       * @property {number} rollUpPrice - Rolled up price including child products
       * @property {number} extPrice - Extended price (price * quantity)
       * @property {number} level - Hierarchy level in the BOM structure
       * @property {{ selected: boolean, disabled: boolean }} selection - Selection state
       * @property {number} extList - Extended list price
       * @property {number} list - List price
       * @property {string} displayName - Display name of the product
       * @property {string|null} parentProduct - ID of parent product if nested
       */

      /**
       * @typedef {Object} BomData
       * @property {{
       *   products: Array<BomProduct>,
       *   total: number,
       *   totalPages: number,
       *   totalItems: number,
       *   errorMessage: string|null,
       *   incompletePricing: boolean
       * }} newProducts - Updated products in the BOM
       */

      /**
       * @typedef {Object} LogikConfigurationData
       * @property {string} configurationId - The unique identifier for the configuration
       * @property {string} productId - The product identifier
       * @property {Object} fields - The current state of all fields in the configuration
       * @property {BomData} [bomData] - Bill of Materials data (only present in BOM events)
       * @property {Object} [quoteData] - Quote data (only present in Quote events)
       */

      /**
       * @typedef {Object} QuoteData
       * @property {Object} quote - Quote-specific data
       * @property {string} quote.SBQQ__PricebookId__c - Pricebook identifier
       * @property {string} quote.LGK__QueriedEditAccess__c - Edit access status
       * @property {Object} product - Configured product data
       * @property {string} product.configuredProductId - ID of the configured product
       * @property {Object} product.configurationAttributes - Configuration attributes
       * @property {string} product.configurationAttributes.LGK__Logik_Id__c - Logik configuration ID
       * @property {Object} product.configurationAttributes.LGK__Configuration_Data__c - Configuration data
       * @property {Array} product.configurationAttributes.LGK__Configuration_Data__c.items - Configuration items
       * @property {Object} product.optionConfiguration - Option configuration data
       * @property {Array} product.optionConfiguration.Dynamic - Dynamic option configurations
       */

      // Configuration
      const logikUrl = 'https://renderdraw02.demo01.logik.io';
      const runtimeToken = 'YIFFI0dluM7ULhibRGR2GB_3F2npxSn_Zw';
      const productId = '01t8c00000RzlKoAAJ';

      const fields = [
        { variableName: 'exampleBooleanField', value: true },
        {
          variableName: 'exampleArrayField',
          value: ['alpha', 'delta', 'beta'],
        },
        { variableName: 'exampleStringField', value: 'left' },
        { variableName: 'exampleNumberField', value: 21 },
      ];

      /**
       * Initializes the Logik UI web component with the specified configuration parameters.
       * @param {string} productId - The unique identifier for the product. This is a configurable product id in the logik Admin
       * @param {string} runtimeToken - The authentication token for runtime access. This can be created in the logik Admin under Runtime Clients. The token must have include an origin matching the url of the page that is hosting the web component.
       * @param {string} tenantApiUrl - This should be set to the url of your logik tenant. eg https://example.demo01.logik.io
       * @param {string} [assetURL] - Optional URL for asset resources. If provided, sets the asset-url attribute. Defaults to the provided tenantApiUrl. You will most likely not need to set this.
       * @param {Array<{
       *   variableName: string,
       *   value: string | number | boolean | Array<string>
       * }>} [fields] - A list of field values to set in the initial state of the configuration.
       * @returns {void}
       */
      function initLogikUI(productId, runtimeToken, tenantApiUrl, assetURL, fields) {
        const logikuiEl = document.querySelector('logik-ui');
        logikuiEl.setAttribute('product-id', productId);
        logikuiEl.setAttribute('runtime-token', runtimeToken);
        logikuiEl.setAttribute('tenant-api-url', tenantApiUrl);
        if (assetURL) {
          logikuiEl.setAttribute('asset-url', assetURL);
        }
        if (fields) {
          logikuiEl.setAttribute('fields', JSON.stringify(fields));
        }
      }

      // Initialize the component
      initLogikUI(productId, runtimeToken, logikUrl, false, fields);

      // Event Listeners
      /**
       * Event fired when the user cancels the configuration. After this event is received,
       * the configuration will be terminated and the logik-ui component should be unmounted.
       * @event logik-ui:cancel
       * @type {CustomEvent}
       * @property {Object} detail - An empty object indicating the configuration was cancelled
       */
      window.addEventListener('logik-ui:cancel', function (event) {
        console.log('Cancel event received', event);
      });

      /**
       * Event fired when the user generates a quote. After this event is received,
       * the configuration will be terminated and the logik-ui component should be unmounted.
       * @event logik-ui:quote
       * @type {CustomEvent}
       * @property {Object} detail - The event details
       * @property {QuoteData} detail.data - The quote data
       */
      window.addEventListener('logik-ui:quote', function (event) {
        console.log('Quote event received', event);
      });

      /**
       * Event fired when the BOM changes during configuration
       * @event logik-ui:bom
       * @type {CustomEvent}
       * @property {Object} detail - The event details
       * @property {LogikConfigurationData} detail.data - The configuration data with BOM information
       */
      window.addEventListener('logik-ui:bom', function (event) {
        console.log('BOM event received', event);
      });
    </script>
  </body>
</html>
```

