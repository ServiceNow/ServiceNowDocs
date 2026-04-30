---
title: Scripting for map pages
description: The Script field on the Map Page form allows the use of attributes or custom code to define map characteristics, such as marker appearance, display information, and more.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Map pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Scripting for map pages

The Script field on the Map Page form allows the use of attributes or custom code to define map characteristics, such as marker appearance, display information, and more.

## Scripting map item attributes

The following attributes are available.

**Note:** To create an item on the map, use the map.addItem\(glideRecord\) method. Pass a valid GlideRecord to **addItem\(\)**.

|Attribute|Description|
|---------|-----------|
|name|Name used for identification.|
|latitude|If you define an address, latitude is not necessary.|
|longitude|If you define an address, longitude is not necessary.|
|icon|URL of the icon to display for the marker. If a custom icon is not specified, the default Google marker is used.|
|icon\_width|Width of the icon. The default is 32.|
|icon\_height|Height of the icon. The default is 32.|
|table\_name|Table whose records display when the marker icon is clicked. Used with the **sys\_id** attribute.|
|sys\_id|Sys\_id of the record that displays when the marker icon is clicked. Used with the **table\_name** attribute.|
|view|View of the form displayed in the dialog box when the marker icon is clicked.|
|html|Arbitrary HTML code for the pop-up window. If used, this value overrides the dialog box.|
|marker\_label|Optional marker icon label text.|
|label\_offset\_left|Optional attribute that is used with **marker\_label** to define the horizontal position of the marker label. The default is 0.|
|label\_offset\_top|Optional attribute that is used with **marker\_label** to define the vertical position of the marker label. The default is 0.|

## Scripting custom map page behavior for smartphone

If you plan to access the map page from a smartphone, you may want to set custom smartphone interface behavior using the **isMobile** variable. You can use the **isMobile** variable to set custom behavior for the smartphone view of the map. For example, you might set different values for the **icon\_width** and **icon\_height** attributes when **isMobile** is true.

## Basic map page script

This script displays all active, critical incident locations.

```
//setup new GlideRecord query on the incident table
var now_GR = new GlideRecord("incident");
//add condition for priority 1
gr.addQuery('priority', '1');
//add condition for active incidents
gr.addActiveQuery();
//execute the query
gr.query();
 
//loop through the list of incidents returned by the query
while (gr.next()) {
 
 //create a new map item to display - linked to the current incident record
 var item = map.addItem(now_GR);
 //add the latitude value from the incident's location
 item.latitude = gr.location.latitude;
 //add the longitude value from the incident's location
 item.longitude = gr.location.longitude;
 //link to the icon image
 item.icon = "http://maps.google.com/mapfiles/kml/pal3/icon51.png";
 //set the icon size
 item.icon_width = "16";
 item.icon_height = "16";
}
```

## isMobile map page script

This script displays all active, critical incident locations with custom settings for smartphone users.

```
//setup new GlideRecord query on the incident table
var now_GR = new GlideRecord("incident");
//add condition for priority 1
gr.addQuery('priority', '1');
//add condition for active incidents
gr.addActiveQuery();
//execute the query
gr.query();
 
//loop through the list of incidents returned by the query
while (gr.next()) {
 
 //create a new map item to display - linked to the current incident record
 var item = map.addItem(now_GR);
 //add the latitude value from the incident's location
 item.latitude = gr.location.latitude;
 //add the longitude value from the incident's location
 item.longitude = gr.location.longitude;
 //link to the icon image
 item.icon = "http://maps.google.com/mapfiles/kml/pal3/icon51.png";
 
 //set the icon size (use smaller icons for smartphone users)
 if (isMobile) {
   item.icon_width = "12";
   item.icon_height = "12";
 }
 else { 
   item.icon_width = "16";
   item.icon_height = "16";
 }
}
```

## Advanced map page script

This script displays the number of open incidents by location. It varies the size of the icon based on the number of open incidents for the location. Using the html parameter, it also displays the location name and number of incidents, as well as a link to the list of related incidents.

