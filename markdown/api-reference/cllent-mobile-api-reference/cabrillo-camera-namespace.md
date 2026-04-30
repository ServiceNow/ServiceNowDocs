---
title: cabrillo.camera - Client
description: Cabrillo JS camera functions to provide camera access for bar code scanning.Provides a standard interface for scanning bar codes. Use this to present a bar code scanner and capture scanned result.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.camera - Client

Cabrillo JS camera functions to provide camera access for bar code scanning.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.camera - getBarcode\(\)

Provides a standard interface for scanning bar codes. Use this to present a bar code scanner and capture scanned result.

Supported bar code types.

-   1D bar codes: EAN-13, EAN-8, UPC-A, UPC-E, Code-39, Code-93, Code-128, ITF
-   2D bar codes: QR Code, Data Matrix, PDF-417, AZTEC

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|promise|Resolves to a bar code string, or if the operation fails, an error.|

```
cabrillo.camera.getBarcode().then(function(barcode) {
    if (barcode) {
        console.log('Scanned barcode.', barcode);
    } else {
        console.log('User cancelled scanning barcode.');
    }
}, function(error) {
    console.log('Failed to scan barcode.', error);
});
```

