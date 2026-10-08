---
title: ServiceNow Quote Experience runtime API calls
description: Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a OpenAPI Specification for testing in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-runtime-api-calls.html
release: brazil
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 20
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience runtime API calls

Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a OpenAPI Specification for testing in CPQ.

## API overview

CPQ APIs are divided into two categories: runtime APIs and admin APIs. Runtime APIs are the same APIs used in the runtime quote experience. The following table lists the runtime APIs for ServiceNow Quote Experience.

|API action|Purpose|Response|
|----------|-------|--------|
|Initialize a session|Initializes a session to establish a context for executing transaction events, managing state, and processing subsequent API calls. Can initialize for an existing transaction. If no transaction is specified, a new transaction is created.|Returns a session ID, a transaction ID, and transaction information.|
|Delete a session|Deletes a session to securely end user activity, clear session-specific data, and free up system resources.|Session is deleted. No information is returned.|
|Create a transaction|Creates a transaction, providing the object to manage the transaction lifecycle, configure and add products, and determine pricing.|Returns a transaction ID and transaction information.|
|Run events on a transaction|Triggers a specified system or custom event on a transaction to execute predefined logic or workflows, such as editing field values, initiating approvals, versioning transactions, and validating configurations.|Varies by event.|
|Add products to a transaction \(upsert\)|Adds one or more products to a transaction, enabling dynamic configuration and pricing updates based on the product's attributes.|Returns updated transaction data with the additional products.|
|Get a list of transactions|Retrieves a list of transactions, enabling users to view, manage, or take action on existing transactions.|A list of transactions with transaction IDs and metadata.|
|Get details of a transaction|Retrieves the header information of a transaction, including stage, account, and summary-level data.|All header field data for the transaction.|
|Get a transaction's lines|Retrieves the line item details for a transaction, including product data, quantities, pricing, and custom attributes for each line.|All line-level field data for the transaction.|

**Note:** Event APIs are authorized via session cookie only. Avoid building a scenario in which the user initiates an event that also fires an event API on the same transaction — such an implementation can result in unpredictable behavior.

## Additional APIs

For details about the API that retrieves metrics for transactions, see [Quote Experience metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-metrics-api.md).

## OpenAPI Specification

The following OpenAPI specification describes all available REST endpoints, request payloads, response formats, parameters, and data models for the ServiceNow Quote Experience runtime APIs.

