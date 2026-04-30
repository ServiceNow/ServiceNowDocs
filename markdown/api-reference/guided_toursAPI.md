---
title: Guided Tours - Client
description: The Guided Tours API provides methods for launching and stopping guided tours.Sets a function to retrieve filtered tour results when the getAllTours\(\) method is called.Stops a currently playing tour. This method silently exits if no tours are playing.Removes an existing event listener.Attaches an event listener to a guided tour event.Gets a list of tours on the current page from which this method is called. Because this method is asynchronous, a callback function must be passed to determine operation success and get a list of tours.Loads the guided tours player on a page in which guided tours player is not present by default.Starts a tour. Because this method is asynchronous, you must pass a callback function to determine operation success.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# Guided Tours- Client

The Guided Tours API provides methods for launching and stopping guided tours.

This API includes methods used in [Guided Tour Designer](../../../../../integrate/inbound-rest/reference/r_RESTAPIHTTPResponseCodes.md).

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## Guided Tours - applyListFilter\(Function filter\_func\)

Sets a function to retrieve filtered tour results when the `getAllTours()` method is called.

Complete signature includes `top.NOW.guided_tours.api` preceding the method name.

|Name|Type|Description|
|----|----|-----------|
|filter\_func|Function|Filter function that takes a single `tour` object from the `tours[]` array returned from `getAllTours()` method.|

|Type|Description|
|----|-----------|
|None| |

The following example shows basic API usage.

```
//create a filter function
var filtFunction = function(tour) {
   //only return those tours whose name starts with 'my'
   return tour.name.indexOf('my') === 0);
}

//apply the filter 
top.NOW.guided_tours.api.applyListFilter (filtFunction);

//call the getAllTours method to observe the filtered tours
top.NOW.guided_tours.api.getAllTours (function(er, tours) {
  if(!er) {
    console.log('The filtered tours are: ');
    console.log(tours);
  }
});

```

The following example shows how to use the `options` field on the tour object to add JSON with custom tour identifiers for reading and filtering tours inside the `filter_func()` function.

```
top.NOW.guided_tours.api.applyListFilter(function(tour) {
       var options = (tour.options)? JSON.parse(tour.options): null;
       return (options && options.my_param) ? (options.my_param == my_value) : false;
});
```

## Guided Tours - endTour\(\)

Stops a currently playing tour. This method silently exits if no tours are playing.

Complete signature includes `top.NOW.guided_tours.api` preceding the method name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Null| |

```
//create a callback function to end the tour if it starts correctly
var cbFunction = function(err) {
	if (err) {
   console.log('Error Occurred');
}
	else {
	   // tour has started so we can call endTour
	   top.NOW.guided_tours.api.endTour();
}
}

//calling the startTour method so that we can end the tour as soon as it starts
top.NOW.guided_tours.api.startTour('a297e04b732313007077edcc5ef6a780', 2, cbFunction);

```

## Guided Tours - events.off\(String event\_name, Function listener\_function\)

Removes an existing event listener.

Complete signature includes `top.NOW.guided_tours.api` preceding the method name.

<table id="table_iwb_kbs_xhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

event\_name

</td><td>

String

</td><td>

Event name to be removed from the listener.Valid event names:

-   tourStarted
-   tourEnded
-   tourCompleted
-   tourFailed
-   tourAbandoned
-   tourDismissed
-   stepStarted

</td></tr><tr><td>

listener\_function

</td><td>

Function

</td><td>

Optional. If provided, specified listener function is removed from remaining event listeners attached with that event. If not provided, all listener functions attached to that event are removed.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
//create a callback function to handle the result of the api call
var eventListenerTourStarted = function() {
   console.log('The tour has started'); 
}
var eventListenerTourEnded = function() {
   console.log('The tour has ended'); 
}

//attaching event listeners for tourStarted and tourEnded Events
top.NOW.guided_tours.events.on('tourStarted',eventListenerTourStarted);
top.NOW.guided_tours.events.on('tourEnded', eventListenerTourEnded);

…
//start a tour
top.NOW.guided_tours.api.startTour ('a297e04b732313007077edcc5ef6a780', 2, cbFunction);
//As soon as the tour starts the eventListenerTourStarted gets fired
…
top.NOW.guided_tours.api.endTour();
// eventListenerTourEnded gets fired

….

//removing the event listeners top.NOW.guided_tours.events.off('tourStarted',eventListenerTourStarted);
top.NOW.guided_tours.events.off('tourEnded', eventListenerTourEnded);

