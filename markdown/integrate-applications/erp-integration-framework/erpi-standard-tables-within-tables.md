---
title: Standard Zero Copy Connector for ERP fields within remote tables
description: The standard ERP \(Enterprise Resource Planning\) remote tables available for use in Zero Copy Connector for ERP contain fields from additional SAP tables.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Standard tables, fields, and models, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Standard Zero Copy Connector for ERP fields within remote tables

The standard ERP \(Enterprise Resource Planning\) remote tables available for use in Zero Copy Connector for ERP contain fields from additional SAP tables.

The standard remote tables contain the following additional fields. For details on the standard tables, see [Standard remote tables for Zero Copy Connector for ERP](erpi-standard-remote-tables.md).

|Remote table|Source table|ERP field name|Mapped field name|
|------------|------------|--------------|-----------------|
|SAP Sales Document|VBAK|VBELN|document\_number|
|SAP Sales Document|VBAK|ERDAT|date\_of\_document|
|SAP Sales Document|VBAK|ERZET|time\_of\_document|
|SAP Sales Document|VBAK|VKORG|sales\_organization|
|SAP Sales Document|VBAK|VBTYP|document\_category|
|SAP Sales Document|VBAK|AUART|document\_type|
|SAP Sales Document|VBAK|AUGRU|order\_reason|
|SAP Sales Document|VBAK|LIFSK|delivery\_block|
|SAP Sales Document|VBAK|FAKSK|billing\_block|
|SAP Sales Document|VBAK|KUNNR|customer\_number|
|SAP Sales Document|VBAK|AUFNR|order\_number|
|SAP Sales Document|VBAK|NETWR|document\_value|
|SAP Sales Document|VBAK|WAERK|currency\_code|
|SAP Sales Document|VBUK|LFGSK|delivery\_status|
|SAP Sales Document|VBAP|MATNR|material\_number|
|SAP Sales Document|VBAP|ARKTX|material\_description|
|SAP Sales Document|VBAP|KWMENG|ordered\_quantity|
|SAP Sales Document|VBAP|KLMENG|confirmed\_quantity|
|SAP Sales Document|VBAP|NETWR|item\_value|
|SAP Sales Document|VBAP|VRKME|sales\_unit|
|SAP Sales Document|VBAP|ROUTE|delivery\_route|
|SAP Sales Document|MARA|MTART|material\_type|
|SAP Sales Document|VBUP|GBSTA|overall\_item\_status|
|SAP Sales Customer|KNA1|KUNNR|customer\_number|
|SAP Sales Customer|KNA1|LAND1|country\_code|
|SAP Sales Customer|KNA1|NAME1|name|
|SAP Sales Customer|KNA1|ORT01|city|
|SAP Sales Customer|KNA1|PSTLZ|postal\_code|
|SAP Sales Customer|KNA1|STRAS|street|
|SAP Sales Customer|KNA1|STKZU|vat\_liable|
|SAP Sales Customer|KNA1|STCEG|vat\_reg\_number|
|SAP Sales Customer|KNVV|VKORG|sales\_organization|
|SAP Sales Customer|KNVV|VTWEG|distribution\_channel|
|SAP Sales Customer|KNVV|SPART|division|
|SAP Sales Customer|KNVV|INCO1|inco\_terms|
|SAP Customer Invoice|VBRK|VBELN|document\_number|
|SAP Customer Invoice|VBRK|FKART|billing\_type|
|SAP Customer Invoice|VBRK|WAERK|currency\_code|
|SAP Customer Invoice|VBRK|ZTERM|payment\_terms|
|SAP Customer Invoice|VBRK|NETWR|document\_value|
|SAP Customer Invoice|VBRK|KUNRG|payer|
|SAP Customer Invoice|VBUK|GBSTK|overall\_document\_status|
|SAP Customer Invoice|VBRP|MATNR|material\_number|
|SAP Customer Invoice|VBRP|ARKTX|material\_description|
|SAP Customer Invoice|VBRP|NETWR|item\_value|
|SAP Customer Invoice|VBRP|FKLMG|billing\_quantity|
|SAP Customer Invoice|VBRP|VRKME|sales\_unit|
|SAP Customer Invoice|VBRP|SHKZG|is\_returns\_item|
|SAP Customer Invoice|VBUP|GBSTA|overall\_item\_status|
|SAP Sales Organization|TVKO|VKORG|sales\_organization|
|SAP Sales Organization|TVKO|EKORG|purchase\_organization|
|SAP Sales Organization|TVKO|BUKRS|company\_code|
|SAP Purchase Document|EKKO|EBELN|document\_number|
|SAP Purchase Document|EKKO|BUKRS|company\_code|
|SAP Purchase Document|EKKO|BSTYP|document\_category|
|SAP Purchase Document|EKKO|LIFNR|vendor\_number|
|SAP Purchase Document|EKKO|ZTERM|payment\_terms|
|SAP Purchase Document|EKKO|EKORG|purchase\_organization|
|SAP Purchase Document|EKKO|WAERS|currency\_code|
|SAP Purchase Document|EKKO|IHREZ|ext\_reference|
|SAP Purchase Document|EKKO|RESWK|supplying\_plant|
|SAP Purchase Document|EKKO|BEDAT|date\_of\_document|
|SAP Purchase Document|EKPO|MATNR|material\_number|
|SAP Purchase Document|EKPO|EMATN|supplier\_material\_number|
|SAP Purchase Document|EKPO|MENGE|ordered\_quantity|
|SAP Purchase Document|EKPO|MEINS|order\_unit|
|SAP Purchase Document|EKPO|NETPR|item\_value|
|SAP Purchase Document|EKPO|MWSKZ|vat\_applicable|
|SAP Purchase Document|EKPO|ELIKZ|fully\_delivered|
|SAP Purchase Document|EKPO|REPOS|fully\_invoiced|
|SAP Material Stock|MARA|MATNR|material\_number|
|SAP Material Stock|MARA|MTART|material\_type|
|SAP Material Stock|MARA|MATKL|material\_class|
|SAP Material Stock|MARA|NTGEW|net\_weight|
|SAP Material Stock|MARA|EANNR|ean\_number|
|SAP Material Stock|MARA|EAN11|ean11\_number|
|SAP Material Stock|MARA|MSTAE|material\_status|
|SAP Material Stock|MAKT|MAKTX|material\_description|
|SAP Material Stock|MARD|WERKS|plant|
|SAP Material Stock|MARD|LGORT|storage\_location|
|SAP Material Stock|MARD|LABST|quantity|
|SAP Material Stock|MARD|DLINL|date\_of\_count|
|SAP Vendor Invoice|RSEG|BELNR|document\_number|
|SAP Vendor Invoice|RSEG|GJAHR|document\_year|
|SAP Vendor Invoice|RSEG|EBELN|purchase\_document\_number|
|SAP Vendor Invoice|RSEG|EBELP|purchase\_document\_item|
|SAP Vendor Invoice|RSEG|MATNR|material\_number|
|SAP Vendor Invoice|RSEG|BUKRS|company\_code|
|SAP Vendor Invoice|RSEG|WERKS|plant|
|SAP Vendor Invoice|RSEG|WRBTR|amount|
|SAP Vendor Invoice|RSEG|SHKZG|credit\_debit\_indicator|
|SAP Vendor Invoice|RSEG|MWSKZ|vat\_applicable|
|SAP Vendor Invoice|RSEG|MENGE|quantity|
|SAP Purchasing Organization|T024E|EKORG|purchase\_organization|
|SAP Purchasing Organization|T024E|EKOTX|name|
|SAP Purchasing Organization|T024E|BUKRS|company\_code|
|SAP Sales Delivery|LIKP|VBELN|document\_number|
|SAP Sales Delivery|LIKP|KUNNR|customer\_number|
|SAP Sales Delivery|LIKP|ERDAT|date\_of\_document|
|SAP Sales Delivery|LIKP|ERZET|time\_of\_document|
|SAP Sales Delivery|LIKP|VKORG|sales\_organization|
|SAP Sales Delivery|LIKP|LFART|delivery\_type|
|SAP Sales Delivery|LIKP|ROUTE|delivery\_route|
|SAP Sales Delivery|VBUK|GBSTK|overall\_document\_status|
|SAP Sales Delivery|LIPS|MATNR|material\_number|
|SAP Sales Delivery|LIPS|CHARG|batch\_number|
|SAP Sales Delivery|LIPS|WERKS|plant|
|SAP Sales Delivery|LIPS|LFIMG|quantity|
|SAP Sales Delivery|LIPS|NTGEW|net\_weight|
|SAP Sales Delivery|LIPS|GEWEI|delivery\_unit|
|SAP Sales Delivery|LIPS|VOLUM|volume|
|SAP Sales Delivery|LIPS|VOLEH|volume\_unit|
|SAP Sales Delivery|LIPS|ARKTX|material\_description|
|SAP Vendor|LFA1|LIFNR|vendor\_number|
|SAP Vendor|LFA1|NAME1|name|
|SAP Vendor|LFA1|ORT01|city|
|SAP Vendor|LFA1|PSTLZ|postal\_code|
|SAP Vendor|LFA1|STRAS|street|
|SAP Vendor|LFA1|STCEG|vat\_reg\_number|
|SAP Vendor|LFA1|WERKS|plant|
|SAP Vendor|LFM1|EKORG|purchase\_organization|
|SAP Vendor|LFM1|WEBRE|gr\_invoice\_indicator|
|SAP Sales Revenue Recognition|VBREVK|VBELN|document\_number|
|SAP Sales Revenue Recognition|VBREVK|POSNR|document\_item|
|SAP Sales Revenue Recognition|VBREVK|SAKRR|accr\_val\_clearing\_account\_number|
|SAP Sales Revenue Recognition|VBREVK|SAKRRK|offset\_clearing\_account\_number|
|SAP Sales Revenue Recognition|VBREVK|ACC\_VALUE|total\_accrued\_value|
|SAP Sales Revenue Recognition|VBREVK|WRBTR|amount|
|SAP Sales Revenue Recognition|VBREVK|RVAMT|revenue\_amount|
|SAP Sales Revenue Recognition|VBREVK|WAERK|currency\_code|
|SAP Country|T005|LAND1|country\_code|
|SAP Country|T002|SPRAS|language\_code|
|SAP Country|T002|LAISO|language\_iso\_code|
|SAP Country|T005T|LANDX|description|
|SAP Language|T002|SPRAS|language\_code|
|SAP Language|T002|LAISO|language\_iso\_code|
|SAP Currency|TCURC|WAERS|currency\_code|
|SAP Currency|TCURC|ISOCD|currency\_iso\_code|
|SAP Currency|TCURT|LTEXT|description|
|SAP Distribution Channel|TVTW|VTWEG|distribution\_channel|
|SAP Distribution Channel|TVTWT|VTEXT|description|
|SAP Division|TSPA|SPART|division|
|SAP Division|TSPAT|VTEXT|description|
|SAP Company Code|T001|BUKRS|company\_code|
|SAP Company Code|T001|BUTXT|description|
|SAP Company Code|T001|LAND1|country\_code|
|SAP Company Code|T001|WAERS|currency\_code|
|SAP Company Code|T001|SPRAS|language\_code|
|SAP Transport|E071|AS4DATE|date\_of\_transport|
|SAP Transport|E071|AS4TIME|time\_of\_transport|
|SAP Transport|E071|AS4USER|user|
|SAP Transport|E071|TRFUNCTION|type|
|SAP Transport|E071|TRKORR|number|
|SAP Transport|E071|TRSTATUS|status|
|SAP Transport|E071|OBJECT|object\_type|
|SAP Transport|E071|OBJ\_NAME|object\_name|
|SAP Transport|E071|PGMID|program\_id|

**Parent Topic:**[Zero Copy Connector for ERP standard tables, fields, and models](erp-canvas-standard-tables-and-fields-landing.md)

