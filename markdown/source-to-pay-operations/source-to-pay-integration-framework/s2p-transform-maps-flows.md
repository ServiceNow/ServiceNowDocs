---
title: Source-to-Pay integration framework transform maps and subflows
description: The transform maps transform the source-to-pay data from the inbound staging tables to the Source-to-Pay primary data tables. The subflows move the source-to-pay data from the outbound staging tables to a third-party ERP system.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay integration framework transform maps and subflows

The transform maps transform the source-to-pay data from the inbound staging tables to the Source-to-Pay primary data tables. The subflows move the source-to-pay data from the outbound staging tables to a third-party ERP system.

## Transform maps

The following transform maps transform the source-to-pay data from the inbound staging tables to the Source-to-Pay primary data tables.

|Transform map|Description|
|-------------|-----------|
|Load product model|Transforms product model data from the sn\_fcms\_intg\_cmdb\_model\_stage staging table to the cmdb\_model primary table.|
|Load service model|Transforms service model data from the sn\_fcms\_intg\_cmdb\_service\_model\_stage staging table to the cmdb\_service\_product\_model primary table.|
|CMN location|Transforms CMN location data from the sn\_fcms\_intg\_cmn\_location\_stage staging table to the cmn\_location primary table.|
|Master data cost center|Transforms cost center data from the sn\_fcms\_intg\_imp\_cost\_center staging table to the cmn\_cost\_center primary table.|
|Load department|Transforms department data from the sn\_fcms\_intg\_department\_stage staging table to the cmn\_department primary table.|
|ERP Plant Address|Transforms ERP plant address data from the sn\_fcms\_intg\_erp\_plant\_address\_mapping\_stage staging table to the sn\_fcms\_intg\_erp\_plant\_address\_mapping primary table.|
|Load FX currency|Transforms FX currency data from the sn\_fcms\_intg\_fx\_currency\_stage staging table to the sn\_fin\_fx\_currency primary table.|
|Load FX rate|Transforms FX rate data from the sn\_fcms\_intg\_fx\_rate\_stage staging table to the sn\_fin\_fx\_rate primary table.|
|GL account load data|Transforms GL account data from the sn\_fcms\_intg\_gl\_account\_stage staging table to the sn\_fin\_gl\_account primary table.|
|Cost allocation stage|Transforms cost allocation data from the sn\_spend\_intg\_imp\_cost\_allocation staging table to the sn\_shop\_cost\_allocation primary table.|
|Order stage|Transforms purchase order data from the sn\_fcms\_intg\_imp\_order staging table to the sn\_shop\_purchase\_order primary table.|
|Order line stage|Transforms purchase order line data from the sn\_fcms\_intg\_imp\_order\_line staging table to the sn\_shop\_purchase\_order\_line primary table.|
|Receipt stage|Transforms receipts data from the sn\_fcms\_intg\_imp\_receipt staging table to the sn\_shop\_receipt primary table. Transform legal entities:|
|Transform legal entities|Transforms legal entity data from the sn\_fcms\_intg\_legal\_entity\_stage staging table to the sn\_fin\_legal\_entity primary table.|
|Load payment terms|Transforms payment terms data from the sn\_fcms\_intg\_payment\_term\_stage staging table to the sn\_shop\_payment\_term primary table.|
|Transform office location|Transforms office location data from the sn\_fcms\_intg\_office\_location\_stage staging table to the sn\_shop\_office\_location primary table.|
|Load product category|Transforms product category data from the sn\_fcms\_intg\_cmdb\_model\_category\_stage staging table to the cmdb\_model\_category primary table.|
|Master data purchase entity|Transforms purchase entity data from the sn\_fcms\_intg\_imp\_purchase\_entity staging table to the sn\_fin\_purchasing\_entity primary table.|
|Load supplier product|Transforms supplier product data from the sn\_spend\_intg\_supplier\_product\_stage staging table to the sn\_shop\_supplier\_product primary table.|
|Transform supplier contact details|Transforms supplier contact details data from the sn\_fcms\_intg\_supplier\_contact\_inbound staging table to the vm\_vdr\_contact primary table.|
|Master data supplier|Transforms supplier data from the sn\_fcms\_intg\_imp\_supplier staging table to the sn\_fin\_supplier primary table.|
|Load legal entity-mapping data|Transforms supplier legal entity data from the sn\_fcms\_intg\_supplier\_legal\_entity\_inbound staging table to the sn\_fin\_supplier\_detail primary table.|
|Load supplier address information|Transforms supplier location data from the sn\_fcms\_intg\_supplier\_location\_inbound staging table to the sn\_slm\_m2m\_location primary table.|
|Transform supplier payment|Transforms supplier payment data from the sn\_fcms\_intg\_supplier\_payment\_inbound\_stage staging table to the sn\_fin\_supplier\_payment primary table.|
|Invoice import|Transforms invoice details from the sn\_spend\_intg\_imp\_invoice staging table to the sn\_shop\_invoice primary table.|
|Invoice line import|Transforms invoice line details from the sn\_spend\_intg\_imp\_invoice\_line staging table to the sn\_shop\_invoice\_line primary table.|
|Invoice payment detail import|Transforms invoice payment details from the sn\_spend\_intg\_imp\_invoice\_payment\_detail staging table to the sn\_shop\_invoice\_payment\_detail primary table.|
|Transform organization tax details|Transforms organization tax details data from the sn\_fcms\_intg\_org\_tax\_detail\_inbound staging table to the sn\_fin\_org\_tax\_detail primary table.|

## Subflows

The following subflows move the source-to-pay data from the outbound staging tables to a third-party ERP system.

|Subflows|Description|
|--------|-----------|
|Create cost allocation on outbound table|Moves cost allocation data from the sn\_shop\_cost\_allocation primary table to the sn\_spend\_intg\_outbound\_cost\_allocation staging table.|
|Create purchase order on outbound order table|Moves purchase order data from the sn\_shop\_purchase\_order primary table to the sn\_spend\_intg\_outbound\_purchase\_order staging table.|
|Create purchase order line on outbound order line table|Moves purchase order line data from the sn\_shop\_purchase\_order\_line primary table to the sn\_spend\_intg\_outbound\_purchase\_order\_line staging table.|
|Create/update receipt on outbound table|Moves receipt data from the sn\_shop\_receipt primary table to the sn\_spend\_intg\_outbound\_receipt staging table.|
|Update Supplier Contact Outbound from trigger Supplier Contact|Moves supplier contact details data from the vm\_vdr\_contact primary table to the sn\_spend\_intg\_supplier\_contact\_outbound staging table.|
|Update Supplier Legal entity details from Legal entity mapping|Moves supplier legal entity data from the sn\_fin\_supplier\_detail primary table to the sn\_fcms\_intg\_supplier\_legal\_entity\_outbound staging table.|
|Update Supplier Location outbound from M2M location|Moves supplier location data from the sn\_slm\_m2m\_location primary table to the sn\_spend\_intg\_supplier\_location\_outbound staging table.|
|Update Supplier Outbound from trigger Supplier|Moves supplier data from the sn\_fin\_supplier primary table to the sn\_spend\_intg\_outbound\_supplier​ staging table.|
|Update Supplier Payment Outbound from trigger Payment|Moves supplier payment data from the sn\_fin\_supplier\_payment primary table to the sn\_spend\_intg\_supplier\_payment\_outbound\_stage staging table.|
|Update tax details outbound from trigger tax details|Moves organization tax details data from the sn\_fin\_org\_tax\_detail primary table to the sn\_spend\_intg\_outbound\_tax\_detail staging table.|

