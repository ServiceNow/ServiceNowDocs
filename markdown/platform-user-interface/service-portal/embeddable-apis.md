---
title: Embeddable APIs
description: Service Portal automatically loads the Seismic framework and embeddable APIs when you enable embeddables. To access these APIs in your Service Portal widget scripts, call the spEmbeddables AngularJS service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-user-interface/service-portal/embeddable-apis.html
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [embeddables, API, spEmbeddables, AngularJS service]
breadcrumb: [Embeddables in Service Portal, Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Embeddable APIs

Service Portal automatically loads the Seismic framework and embeddable APIs when you enable embeddables. To access these APIs in your Service Portal widget scripts, call the `spEmbeddables` AngularJS service.

## spEmbeddables service

The `spEmbeddables` service is the entry point for all embeddable interactions. Inject the `spEmbeddables` service into your widget controller to use the available APIs.

## API details

<table id="simpletable_k2x_qft_rkc"><thead><tr><th align="left" id="d132205e80">

API

</th><th align="left" id="d132205e83">

Description and example

</th></tr></thead><tbody><tr><td>

`init()`

</td><td>

Initializes the embeddables framework with a specified UI Builder theme.

 Service Portal calls this API automatically based on the theme you configured in the portal settings.

</td></tr><tr><td>

`getEmbeddables(tagNames)`

</td><td>

Retrieves embeddable component data by component tag name.

 For example:

 ```
spEmbeddables.getEmbeddables(['case-list']).then(function(components) {
  $scope.caseList = components['case-list'];
});
```

</td></tr><tr><td>

`setEvents(element, events)`

</td><td>

Registers event handlers on an embeddable component element.

 For example:

 ```
var caseListElement = document.querySelector('case-list');
spEmbeddables.setEvents(caseListElement, {
  onSelect: $scope.onCaseSelect,
  onUpdate: $scope.onCaseUpdate
});
```

</td></tr><tr><td>

`setProperties(element, properties)`

</td><td>

Updates component properties at runtime. The component re-renders with the new values.

 For example:

 ```
var caseListElement = document.querySelector('case-list');
spEmbeddables.setProperties(caseListElement, {
  filterConfig: newFilter
});
```

</td></tr></tbody>
</table>**Parent Topic:**[Embeddables in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/embeddables-service-portal.md)

