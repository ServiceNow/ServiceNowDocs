---
title: Configuring the Telecom Discovery Builder framework ETL in a connector
description: Leverage the prebuilt Telecom Discovery Builder framework ETL by duplicating it into your connector scope, assigning the appropriate data source, and deploying it as part of a new service graph connector.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configuring the Telecom Discovery Builder framework ETL in a connector

Leverage the prebuilt Telecom Discovery Builder framework ETL by duplicating it into your connector scope, assigning the appropriate data source, and deploying it as part of a new service graph connector.

The Telecom Discovery Builder framework ETL provided with the Telecom Service Operations Management \(TSOM\) Core is a ready-to-use framework designed to streamline data ingestion into the CMDB across telecom connectors. Rather than configuring it directly, as an administrator, you can duplicate the ETL into a connector’s application scope and update the data source to align with the connector’s discovery payload.

## Steps to use the Telecom Discovery Builder framework ETL in a connector

1.  Create a temporary data source: Create a data source in your connector’s application scope based on the Generic Schema multi source data source from TSOM Core. This enables you to run and test the duplicated ETL with schema-aligned placeholder data. For more information, see [Create a data source similar to Telecom core data source](../task/create-a-data-source-similar-to-tsom-core-data-source.md)
2.  Duplicate the Telecom Discovery Builder framework ETL: Access ETL Studio, locate the Telco Generic Schema ETL, and duplicate it into the connector’s scope. During duplication: Provide a new name. Assign the temporary data source. Use importSet as the discovery source. For more information, see [Duplicate the Telecom Discovery Builder framework ETL into a connector scope](../task/duplicate-the-generic-etl-to-use-a-specific-connector.md)
3.  After duplication, open the new ETL and replace the temporary data source with the connector’s actual discovery data source. For more information, see [Update the data source of the connector](../task/update-data-source-of-the-connector.md).
4.  Test or deploy the service graph connector. For more information, see [Deploy a new service graph connector with existing ETL](../task/deploy-a-new-service-graph-connector-with-duplicated-etl.md)

