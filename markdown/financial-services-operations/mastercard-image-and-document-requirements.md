---
title: Mastercard document requirements
description: Learn about Mastercard requirements for dispute supporting documents and images.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Mastercard, Integrate, Financial Services Operations \(FSO\)]
---

# Mastercard document requirements

Learn about Mastercard requirements for dispute supporting documents and images.

## Document requirements and acceptance criteria

-   Mastercom supports `.jpeg`, `.tiff`, and `.pdf` files only.
-   Document names must not exceed 16 characters.
-   The total size of all documents for one transaction must not exceed 18MB or 18000000 bytes.

    **Note:** Mastercom recommends keeping the total size of all documents for one transaction under 14.5MB or 14500000 bytes to improve performance.

-   Document names must use only English characters or numbers. They must not contain special characters or spaces within the zip file name \(when attaching multiple images for a single transaction\) or in file names within the zip.
-   Documents must not contain extensive graphics or color elements.
-   Document or image resolution must not exceed 300 X 300 DPI, and the pixel count must be less than 30000000.

## Valid image format

Mastercom supports the following image formats:

-   `TIFF_UNCOMPRESSED`
-   `TIFF_HUFFMAN`
-   `TIFF_G3_FAX`
-   `TIFF_LZQ`
-   `TIFF_G4_FAX`
-   `JPEG`
-   `TIFF_PACK`
-   `TIFF_LZW`
-   `TIFF_2D`
-   `CCITT_G3`
-   `CCITT_G4`
-   `TIFF_JPEG`
-   `TIFF_ABIC`
-   `TIFF_ABIC_BW`
-   `TIFF_G4_FAX_FO`
-   `CCITT_G4_FO`
-   `CCITT_G3_FO`
-   `TIFF_JBIG`
-   `TIFF_G4_FAX_STRIP`
-   `JPEG2000`
-   `TIFF_JPEG7` with single strip
-   `PDF`
-   `PDF_15`
-   `PDF_LZW`
-   `PDF_16`
-   `TIFF_LZWWINFAX`
-   `NCR`

