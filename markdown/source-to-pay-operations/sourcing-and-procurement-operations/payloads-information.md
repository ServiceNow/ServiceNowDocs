---
title: Payloads samples and errors
description: Use the following sample payloads to enable procurement data import and export.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data source table information, Procurement File Transfer Framework, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Payloads samples and errors

Use the following sample payloads to enable procurement data import and export.

## Payloads

See the following sample payload for importing and exporting procurement records.

|Name|Sample payload|
|----|--------------|
|Invoice Import|See Spendint API - POST /sn\_spend\_intg/spendint/invoice|
|Catalog Import|See Spendint API - POST /sn\_spend\_intg/spendint/catalog|
|Availability Import|See Spendint API - POST /sn\_spend\_intg/spendint/availability|
|Shipment Import|See Spendint API - POST /sn\_spend\_intg/spendint/shipment|
|Order Acknowledgment|See Spendint API - POST /sn\_spend\_intg/spendint/orderack|
|Price Import|See Spendint API - POST /sn\_spend\_intg/spendint/price|

## Errors

This section describes the following procurement errors:

**Catalog Error \(Outbound\)**

```
{
  "root": {
    "status_message": "",
    "status_code": "Failure",
    "customer_id": "AB-1234323",
    "supplier_id": "SUP-123456",
    "error_response_body": [
      {
        "error_message": "Field Value empty/Formatting issue Negotiated currency \n",
        "mpn": "Z0WQ-20004301931",
        "sku": "55788741"
      }
    ]
  }
}
```

**Price Error \(Outbound\)**

```

{
  "root": {
    "status_message": "",
    "status_code": "Failure",
    "customer_id": "AB-1234323",
    "supplier_id": "SUP-123456",
    "error_response_body": [
      {
        "error_message": "Field Value empty/Formatting issue Negotiated currency \n",
        "mpn": "Z0WQ-20004301931"
      }
    ]
  }
}
```

**Availability Error \(Outbound\)**

```
{
  "root": {
    "status_message": "",
    "status_code": "Failure",
    "customer_id": "AB-1234323",
    "supplier_id": "SUP-123456",
    "error_response_body": [
      {
        "error_message": "Field Value empty/Formatting issue Negotiated currency \n",
        "mpn": "Z0WQ-20004301931"
      }
    ]
  }
}
```

**Shipment Error \(Outbound\)**

```
{
  "root": {
    "status_message": "",
    "status_code": "Failure",
    "customer_id": "AB-1234323",
    "supplier_id": "SUP-123456",
    "error_response_body": [
      {
        "supplier_shipment_number": "SHIPSUP00001 \n",
        "sales_order_number": "SOL0010001 \n",
        "sales_order_line_number": "SOL0010001 \n",
        "error_message": "The purchase order for this shipment does not exist \n"
      }
    ]
  }
}
```

**Invoice Error \(Outbound\)**

```
{
  "root": {
    "status_message": "",
    "status_code": "Failure",
    "customer_id": "AB-1234323",
    "supplier_id": "SUP-123456",
    "error_response_body": [
      {
        "supplier_invoice_number": "SUPINV000001 \n",
        "supplier_invoice_line_number": "SUPINVL0000001 \n",
        "sales_order_number": "SOL0010001 \n",
        "sales_order_line_number": "SOL0010001 \n",
        "error_message": "The provided invoices does not have a purchase order line number \n"
      }
    ]
  }
}
```

**Outbound Order**

```

{
  "root": {
    "order_amount": "200",
    "order_number": "PO0010001",
    "currency": "USD",
    "order_date": "01-01-2021",
    "customer_id": "AB-1234323",
    "supplier_id": "SUP-123456",
    "catalog_id": "ABC780987",
    "order_lines": [
      {
        "sku": "A20002 \n",
        "line_number":"POL0010001 \n",
        "mpn": "09876789 \n",
        "purchased_quantity": "2 \n",
        "unit": "Each \n",
        "unit_price": "USD \n",
        "ship_to": "John A \n",
        "contract_number": "VEN09000002 \n",
        "organization_id": "868979 \n",
        "enroll_in_abm": "yes",
        "shipping_address": {
          "name": "2225 Lawson Ln, Santa Clara, CA 95054, United States\n",
          "street": "2225 Lawson Ln \n",
          "city": "Santa Clara \n",
          "state": "CA \n",
          "zip_code": "95054 \n",
          "country": "Unites States of America \n"
        }
      }
    ]
  }
}
```

**Parent Topic:**[Data source table information](data-sources-info.md)

