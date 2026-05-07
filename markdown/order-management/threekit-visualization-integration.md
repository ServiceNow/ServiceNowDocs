---
title: Integrating Threekit visualization
description: Integrate Threekit for visualization. Sync configuration inputs with visual updates to enhance user experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating CPQ with visualization tools, CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Integrating Threekit visualization

Integrate Threekit for visualization. Sync configuration inputs with visual updates to enhance user experience.

CPQ can share field values with Threekit so that Threekit visualization is updated in real time as the user changes CPQ configuration inputs.

Integration between CPQ and Threekit is accomplished in the blueprint layout definition. The following layout CSV file contains a sample of how the CPQ administrator defines where the Threekit visualization will be rendered in the UI, specifies the Threekit environment authorization token, and identifies the CPQ field data to be sent.

[Layout\_ThreeKit\_in\_sidebar \[Google Sheet\]](https://docs.google.com/spreadsheets/d/16peVBjoVJoaGfNgXZYzbegAjBOUeUHZB5Cgejf0RPlw/edit?usp=sharing)

Notes:

-   In the layout definition sample, the Threekit rendering displays in a sidebar BasicContainer positioned on the upper right of the UI.
-   The JSON provided in the `value` column of the ThreeKit element row contains the following syntax:

    ```
    
    {  
      "authToken": "3KIT_AUTH_TOKEN",
      "assetIdField": "<LGK field that holds 3KIT Asset ID",
      "apiSubdomain": "exampleThreekitSubdomain"
      "eventFields": {
        "LGK_FIELD1_VARNAME": "3KIT_FIELD1_VARNAME",
        "LGK_FIELD2_VARNAME": "3KIT_FIELD2_VARNAME",
        "LGK_FIELD3_VARNAME": "3KIT_FIELD3_VARNAME"
      }
    }
    ```

-   `authToken`: an authorization token provided by the Threekit application environment.

    **Important:** The authToken is how Threekit determines which of its environments will serve the visual asset: production or non-production. Therefore, be sure that the production CPQ environment passes the Threekit production authToken; nonproduction CPQ environments must pass the Threekit non-production authToken.

    When copying a layout from one CPQ environment to another, be aware that this manual edit must be made. Otherwise, non-production Threekit assets may be inadvertently displayed in CPQ production layouts.

-   `assetIdField` defines the name of the CPQ text field that holds the Threekit asset IDs, as provided by Threekit. In this way, CPQ can pass a dynamic Threekit asset ID. This helps Threekit optimize image load times. This feature provides flexibility, should the Threekit model need to be broken into two or more asset definitions to facilitate a better user experience.

    **Note:** If your CPQ blueprint only passes one static Threekit asset ID, you can replace the `assetIdField` parameter with `assetId: <hard-coded Threekit Asset ID>`.

-   `apiSubdomain`: The subdomain of your Threekit environment URL.
-   `eventFields` contains key-value pairs where each key is the variable names of the CPQ field passed to Threekit. The corresponding values are the variable names, as defined in Threekit.

To learn more about the use of Threekit visualization with a set repeater, see [Use case: Pairing set repeaters and visualization components](use-case-pairing-set-repeaters-and-visualization-components.md)

For a discussion of the features available in supported visualization applications in integration with CPQ, see [Integrating CPQ with visualization tools](logik-io-integration-wtih-visualization-tools.md).

