---
title: WADL service support for Oracle E-Business Suite
description: Oracle E-Business Suite \(EBS\) exposes custom PL/SQL integration services that are described by WADL documents rather than OpenAPI specifications. Zero Copy Connector for ERP discovers, parses, and models these services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-wadl-support.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, zero, copy, connector, oracle, ebs, wadl, isg, xsd]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# WADL service support for Oracle E-Business Suite

Oracle E-Business Suite \(EBS\) exposes custom PL/SQL integration services that are described by WADL documents rather than OpenAPI specifications. Zero Copy Connector for ERP discovers, parses, and models these services.

## Services described by WADL

Oracle EBS publishes custom PL/SQL packages as REST services through the Integrated SOA Gateway \(ISG\). ISG describes each service with a Web Application Description Language \(WADL\) document plus a set of referenced XML Schema Definition \(XSD\) grammar files. ISG does not use an OpenAPI or Swagger specification.

Because of this, Oracle EBS services follow a separate path through Zero Copy Connector for ERP from the OpenAPI-based REST services described in [Connecting to other ERP systems using REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-use-rest.md). Both paths end at the same place: model entities and fields you map in Model Manager.

## Service discovery and caching

When you add a WADL service, Zero Copy Connector for ERP fetches the WADL document and then walks the schema import graph to collect every XSD file the document references.

A WADL service is identified by its ISG alias combined with the ERP system it belongs to. That pairing must be unique. If you try to add a service whose alias already exists for the same system, the duplicate is rejected rather than overwriting the existing catalog record.

\[Omitted image "erp-add-oracle-rest-service-manually1.jpg"\] Alt text: Add rest service manually modal with use wadl option selected, ISG alias specified, and service name added.

## Input validation strategy

After fields are generated, a validation strategy is set on the operation based on how many of its required input fields were created. The strategy determines whether all required inputs must be supplied, at least one must be supplied, or no input validation is applied.

## Related tasks and reference

To add a WADL service manually when discovery does not find it, see [Add a WADL service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-wadl-service-manually.md).