```
openapi: 3.0.3
info:
  title: Logik Transaction API 09.04.2026
  version: 09.04.2026
paths:
  /api/t:
    post:
      description: Creates or loads a transaction. If a transaction ID is passed in, it will load the existing transaction.
        Otherwise, one will be created.
      operationId: initWorkingInstance
      parameters:
      - $ref: '#/components/parameters/personaHeader'
      - $ref: '#/components/parameters/logExecution'
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/InitRequest'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/InitTransaction'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Initialize a transaction
      tags:
      - txnManager
  /api/t/{session}:
    get:
      description: Retrieves the full transaction state for the given session, including fields, events, messages, layouts
        and tenant settings. No rules are re-executed.
      operationId: getWorkingInstance
      parameters:
      - $ref: '#/components/parameters/session'
      - $ref: '#/components/parameters/personaHeader'
      - $ref: '#/components/parameters/applyAccessPolicy'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/WorkingInstance'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get the current state of a working session
      tags:
      - txnManager
    patch:
      description: Runs any rules that should be run, and returns updates to be made to view state
      operationId: patchWorkingInstance
      parameters:
      - $ref: '#/components/parameters/session'
      - $ref: '#/components/parameters/personaHeader'
      - $ref: '#/components/parameters/logExecution'
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/PatchWorkingInstanceRequest'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/PatchWorkingInstance'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Update the working session with data bits
      tags:
      - txnManager
  /api/t/{sessionId}:
    delete:
      description: Will summarily remove the instance. Saving the instance would be responsibility of client.
      operationId: removeWorkingInstance
      parameters:
      - description: ID of the working instance
        in: path
        name: sessionId
        required: true
        schema:
          type: string
      responses:
        '200':
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Delete the working instance
      tags:
      - txnManager
  /api/t/{session}/removeSession:
    post:
      description: Will summarily remove the instance. Saving the instance would be responsibility of client.
      operationId: removeWorkingInstanceForPost
      parameters:
      - $ref: '#/components/parameters/session'
      responses:
        '200':
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Delete the working instance
      tags:
      - txnManager
  /api/t/{session}/flightpath:
    get:
      description: Flightpath contains rule execution history for a given transaction session
      operationId: getFlightPath
      parameters:
      - $ref: '#/components/parameters/session'
      responses:
        '200':
          content:
            application/json:
              schema:
                items:
                  items:
                    $ref: '#/components/schemas/RuleExecutionEvent'
                  type: array
                type: array
          description: OK
        '400':
          $ref: '#/components/responses/400error'
      summary: Get flightpath
      tags:
      - txn
  /api/t/{blueprintId}/revisions/{revision}/layouts/{layoutId}:
    get:
      description: Gets layout json by layout id, blueprint id and revision.
      operationId: getLayout_1
      parameters:
      - $ref: '#/components/parameters/blueprintId'
      - $ref: '#/components/parameters/revision'
      - $ref: '#/components/parameters/layoutId'
      responses:
        '200':
          content:
            application/json:
              schema:
                type: string
          description: Successful
      summary: Gets layout json by layout id, blueprint id and revision
      tags:
      - txnManager
  /api/t/{transactionId}/events/{eventId}:
    post:
      description: Event API. Handles custom and most system events. Some system events may have distinct payloads, and are
        represented as separate endpoints here. If a system endpoint does not have a specific endpoint defined, it is handled
        by this one.
      operationId: runEvent
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/eventId'
      - $ref: '#/components/parameters/async'
      - $ref: '#/components/parameters/personaHeader'
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/EventPostRequest'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/EventExecution'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Execute a txn event
      tags:
      - txn
  /api/t/{transactionId}/events/{eventId}/{jobId}:
    get:
      description: This will get the status or result from an async event execution. The jobId is returned from the call to
        execute the async event. Only the user who made the execution request is allowed to get the status or result.
      operationId: getEventRun
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/eventId'
      - $ref: '#/components/parameters/jobId'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/EventExecution'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get result from async event execution
      tags:
      - txn
  /api/t/{transactionId}/moveLine:
    post:
      description: API to move line within a transaction by specifying the current line, target line, and desired position.
        If currentLineId == targetLineId, line will move one above previousLineId or one below nextLineId if targetPosition
        is specified as BEFORE or AFTER respectively. This is to handle the scenario when a user selects the first or last
        line id on current page in UI.
      operationId: moveLine
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/personaHeader'
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/MoveLinePostRequest'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/MoveLineSuccessResponse'
          description: Line moved successfully.
        '400':
          $ref: '#/components/responses/400error'
      summary: Transaction Line Reordering API
      tags:
      - txn
  /api/t/{transactionId}/lines:
    post:
      description: Limited set of fields for each line. The exact fields may depend upon the session context if there is one.
      operationId: getLinesPost
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/search'
      - $ref: '#/components/parameters/filter'
      - $ref: '#/components/parameters/format'
      - $ref: '#/components/parameters/parentId'
      - $ref: '#/components/parameters/expand'
      - $ref: '#/components/parameters/page'
      - $ref: '#/components/parameters/size'
      - $ref: '#/components/parameters/sort'
      - $ref: '#/components/parameters/direction'
      - $ref: '#/components/parameters/lineId-2'
      - $ref: '#/components/parameters/txnSession'
      - $ref: '#/components/parameters/session-2'
      - $ref: '#/components/parameters/personaHeader'
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/LineResponseFilter'
        required: false
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/LinePage'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get data for lines under a transaction
      tags:
      - txn
  /api/t/{transactionId}/events/upsertLines:
    post:
      description: Adds lines to the transaction. Payload is an array of either catalog or configurable product IDs, along
        with the line ID in the case of reconfigure
      operationId: upsertLines
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/async'
      - $ref: '#/components/parameters/personaHeader'
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/UpsertLinesPostRequest'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/EventExecution'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Execute a txn event
      tags:
      - txn
  /api/t/{transactionId}/messages:
    get:
      description: Get line messages under a transaction. Sort param must be the same as for getLines to get correct line
        indexes
      operationId: getMessages
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/parentId'
      - $ref: '#/components/parameters/page'
      - $ref: '#/components/parameters/size'
      - $ref: '#/components/parameters/sort'
      - $ref: '#/components/parameters/direction'
      - $ref: '#/components/parameters/session-2'
      - $ref: '#/components/parameters/personaHeader'
      - $ref: '#/components/parameters/search'
      - $ref: '#/components/parameters/filter'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/MessagePage'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get line messages under a transaction
      tags:
      - txn
  /api/t/{transactionId}/fields/{fieldVariableName}/options:
    get:
      description: Fetch a page of options that are associated with a field.
      operationId: getFieldOptions_2
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/fieldVariableName'
      - $ref: '#/components/parameters/txnSession'
      - $ref: '#/components/parameters/session-2'
      - $ref: '#/components/parameters/page'
      - $ref: '#/components/parameters/size'
      - $ref: '#/components/parameters/search'
      - $ref: '#/components/parameters/personaHeader'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/PagedOptionSet'
          description: Successful
      summary: Fetch options for a field
      tags:
      - txn
  /api/t/{transactionId}/lines/{lineId}/fields/{fieldVariableName}/options:
    get:
      description: Fetch a page of options that are associated with a line field.
      operationId: getLineFieldOptions
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/lineId'
      - $ref: '#/components/parameters/fieldVariableName'
      - $ref: '#/components/parameters/txnSession'
      - $ref: '#/components/parameters/session-2'
      - $ref: '#/components/parameters/page'
      - $ref: '#/components/parameters/size'
      - $ref: '#/components/parameters/search'
      - $ref: '#/components/parameters/personaHeader'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/PagedOptionSet'
          description: Successful
      summary: Fetch options for a line field
      tags:
      - txn
  /api/txn:
    get:
      description: Get high-level information for each transaction in the list
      operationId: getTxns
      parameters:
      - description: filter expression
        in: query
        name: filter
        required: false
        schema:
          type: string
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/HeaderPage'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get data for transactions
      tags:
      - txn
      x-spring-paginated: true
  /api/txn/{transactionId}:
    get:
      description: Fetches details for a specific transaction, as well as optionally the lines associated with it.
      operationId: getTransaction
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/format'
      - $ref: '#/components/parameters/lineId-2'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/HeaderDto'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get data for transaction
      tags:
      - txn
  /api/txn/{transactionId}/lines:
    get:
      description: Limited set of fields for each line. The exact fields may depend upon the session context if there is one.
      operationId: getLines
      parameters:
      - $ref: '#/components/parameters/transactionId'
      - $ref: '#/components/parameters/search'
      - $ref: '#/components/parameters/filter'
      - $ref: '#/components/parameters/format'
      - $ref: '#/components/parameters/parentId'
      - $ref: '#/components/parameters/expand'
      - $ref: '#/components/parameters/page'
      - $ref: '#/components/parameters/size'
      - $ref: '#/components/parameters/sort'
      - $ref: '#/components/parameters/direction'
      - $ref: '#/components/parameters/lineId-2'
      - $ref: '#/components/parameters/txnSession'
      - $ref: '#/components/parameters/session-2'
      - $ref: '#/components/parameters/personaHeader'
      responses:
        '200':
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/LinePage'
          description: Successful
        '400':
          $ref: '#/components/responses/400error'
      summary: Get data for lines under a transaction
      tags:
      - txn
components:
  parameters:
    applyAccessPolicy:
      name: applyAccessPolicy
      in: query
      required: false
      schema:
        type: boolean
    async:
      name: async
      in: query
      description: Parameter to make event execution asynchronous.
      required: false
      schema:
        type: boolean
    blueprintId:
      name: blueprintId
      in: path
      required: true
      schema:
        type: integer
        format: int64
    direction:
      name: direction
      in: query
      description: Sorting direction
      required: false
      schema:
        type: string
        enum:
        - DESC
        - ASC
        default: ASC
    eventId:
      name: eventId
      in: path
      description: <TODO>
      required: true
      schema:
        type: string
    expand:
      name: expand
      in: query
      description: "A comma-separated list of line UUIDs to control which lines are expanded.  \n- If not provided, all lines\
        \ are expanded.  \n- If provided (e.g., `expand=line1,line2`), only those lines are expanded.  \n- If empty (`expand=`),\
        \ no lines are expanded.\n"
      required: false
      schema:
        type: string
    fieldVariableName:
      name: fieldVariableName
      in: path
      required: true
      schema:
        type: string
    filter:
      name: filter
      in: query
      description: Filter parameter
      required: false
      schema:
        type: string
    format:
      name: format
      in: query
      description: Format of the response
      required: false
      schema:
        $ref: '#/components/schemas/Format'
    jobId:
      name: jobId
      in: path
      required: true
      schema:
        type: integer
        format: int64
    layoutId:
      name: layoutId
      in: path
      required: true
      schema:
        type: integer
        format: int64
    lineId:
      name: lineId
      in: path
      description: Transaction Line Id
      required: true
      schema:
        type: string
    lineId-2:
      name: lineId
      in: query
      description: Transaction Line Id
      required: false
      schema:
        type: string
    logExecution:
      name: logExecution
      in: query
      description: Parameter to enable logging to flightpath
      required: false
      schema:
        type: boolean
    page:
      name: page
      in: query
      description: Number of the page to return if the resource supports paged response
      required: false
      schema:
        type: integer
        default: 0
    parentId:
      name: parentId
      in: query
      description: Parent Id
      required: false
      schema:
        type: string
    personaHeader:
      in: header
      name: X-Logik-User-Persona
      schema:
        type: string
    revision:
      name: revision
      in: path
      description: revision of the blueprint
      required: true
      schema:
        type: string
    search:
      name: search
      in: query
      description: Search parameter
      required: false
      schema:
        type: string
    session:
      name: session
      in: path
      description: ID of the working instance
      required: true
      schema:
        type: string
    session-2:
      name: session
      in: query
      description: Session Id
      required: false
      schema:
        type: string
    size:
      name: size
      in: query
      description: Size of the page to return if the resource supports paged response
      required: false
      schema:
        type: integer
        default: 10
    sort:
      name: sort
      in: query
      description: Sorting parameter
      required: false
      schema:
        type: string
        default: txn.line.order
    transactionId:
      name: transactionId
      in: path
      description: <TODO>
      required: true
      schema:
        type: string
    txnSession:
      name: txnSession
      in: query
      description: Txn Session Id
      required: false
      deprecated: true
      schema:
        type: string
  responses:
    400error:
      description: Invalid input(s)
      content:
        application/json:
          schema:
            $ref: '#/components/schemas/error'
  schemas:
    AggregateAccessStateDto:
      title: AggregateAccessStateDto
      type: object
      properties:
        fields:
          type: array
          items:
            $ref: '#/components/schemas/FieldAggregateVisibilityDto'
        events:
          type: array
          items:
            $ref: '#/components/schemas/EventAggregateVisibilityDto'
    AggregateMessageStateDto:
      title: AggregateMessageStateDto
      type: object
      properties:
        messageCount:
          type: integer
        errorCount:
          type: integer
        warningCount:
          type: integer
    CatalogItem:
      title: CatalogItem
      type: object
      properties:
        id:
          type: string
        quantity:
          type: number
          deprecated: true
          description: 'DEPRECATED: This field is no longer respected. Use the ''fields'' array instead.

            Set quantity via: { "variableName": "txn.line.quantity", "value": 5 }

            This field will be removed in a future release.

            '
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
          description: Additional line fields to set on the transaction line
      required:
      - id
    ChangeType:
      title: Change Type
      type: string
      enum:
      - VALIDATE_CONFIGS_TASK_EXECUTED
    ConfigItem:
      title: ConfigItem
      type: object
      properties:
        configurationId:
          type: string
        lineId:
          type: string
      required:
      - configurationId
    ContextDto:
      title: ContextDto
      type: object
      description: Used to contain the context for relevant API calls, such as init and event actions.
      properties:
        txnSession:
          type: string
          deprecated: true
        session:
          type: string
        delta:
          type: boolean
        logExecution:
          type: boolean
        lineIds:
          uniqueItems: true
          type: array
          items:
            type: string
        copyCount:
          type: integer
          minimum: 1
          default: 1
          description: 'Number of copies to create for a cloneLine event. Optional; defaults to 1 (single copy = legacy behavior).
            Only honored for the cloneLine event and only when the tenant setting transaction.events.cloneLine.multiCopy.enabled
            is true; otherwise it is clamped to 1. Validated against the per-tenant maximum (transaction.events.cloneLine.multiCopy.maxCopies)
            in transaction-service, which rejects a count above the maximum; the rules engine re-enforces the same ceiling
            for non-UI requests.

            '
    Event:
      title: Event
      type: object
      properties:
        name:
          type: string
        variableName:
          type: string
        visibilityState:
          type: string
        active:
          type: string
      required:
      - variableName
      x-class-extra-annotation: '@lombok.AllArgsConstructor

        @lombok.Builder'
    EventAggregateVisibilityDto:
      title: EventAggregateVisibilityDto
      type: object
      properties:
        variableName:
          type: string
        visibilityState:
          type: string
        active:
          type: string
      required:
      - variableName
      - visibilityState
      - active
    EventExecution:
      title: Event Execution
      type: object
      properties:
        state:
          type: string
          enum:
          - SUCCESS
          - FAILURE
          - SUCCESS_SAVE_FAILED
          - PARTIAL_SUCCESS
        response:
          $ref: '#/components/schemas/PatchWorkingInstance'
        relatedChanges:
          type: array
          items:
            $ref: '#/components/schemas/RelatedChange'
        executionInstance:
          $ref: '#/components/schemas/Job'
      required:
      - state
    EventPostRequest:
      title: EventPostRequest
      type: object
      properties:
        context:
          $ref: '#/components/schemas/ContextDto'
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        lines:
          type: array
          items:
            $ref: '#/components/schemas/PatchLine'
    ExternalCallEvent:
      title: ExternalCallEvent
      type: object
      properties:
        name:
          type: string
        startTime:
          type: integer
          format: int64
        endTime:
          type: integer
          format: int64
        externalCallType:
          type: string
    Field:
      title: Field
      type: object
      x-class-extra-annotation: '@lombok.AllArgsConstructor

        @lombok.Builder'
      properties:
        name:
          type: string
        value:
          type: object
          x-field-extra-annotation: "@com.fasterxml.jackson.annotation.JsonInclude(\n  com.fasterxml.jackson.annotation.JsonInclude.Include.ALWAYS\n\
            )"
        dataType:
          type: string
        visibilityState:
          type: string
        editable:
          type: string
        variableName:
          type: string
        userEdited:
          type: boolean
        uniqueName:
          type: string
        step:
          type: number
        index:
          type: integer
        selectAll:
          type: string
        set:
          type: string
        optionSet:
          $ref: '#/components/schemas/OptionSet'
      required:
      - variableName
    FieldAggregateVisibilityDto:
      title: FieldAggregateVisibilityDto
      type: object
      properties:
        variableName:
          type: string
        visibilityState:
          type: string
      required:
      - variableName
      - visibilityState
    Format:
      type: string
      enum:
      - FLAT
      - TREE
    HeaderDto:
      title: HeaderDto
      type: object
      properties:
        uuid:
          type: string
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        lines:
          type: array
          items:
            $ref: '#/components/schemas/Line'
    HeaderPage:
      title: Headers Page
      type: object
      allOf:
      - $ref: '#/components/schemas/PaginationResponse'
      - type: object
        properties:
          content:
            type: array
            items:
              $ref: '#/components/schemas/HeaderWithoutLines'
            default: []
    HeaderWithoutLines:
      title: HeaderWithoutLines
      type: object
      properties:
        uuid:
          type: string
          deprecated: true
        id:
          type: string
        txn.externalId:
          type: string
        txn.account.id:
          type: string
        txn.pricebook.id:
          type: string
        txn.opportunity.id:
          type: string
        txn.persona:
          type: string
        txn.pricing.total:
          type: number
        txn.pricing.subTotal:
          type: number
        txn.pricing.discount.percent:
          type: number
        txn.pricing.discount.amount:
          type: number
        txn.pricing.currencyCode:
          type: string
        txn.stage:
          type: string
        txn.version.number:
          type: integer
        txn.version.path:
          type: string
        txn.parent.id:
          type: string
        txn.created:
          type: string
          format: date-time
        txn.createdBy:
          type: string
        txn.modified:
          type: string
          format: date-time
        txn.modifiedBy:
          type: string
    InitRequest:
      title: initRequest
      description: Auto generated JSON schema based on the 'bomProduct' file
      type: object
      properties:
        txnId:
          type: string
        id:
          type: string
        partnerData:
          type: object
          properties:
            account:
              type: string
            contact:
              type: string
            pricebookInfo:
              type: string
          required:
          - account
          - contact
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        items:
          type: array
          items:
            type: object
            title: UpsertLinesItem
            oneOf:
            - $ref: '#/components/schemas/CatalogItem'
            - $ref: '#/components/schemas/ConfigItem'
            - $ref: '#/components/schemas/ManualConfigItem'
        stateful:
          type: boolean
      required:
      - stateful
    InitTransaction:
      title: InitTransaction
      type: object
      properties:
        txnSession:
          type: string
          description: The identifier of the working instance
          deprecated: true
        session:
          type: string
          description: The identifier of the working instance
        uuid:
          type: string
          description: The identifier of the transaction
          deprecated: true
        id:
          type: string
          description: The identifier of the transaction
        stage:
          type: string
          description: Variable name of the stage the transaction is in
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        events:
          type: array
          items:
            $ref: '#/components/schemas/Event'
        messages:
          type: array
          items:
            $ref: '#/components/schemas/Message'
        aggregateAccessState:
          $ref: '#/components/schemas/AggregateAccessStateDto'
        aggregateMessageState:
          $ref: '#/components/schemas/AggregateMessageStateDto'
        layouts:
          type: array
          items:
            $ref: '#/components/schemas/LayoutUrlDto'
        tenantSettings:
          $ref: '#/components/schemas/TenantSettings'
      required:
      - fields
    Job:
      title: Job
      type: object
      properties:
        id:
          type: integer
          format: int64
          description: The identifier of the job
        status:
          type: string
          description: The status of the job
        errorMessage:
          type: string
          description: Error message if the job failed
        started:
          type: string
          description: When the job started
        finished:
          type: string
          description: When the job finished
    LayoutUrlDto:
      title: LayoutUrlDto
      type: object
      properties:
        url:
          type: string
        variableName:
          type: string
        label:
          type: string
      x-class-extra-annotation: '@lombok.AllArgsConstructor

        @lombok.NoArgsConstructor'
    Line:
      title: Line
      type: object
      properties:
        uuid:
          type: string
          deprecated: true
        id:
          type: string
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        events:
          type: array
          items:
            $ref: '#/components/schemas/Event'
        messages:
          type: array
          items:
            $ref: '#/components/schemas/Message'
        lines:
          type: array
          items:
            $ref: '#/components/schemas/Line'
        predecessors:
          type: array
          items:
            type: string
        visiblePredecessors:
          type: array
          items:
            type: string
        hasChildren:
          type: boolean
    LinePage:
      title: Lines Page
      type: object
      allOf:
      - type: object
        properties:
          content:
            type: array
            items:
              $ref: '#/components/schemas/Line'
            default: []
          referencePredecessors:
            type: array
            items:
              $ref: '#/components/schemas/Line'
            default: []
      - $ref: '#/components/schemas/PaginationResponse'
    LineResponseFilter:
      title: LineResponseFilter
      type: object
      properties:
        filteredFields:
          type: array
          items:
            type: string
      x-class-extra-annotation: '@lombok.Builder

        @lombok.AllArgsConstructor

        @lombok.NoArgsConstructor'
    ManualConfigItem:
      title: ManualConfigItem
      type: object
      properties:
        configurationId:
          type: string
        lines:
          type: array
          maxItems: 200
          items:
            $ref: '#/components/schemas/ManualConfigLine'
          description: 'The hierarchy of transaction lines for this configuration, supplied directly by the caller.

            Lines are matched against hive lines using txn.line.configuration.item.uniqueIdentifier,

            txn.line.product.id, or txn.line.configuration.item.key (in priority order). Where a match is

            found, the caller''s fields are superimposed on top of the configuration line''s fields. Configuration lines with

            no matching caller line are included unchanged. Caller lines with no matching config line are

            dropped. The root line is stamped with CONFIGURATION_STATUS=Valid if the persisted CBOM is

            valid, or CONFIGURATION_STATUS=Invalid otherwise.

            '
      required:
      - configurationId
      - lines
    ManualConfigLine:
      title: ManualConfigLine
      type: object
      properties:
        id:
          type: string
        parent:
          type: string
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
          description: Line fields to set on this transaction line
      required:
      - id
    Message:
      title: Message
      type: object
      properties:
        message:
          type: string
        type:
          type: string
        error:
          type: boolean
        target:
          type: string
        targetType:
          type: string
        set:
          type: string
        index:
          type: integer
        color:
          type: string
        icon:
          type: string
      required:
      - type
      - message
      x-class-extra-annotation: '@lombok.AllArgsConstructor

        @lombok.Builder'
    MessagePage:
      title: Messages Page
      type: object
      allOf:
      - type: object
        properties:
          content:
            type: array
            items:
              $ref: '#/components/schemas/MessageWithLineInfo'
            default: []
      - $ref: '#/components/schemas/PaginationResponse'
    MessageWithLineInfo:
      title: Message with Line info
      type: object
      properties:
        id:
          type: string
        lineIndex:
          type: integer
        message:
          $ref: '#/components/schemas/Message'
    MoveLinePostRequest:
      title: MoveLinePostRequest
      type: object
      properties:
        sourceLineIds:
          type: array
          items:
            type: string
            format: uuid
            description: The IDs of the lines to be moved.
        currentLineId:
          deprecated: true
          type: string
          format: uuid
          description: The ID of the line to be moved.
          example: 42c85098-897e-4e26-938b-12ac043478cc
        targetLineId:
          type: string
          format: uuid
          description: The ID of the target line to position around.
          example: 62c8798-897e-4e26-938b-12ac043478888
        targetPosition:
          type: string
          enum:
          - BEFORE
          - AFTER
          description: Specifies whether to move the current line before or after the target line.
          example: BEFORE
        sessionId:
          type: string
          description: Txn session ID.
      required:
      - targetLineId
      - targetPosition
      - sessionId
    MoveLineSuccessResponse:
      title: Lines moved successfully.
      type: object
      properties:
        currentLineId:
          deprecated: true
          type: string
          format: uuid
          description: The ID of the line that was moved.
          example: 42c85098-897e-4e26-938b-12ac043478cc
        newIndex:
          type: integer
          description: The new index of the first moved line in the list of all lines when sorted.
          example: 56
    Option:
      title: Option
      type: object
      properties:
        label:
          type: string
        state:
          type: string
        value:
          type: string
        imageUrl:
          type: string
        orderNumber:
          type: number
      required:
      - label
      - state
      - value
      - imageUrl
      - orderNumber
      x-class-extra-annotation: '@lombok.Builder'
    OptionSet:
      title: OptionSet
      type: object
      properties:
        selectedOptions:
          type: array
          items:
            $ref: '#/components/schemas/Option'
      allOf:
      - oneOf:
        - $ref: '#/components/schemas/PagedOptionSet'
        - $ref: '#/components/schemas/UnpagedOptionSet'
    Pageable:
      type: object
      format: pageable
      properties:
        page:
          type: integer
          minimum: 0
        size:
          type: integer
          minimum: 1
        sort:
          type: array
          items:
            type: string
    PageableObject:
      title: PageableObject
      type: object
      properties:
        sort:
          type: array
          items:
            $ref: '#/components/schemas/SortObject'
        offset:
          type: integer
        pageNumber:
          type: integer
        pageSize:
          type: integer
        paged:
          type: boolean
        unpaged:
          type: boolean
      x-class-extra-annotation: '@lombok.AllArgsConstructor

        @lombok.Builder'
    PagedOptionSet:
      title: PagedOptionSet
      type: object
      properties:
        options:
          type: array
          items:
            $ref: '#/components/schemas/Option'
        pageable:
          type: object
          $ref: '#/components/schemas/PageableObject'
        last:
          type: boolean
        totalPages:
          type: integer
        totalElements:
          type: integer
        sort:
          type: array
          items:
            $ref: '#/components/schemas/SortObject'
        first:
          type: boolean
        size:
          type: integer
        number:
          type: integer
        numberOfElements:
          type: integer
        empty:
          type: boolean
    PaginationResponse:
      type: object
      properties:
        totalElements:
          type: integer
          format: int64
          default: 0
        totalPages:
          type: integer
          default: 0
        sort:
          $ref: '#/components/schemas/Sort'
        first:
          type: boolean
        last:
          type: boolean
        number:
          type: integer
        pageable:
          $ref: '#/components/schemas/Pageable'
        numberOfElements:
          type: integer
        size:
          type: integer
        empty:
          type: boolean
        content:
          type: array
          items: {}
    PatchLine:
      title: PatchLine
      type: object
      properties:
        uuid:
          type: string
          deprecated: true
        id:
          type: string
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
      required:
      - fields
    PatchWorkingInstance:
      title: PatchWorkingInstance
      type: object
      properties:
        uuid:
          type: string
          description: The identifier of the transaction
          deprecated: true
        id:
          type: string
          description: The identifier of the transaction
        errorMessage:
          type: string
          description: This will hold any messages generated from business logik errors.
        timestamp:
          type: string
          description: This will show the timestamp when errors occurred.
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        stage:
          type: string
          description: Variable name of the stage the transaction is in
        lines:
          type: array
          items:
            $ref: '#/components/schemas/Line'
        events:
          type: array
          items:
            $ref: '#/components/schemas/Event'
        messages:
          type: array
          items:
            $ref: '#/components/schemas/Message'
        aggregateAccessState:
          type: object
          $ref: '#/components/schemas/AggregateAccessStateDto'
        aggregateMessageState:
          $ref: '#/components/schemas/AggregateMessageStateDto'
    PatchWorkingInstanceRequest:
      title: PatchWorkingInstanceRequest
      type: object
      properties:
        context:
          $ref: '#/components/schemas/ContextDto'
        uuid:
          type: string
          deprecated: true
        id:
          type: string
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        lines:
          type: array
          items:
            $ref: '#/components/schemas/PatchLine'
      required:
      - fields
      - lines
    RelatedChange:
      title: Related Change
      type: object
      properties:
        key:
          type: string
        type:
          $ref: '#/components/schemas/ChangeType'
      required:
      - key
      - type
    RuleExecutionEvent:
      title: RuleExecutionEvent
      type: object
      properties:
        name:
          type: string
        ruleVariableName:
          type: string
        inputs:
          type: array
          items:
            type: string
        endTime:
          type: integer
          format: int64
          writeOnly: true
        executionTime:
          type: string
          format: date-time
        actionVariableName:
          type: string
        changes:
          type: array
          items:
            $ref: '#/components/schemas/StateUpdateEvent'
        elapsedTime:
          type: integer
          format: int64
        stageRule:
          type: boolean
        eventName:
          type: string
        eventActionName:
          type: string
        externalCalls:
          type: array
          items:
            $ref: '#/components/schemas/ExternalCallEvent'
    Sort:
      type: object
      format: sort
      properties:
        sorted:
          type: boolean
        unsorted:
          type: boolean
        empty:
          type: boolean
    SortObject:
      title: Sort
      type: object
      properties:
        empty:
          type: boolean
        sorted:
          type: boolean
        unsorted:
          type: boolean
      x-class-extra-annotation: '@lombok.AllArgsConstructor'
    StateUpdateEvent:
      title: StateUpdateEvent
      type: object
      properties:
        source:
          type: string
          enum:
          - USER_INPUT
          - RULE
        event:
          type: string
          enum:
          - CREATE
          - DELETE
          - UPDATE
        type:
          type: string
          enum:
          - FIELD
          - DETERMINATION
          - MESSAGE
          - PRODUCT
          - SOLUTION_PRODUCT
          - EXCLUSION
          - INCLUSION
          - VISIBILITY
          - EDITABLE
          - EVENT_ACTIVE
          - EVENT_VISIBILITY
          - TRANSACTION_LINE
        identifier:
          type: string
        oldValue:
          type: object
        newValue:
          type: object
        baseStateIdentifier:
          type: string
    TenantSettings:
      title: TenantSettings
      type: object
      x-class-extra-annotation: '@lombok.AllArgsConstructor

        @lombok.Builder'
      properties:
        autosaveTxn:
          type: boolean
        sessionTTL:
          type: integer
        sessionKeepAlive:
          type: integer
        allowCosmoConverse:
          type: string
        showConverseRlhf:
          type: boolean
        trainConverseRlhf:
          type: boolean
        accessControlEnabled:
          type: boolean
        favoritesSharingEnabled:
          type: boolean
        oneQuotingEnabled:
          type: boolean
          x-field-extra-annotation: "@com.fasterxml.jackson.annotation.JsonInclude(\n  com.fasterxml.jackson.annotation.JsonInclude.Include.NON_NULL\n\
            )"
        oneQuotingApprovalsEnabled:
          type: boolean
          x-field-extra-annotation: "@com.fasterxml.jackson.annotation.JsonInclude(\n  com.fasterxml.jackson.annotation.JsonInclude.Include.NON_NULL\n\
            )"
        oneQuotingSubscriptionsEnabled:
          type: boolean
          x-field-extra-annotation: "@com.fasterxml.jackson.annotation.JsonInclude(\n  com.fasterxml.jackson.annotation.JsonInclude.Include.NON_NULL\n\
            )"
        multiCopyEnabled:
          type: boolean
          x-field-extra-annotation: "@com.fasterxml.jackson.annotation.JsonInclude(\n  com.fasterxml.jackson.annotation.JsonInclude.Include.NON_NULL\n\
            )"
        multiCopyMaxCopies:
          type: integer
          x-field-extra-annotation: "@com.fasterxml.jackson.annotation.JsonInclude(\n  com.fasterxml.jackson.annotation.JsonInclude.Include.NON_NULL\n\
            )"
    UnpagedOptionSet:
      title: UnpagedOptionSet
      type: object
      properties:
        options:
          type: array
          items:
            $ref: '#/components/schemas/Option'
    UpsertLinesPostRequest:
      title: UpsertLinesPostRequest
      type: object
      properties:
        context:
          $ref: '#/components/schemas/ContextDto'
        items:
          type: array
          items:
            type: object
            title: UpsertLinesItem
            oneOf:
            - $ref: '#/components/schemas/CatalogItem'
            - $ref: '#/components/schemas/ConfigItem'
            - $ref: '#/components/schemas/ManualConfigItem'
          maxItems: 200
    WorkingInstance:
      title: WorkingInstance
      type: object
      properties:
        txnSession:
          type: string
          description: The identifier of the working instance
          deprecated: true
        session:
          type: string
          description: The identifier of the working instance
        uuid:
          type: string
          description: The identifier of the transaction
          deprecated: true
        id:
          type: string
          description: The identifier of the transaction
        stage:
          type: string
          description: Variable name of the stage the transaction is in
        fields:
          type: array
          items:
            $ref: '#/components/schemas/Field'
        events:
          type: array
          items:
            $ref: '#/components/schemas/Event'
        messages:
          type: array
          items:
            $ref: '#/components/schemas/Message'
        aggregateAccessState:
          $ref: '#/components/schemas/AggregateAccessStateDto'
        aggregateMessageState:
          $ref: '#/components/schemas/AggregateMessageStateDto'
        layouts:
          type: array
          items:
            $ref: '#/components/schemas/LayoutUrlDto'
        tenantSettings:
          $ref: '#/components/schemas/TenantSettings'
      required:
      - fields
    error:
      title: error
      description: Every error has this format
      type: object
      properties:
        errorMessage:
          type: string
        errorCode:
          type: string
        timestamp:
          type: string
```