```
//get the instances url so we can link back to it
var uri = gs.getProperty("glide.servlet.uri");
//create an aggregate query on the incident table
var count = new GlideAggregate('incident');
//set condition for active incidents
count.addQuery('active', 'true');
//set aggregate field to location to get count by location
count.addAggregate('COUNT', 'location');
//execute the query
count.query();
 
//loop through the results
while (count.next()) {
 
 //get the current record's location
 var loc = count.location;
 //get the count of incidents for this location
 var locCount = count.getAggregate('COUNT', 'location');
 //only display location is there are active incidents
 if (locCount > 0) {
 //create new new map item for this location
 var item = map.addItem(count);
 //set lat/long from the location record
 item.latitude = loc.latitude;
 item.longitude = loc.longitude;
 //build the link to the list of incidents for the location
 var link = 'href=' + uri + 'incident_list.do?sysparm_query=active%3Dtrue^location%3D' + loc;
 //build the html value to be displayed when you click the map icon
 item.html='<a ' + link + '>' + loc.getDisplayValue() + ' (' + locCount + ')</a>';
 //link to the icon image
 item.icon = "http://maps.google.com/mapfiles/kml/pal3/icon51.png";
 //set the size of the icon based on the number of active incidents
 if (locCount < 5) {
 item.icon_width = "12";
 item.icon_height = "12";
 }
 else if (locCount < 15) {
 item.icon_width = "16";
 item.icon_height = "16";
 }
 else {
 item.icon_width = "32";
 item.icon_height = "32";
 }
 }
}
```

## Map page marker label script

Marker labels allow you to add dynamic text to markers. This example displays the active incident count at each location.

![](../image/MapMarkerLabels.png "Map marker labels")

```
//get the instances url so we can link back to it
var uri = gs.getProperty("glide.servlet.uri");
//create an aggregate query on the incident table
var count = new GlideAggregate('incident');
//set condition for active incidents
count.addQuery('active', 'true');
//set aggregate field to location to get count by location
count.addAggregate('COUNT', 'location');
//execute the query
count.query();
 
//loop through the results
while (count.next()) {
 
 //get the current record's location
 var loc = count.location;
 //get the count of incidents for this location
 var locCount = count.getAggregate('COUNT', 'location');
 //only display location is there are active incidents
 if (locCount > 0) {
 //create new new map item for this location
 var item = map.addItem(count);
 //set lat/long from the location record
 item.latitude = loc.latitude;
 item.longitude = loc.longitude; 
 
 //create a marker label with the count
 item.marker_label = locCount;
 //define label offset for proper position
 item.label_offset_left = -4;
 item.label_offset_top = -20;
 
 //option to define table and record for label hyperlink
 //setting table and sys_id will override the use of html parameter
 //item.table = 'cmn_location';
 //item.sys_id = loc;
 
 //build the link to the list of incidents for the location
 var link = 'href=' + uri + 'incident_list.do?sysparm_query=active%3Dtrue^location%3D' + loc;
 //build the html value to be displayed when you click the map icon
 item.html='<a ' + link + '>' + loc.getDisplayValue() + ' (' + locCount + ')</a>';
 
 //link to the icon image
 item.icon = "images/red_marker.png";
 //set the size of the icon based on the number of active incidents
 item.icon_width = 24;
 item.icon_height = 24;
 
 }
}
```

**Parent Topic:**[Map pages](../concept/c_MapPages.md)

**Related topics**  


[Set up Google Maps API](../task/set-up-google-maps-api.md)

[Create a map page](../task/t_CreateAMapPage.md)

[Create a map page module](../task/create-map-page-module.md)

[Create an advanced Map Page](../task/create-advanced-map-page.md)

[Set map application scope](../task/set-map-application-scope.md)

[Create a smartphone map page module](../task/t_CreateASmartphoneMapPageModule.md)