```

## Guided Tours - events.on\(String event\_name, Function listener\_function\)

Attaches an event listener to a guided tour event.

Complete signature includes `top.NOW.guided_tours.api` preceding the method name.

<table id="table_iwb_kbs_xhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

event\_name

</td><td>

String

</td><td>

Event name to be attached to the listener.Valid event names:

-   stepStarted
-   tourStarted
-   tourEnded
-   tourCompleted
-   tourFailed
-   tourAbandoned
-   tourDismissed

</td></tr><tr><td>

listener\_function

</td><td>

Function

</td><td>

Listener to be added.**Note:** Clear any event listener after it solves its purpose.

</td></tr><tr><td>

listener\_function.obj

</td><td>

Object

</td><td>

Passed to `listener_function()` by each event in the following format:-   For stepStarted events:

    ```
{tour: '<tour_sys_id>', step: step_num}
    ```

-   For all other events:

    ```
{tour: '<tour_sys_id>'}
    ```


 JSON parameters:

-   tour\_sys\_id: String. Guided tour ID from the Guided Tours \[sys\_embedded\_tour\_guide\] table
-   step\_num: Number. Value between 0 \(first step\) and `n` \(final step\)

</td></tr></tbody>
</table>The following example shows basic API usage.

```
//create a callback function to handle the result of the api call
var eventListenerTourStarted = function() {
   console.log('The tour has started'); 
}
var eventListenerTourEnded = function() {
   console.log('The tour has ended'); 
}

//attaching event listeners for tourStarted and tourEnded Events
top.NOW.guided_tours.events.on('tourStarted',eventListenerTourStarted);
top.NOW.guided_tours.events.on('tourEnded', eventListenerTourEnded);

…
//start a tour
top.NOW.guided_tours.api.startTour ('a297e04b732313007077edcc5ef6a780', 2, cbFunction);
//As soon as the tour starts the eventListenerTourStarted gets fired
…
top.NOW.guided_tours.api.endTour();
// eventListenerTourEnded gets fired

….

//removing the event listeners top.NOW.guided_tours.events.off('tourStarted',eventListenerTourStarted);
top.NOW.guided_tours.events.off('tourEnded', eventListenerTourEnded);

```

The following example shows how to use the `listener_function` parameter with `obj` as an argument.

```
top.NOW.guided_tours.events.on("tourStarted", function (obj){console.log(obj);});
```

## Guided Tours - getAllTours\(Function cb\_function\)

Gets a list of tours on the current page from which this method is called. Because this method is asynchronous, a callback function must be passed to determine operation success and get a list of tours.

Complete signature includes `top.NOW.guided_tours.api` preceding the method name.

<table id="table_nrj_bbs_xhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cb\_function

</td><td>

Function

</td><td>

Callback function called by `getAllTours()` after attempt to fetch all tours for the current page from which `getAllTours()` method is called.

</td></tr><tr><td>

cb\_function.err

</td><td>

Object

</td><td>

Points to the error object if any occurred during the operation:`err = { success: false, message: 'string containing the error object' }`

 Null otherwise.

</td></tr><tr><td>

cb\_function.tours

</td><td>

Array

</td><td>

List of available tours for the page.If no tours are present on the page, `cb_function.tours` returns undefined.

 `if(!tours) console.log('No tour present')`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
//create a callback function to handle the result of the API call
var cbFunction = function(err, tours) {
	if (err) {
   console.log('Error Occurred');
}
	else {
	    if(!tours) console.log('No tour present')
   else {
      tours.forEach(function(t) {
               console.log(t);
             });
          }
}
}
//calling the getTours method
top.NOW.guided_tours.api.getAllTours(cbFunction);

```

## Guided Tours - loadPlayer\(\)

Loads the guided tours player on a page in which guided tours player is not present by default.

Complete signature:

```
NOW.guided_tours.api.loadPlayer()
```

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

## Guided Tours - startTour\(String tour\_id, Number step\_number, Function cb\_function\)

Starts a tour. Because this method is asynchronous, you must pass a callback function to determine operation success.

Complete signature includes `top.NOW.guided_tours.api` preceding the method name.

<table id="table_wh5_w1s_xhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tour\_id

</td><td>

String

</td><td>

Sys ID of the tour from the Guided Tours \[sys\_embedded\_tour\_guide\] table.

</td></tr><tr><td>

step\_number

</td><td>

Number

</td><td>

Optional. Step at which to start the tour. If not provided \(or step number is 0\), tour starts from the beginning.

</td></tr><tr><td>

cb\_function

</td><td>

Function

</td><td>

Optional. Callback function called by `startTour()` method after attempt to launch the tour.

</td></tr><tr><td>

cb\_function.err

</td><td>

Object

</td><td>

Points to the error object if any occurred during the operation:`err = { success: false, message: 'string containing the error object' }`

 Null otherwise.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
//create a callback function to handle the result of the API call
var cbFunction = function(err) {
	if (err) {
   console.log('Error Occurred');
}
	else {
   console.log('The tour with tourid=%s was successfully launched', tourId);
}
}

//calling the startTour method
top.NOW.guided_tours.api.startTour('a297e04b732313007077edcc5ef6a780', 2, cbFunction);

```

