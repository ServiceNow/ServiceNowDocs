---
title: Tutorial: Build a custom widget
description: Follow this tutorial to build a custom widget that displays Service Catalog items. Use this tutorial as a model to help you understand the advanced scripting power of the Service Portal.Create the Quick Order widget to query items in the Service Catalog.After adding your widget and creating a basic template, you can define advanced client and server scripts that enable users to query data from an instance table. You can pass the data model between the client and server by querying data from the database, displaying it to the user, and sending any updates back to the server.Display a list of popular items to the user before any search terms are entered.Enable the user to view and purchase Service Catalog items in the Quick Order widget by embedding the SC Catalog Item widget.Angular Providers are reusable components that can be added to multiple widgets. Using the Widget Angular Providers table, create a directive that shows a category icon next to each result in the Quick Order widget.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Tutorial: Build a custom widget

Follow this tutorial to build a custom widget that displays Service Catalog items. Use this tutorial as a model to help you understand the advanced scripting power of the Service Portal.

In this tutorial, you will create the Quick Order widget. This widget:

-   Displays popular items to the user prior to any search.
-   Queries the Service Catalog and displays available options to the user.
-   Includes an embedded SC Catalog Item widget, allowing the user to view and order items within the Quick Order widget.
-   Uses an Angular Provider to display a category icon beside each queried item.

**Parent Topic:**[Developing custom widgets](widget-dev-guide.md)

## Create a widget and set up a template

Create the Quick Order widget to query items in the Service Catalog.

### Before you begin

Role required: admin or sp\_admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** and click **Widget Editor**.

2.  Click **Create a new widget**.

3.  Define the following values.

    -   **Widget Name**: Quick Order
    -   **Widget ID**: quick\_order
    -   **Create a test page**: Active
    -   **Page ID**: quick\_order
    Adding a widget to a test page creates a record in each of the following tables:

    -   sp\_page
    -   sp\_container
    -   sp\_row
    -   sp\_column
    -   sp\_instance
    -   sp\_widget
    **Note:** You can use the Page Editor in Service Portal Configuration to view the hierarchy of elements on your test page.

4.  Click **Submit**.

5.  From the **Widget Editor**, open the Quick Order widget.

6.  Add the following simple template to the HTML field.

    ```
    <div class="panel panel-primary">
     <div class="panel-heading">Request an item from the catalog</div>
     <div class="panel-body">
       My catalog results
     </div>
    </div>
    
    ```

7.  Click **Save**.

8.  Preview your test page in a new tab using the following URL: `<yourInstanceUrl>/sp?id=quick_order`.

    Your widget template displays on the test page.

    ![Widget rendering on a page](../image/quick-order-test.png)


## Add a server script to query an instance table

After adding your widget and creating a basic template, you can define advanced client and server scripts that enable users to query data from an instance table. You can pass the data model between the client and server by querying data from the database, displaying it to the user, and sending any updates back to the server.

### Before you begin

Role required: admin or sp\_admin

### Procedure

1.  From the **Widget Editor**, open the Quick Order widget.

2.  Select **Server Script** to open the server script field.

3.  Replace the default server script with the following custom script.

    ```javascript
    (function() {
    	if (input.keywords != null && input.keywords != '')
    		data.items = getCatalogItems(input.keywords);
    	
    	function getCatalogItems(keywords) {
    		var sc = new GlideRecord('sc_cat_item');
    		sc.addActiveQuery();
    		sc.addQuery('123TEXTQUERY321', keywords);
    		sc.addQuery('sys_class_name', 'NOT IN', 'sc_cat_item_wizard,sc_cat_item_content');
    		sc.addQuery('sc_catalogs', 'e0d08b13c3330100c8b837659bba8fb4');
    		sc.setLimit(100);
    		sc.orderByDesc("ir_query_score");
    		sc.query();
    		var results = [];
    		while (sc.next()) {
    			if (!$sp.canReadRecord(sc))
    				continue;
    
    			var item = {};
    			$sp.getRecordDisplayValues(item, sc, 'name,price,sys_id');
    			item.category = sc.getValue('category');
    			results.push(item);
    		}
    		return results;
    	}
    })();
    
    ```

    This script performs a keyword search on the sc\_cat\_item table using the 123TEXTQUERY321 query method.

4.  Replace the HTML template with the following script:

    ```
    <div class="panel panel-primary">
     <div class="panel-heading">Request an item from the catalog</div>
     <div class="panel-body">
       <input class="form-control" type="search" placeholder="Start typing here to search the list of catalog items" ng-model="c.data.keywords" ng-change="c.server.update()" ng-model-options="{debounce: 250}" />
       <ul class="list-group result-container">
         <li class="list-group-item" ng-repeat="item in c.data.items">
           <a href>{{item.name}}</a><span class="pull-right">{{item.price}}</span>
         </li>
       </ul>
     </div>
    </div>
    
    ```

    This template adds a search field and displays the results of the query performed in the server script using the following Angular directives. To learn more about these directives, review the [Angular API Reference](https://docs.angularjs.org/api/ng/directive).

    |Angular directive|Description|
    |-----------------|-----------|
    |ng-model|Automatically reads and writes value changes to the model variable `c.data.keywords`.|
    |ng-model-options|Configures ng-model behavior. In this template, ng-model updates the model after a user has stopped typing for 250 milliseconds.|
    |ng-change|Executes `c.server.update()` after the model value changes. This function posts the data object to the server script. After the script is executed, the data object is automatically updated with the new values from the server generated data object.|
    |ng-repeat|Creates a template from the parent element and child elements. For each `item in c.data.items`, an instance of the template is created and the expressions `{{item.name}}` and `{{item.price}}` are replaced with the values from each item.|

5.  Add the following script to the **CSS - SCSS** field:

    ```css
    .result-container {
     margin-top: 10px;
    }
    
    ```

6.  Refresh your test page preview to view the changes.

    As you type in the search box, matching catalog items appear. Try searching for **ipad**.

    ![Search displays results for iPad.](../image/widget-tutorial-search.png)


## Manage the empty state of a widget

Display a list of popular items to the user before any search terms are entered.

### Before you begin

Role required: admin or sp\_admin

### About this task

Because no search has been executed when the widget initializes, the server **input** variable is undefined. This empty state may cause confusion when a user first interacts with the widget. To solve this issue, give your widget something to display when the **input** variable is empty. This initial data can guide your users when initially interacting with your widget.

### Procedure

1.  From the **Widget Editor**, open the Quick Order widget.

2.  Replace the existing server script with the following script:

    ```javascript
    (function() {
        if (input.keywords != null && input.keywords != '')
            data.items = getCatalogItems(input.keywords);
        else data.items = getPopularItems();
    
        function getCatalogItems(keywords) {
            var sc = new GlideRecord('sc_cat_item');
            sc.addActiveQuery();
            sc.addQuery('123TEXTQUERY321', keywords);
            sc.addQuery('sys_class_name', 'NOT IN', 'sc_cat_item_wizard,sc_cat_item_content');
            sc.addQuery('sc_catalogs', 'e0d08b13c3330100c8b837659bba8fb4');
            sc.setLimit(100);
            sc.orderByDesc("ir_query_score");
            sc.query();
            var results = [];
            while (sc.next()) {
                if (!$sp.canReadRecord(sc))
                    continue;
    
                var item = {};
                $sp.getRecordDisplayValues(item, sc, 'name,price,sys_id');
                item.category = sc.getValue('category');
                results.push(item);
            }
            return results;
        }
    
        function getPopularItems() {
            var items = [];
            var count = new GlideAggregate('sc_req_item');
            count.addAggregate('COUNT', 'cat_item');
            count.groupBy('cat_item');
            count.addQuery('cat_item.sys_class_name', 'NOT IN', 'sc_cat_item_guide,sc_cat_item_wizard,sc_cat_item_content');
            count.addQuery('cat_item.sc_catalogs', 'e0d08b13c3330100c8b837659bba8fb4');
            count.orderByAggregate('COUNT', 'cat_item');
            count.query();
            while (count.next() && items.length < 9) {
                if (!$sp.canReadRecord("sc_cat_item", count.cat_item.sys_id.getDisplayValue()))
                    continue; // user does not have permission to see this item
    
                var item = {};
                item.name = count.cat_item.name.getDisplayValue();
                item.category = count.cat_item.category.toString();
                item.price = count.cat_item.price.getDisplayValue();
                item.sys_id = count.cat_item.sys_id.getDisplayValue();
                items.push(item);
            }
            return items;
        }
    })();
    ```

    This script introduces a new function `getPopularItems()` to query the database and return popular items when the **input** variable is empty.

3.  Replace the HTML template with the following script:

    ```
    <div class="panel panel-primary">
      <div class="panel-heading">Request an item from the catalog</div>
      <div class="panel-body">
        <input class="form-control" type="search" placeholder="Start typing here to search the list of catalog items" ng-model="c.data.keywords" ng-change="c.server.update()" ng-model-options="{debounce: 250}" />
        <h5 ng-if="!c.data.keywords">Showing the most popular items</h5>
        <ul class="list-group result-container">
          <li class="list-group-item" ng-repeat="item in c.data.items">
            <a href>{{item.name}}</a><span class="pull-right">{{item.price}}</span>
          </li>
        </ul>
      </div>
      <div class="panel-footer" ng-if="c.data.keywords">
        <ng-pluralize count="c.data.items.length"
                     when="{'0': 'No items found for ',
                         '1': 'One item matching ',
                         'other': 'Found {} items matching '}">
        </ng-pluralize>
        {{c.data.keywords}}
      </div>
    </div>
    
    ```

    This script provides a template to display the popular items returned from the server script.

4.  Refresh your test page preview to view the changes.

    The widget displays popular items to the user prior to any search input.

    ![A search box with the text "Start typing here to search the list of catalog items".](../image/empty-state.png)


## Embed an existing widget

Enable the user to view and purchase Service Catalog items in the Quick Order widget by embedding the SC Catalog Item widget.

### Before you begin

Role required: admin or sp\_admin

### About this task

Instead of duplicating code, you can embed widgets to leverage pre-existing functionality. The SC Catalog Item widget is a base system widget that enables the user to view and purchase Service Catalog items.

### Procedure

1.  Inspect the SC Catalog Item widget.

    Before embedding the SC Catalog Item widget, inspect the widget to understand what data it needs access to. You may need to update your Quick Order widget client or server script to make sure that the correct data is passed to the embedded widget.

    1.  Navigate to `<yourInstanceURL>/sp_config?id=widget_editor`.

    2.  Open the SC Catalog Item widget.

    3.  Note that the widget ID is `widget-sc-cat-item`.

        You will use this ID to embed the widget model in the client script.

    4.  Examine the server script.

        Notice that the **data** object includes a sys\_id property populated by either the **input** or **options** objects. If neither **input** nor **options** include a sys\_id, the [$sp.getParameter\(\)](https://www.servicenow.com/docs/access?context=c_GlideSPScriptableScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) method retrieves the sys\_id from the request query string.

        ![Sample server script using an If Else statement to retrieve the sys_id.](../image/embedded-widget.png)

        To populate the **input** object, you can pass a catalog item sys\_id from the Quick Order widget client script.

2.  From the **Widget Editor**, open the Quick Order widget.

3.  Replace the Quick Order widget client script with the following script.

    ```javascript
    function($location, spUtil) {
        var c = this;
    
        c.select = function(item_id) {
            if (c.openItem == item_id) {
                c.openItem = null;
                return;
            }
    
            renderCatalogItemWidget(item_id);
        }
    
        function renderCatalogItemWidget(item_id) {
            c.catalogItemWidget = null;
            spUtil.get("widget-sc-cat-item", {
                sys_id: item_id
            }).then(function(response) {
                c.catalogItemWidget = response;
                c.openItem = item_id;
            });
        }
    }
    ```

    This script uses `spUtil.get()` to retrieve the widget model by ID \(`widget-sc-cat-item`\) and define the `{sys_id: item_id}` object. This object posts to the server script as **input**.

4.  Replace the HTML template with the following script:

    ```
    <div class="panel panel-primary">
      <div class="panel-heading">Request an item from the catalog</div>
      <div class="panel-body">
        <input class="form-control" type="search" placeholder="Start typing here to search the list of catalog items" ng-model="c.data.keywords" ng-change="c.server.update()" ng-model-options="{debounce: 250}" />
        <h5 ng-if="!c.data.keywords">Showing the most popular items</h5>
        <ul class="list-group result-container">
          <li class="list-group-item" ng-repeat="item in c.data.items">
            <a href ng-click="c.select(item.sys_id)">{{item.name}}</a><span class="pull-right">{{item.price}}</span>
            <div class="catalog-item" ng-if="item.sys_id == c.openItem">
                <sp-widget ng-if="c.catalogItemWidget" widget="c.catalogItemWidget" />
            </div>
          </li>
        </ul>
      </div>
      <div class="panel-footer" ng-if="c.data.keywords">
        <ng-pluralize count="c.data.items.length"
                     when="{'0': 'No items found for ',
                         '1': 'One item matching ',
                         'other': 'Found {} items matching '}">
        </ng-pluralize>
        {{c.data.keywords}}
      </div>
    </div>
    ```

    This template:

    -   Adds on-click behavior using the ng-click directive.
    -   Displays the embedded SC Catalog Item widget using the sp-widget directive.
5.  Replace the CSS with the following script:

    ```css
    .result-container {
      margin-top: 10px;
    }
    
    .catalog-item {
      background-color: #f5f5f5;
      padding: 10px;
      @include border-top-radius($panel-border-radius);
      @include border-bottom-radius($panel-border-radius);
    }
    
    ```

6.  Refresh your test page preview to view the changes.

    When you select a search result, the item opens in the embedded SC Catalog Item widget.

    ![Test page showing a selected item displaying in an embedded widget.](../image/embed-widget-result.png)


## Create a reusable directive and add it to a widget

Angular Providers are reusable components that can be added to multiple widgets. Using the Widget Angular Providers table, create a directive that shows a category icon next to each result in the Quick Order widget.

### Before you begin

Role required: admin or sp\_admin

### About this task

Angular Providers let you build angular directives and services that can be injected into your client script controller. The code in a Provider differs from a typical Angular directive or service because it must be anonymous, without being appended to a specific module.

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** &gt; **Portal Tables** &gt; **Widget Angular Provider**.

    The Widget Angular Providers table opens.

2.  Select **New** to create a new record.

3.  Fill out the form.

    1.  Add the type and name.

        -   **Type**: Directive
        -   **Name**: categoryIcon
    2.  Add the client script.

        ```javascript
        function() {
            return {
                template: '<span class="fa fa-stack fa-lg"><i class="fa fa-circle fa-stack-2x"></i><i class="fa fa-{{::icon}} fa-stack-1x fa-inverse"></i></span>',
                restrict: 'E',
                replace: true,
                scope: {
                    category: '='
                },
                link: function(scope, element) {
        
                    var _iconMap = {
                        "b06546f23731300054b6a3549dbe5dd8": "tablet",
                        /* Tablets */
                        "15706fc0a0a0aa7007fc21e1ab70c2f": "question",
                        /* Can we help you? */
                        "d68eb4d637b1300054b6a3549dbe5db2": "mobile-phone",
                        /* Mobiles */
                        "109cdff8c6112276003b17991a09ad65": "print",
                        /* Office and Print */
                        "5d643c6a3771300054b6a3549dbe5db0": "print",
                        /* Printers */
                        "2c0b59874f7b4200086eeed18110c71f": "plug",
                        /* Peripherals */
                        "2809952237b1300054b6a3549dbe5dd4": "desktop", 
                        /* Software */
                    };
        
                    scope.icon = _iconMap[scope.category] || "shopping-cart";
                }
            }
        }
        ```

        This script associates the sys\_id of the Category record with the Service Catalog item. The icon that displays is the icon defined in the Category record in the Service Catalog.

    3.  Select **Save**.

4.  Associate the new Angular directive with the Quick Order Widget.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

    2.  Open the Quick Order widget.

    3.  Under **Related Lists**, select **Angular Providers**.

    4.  In the Angular Providers list, select **Edit** and associate the categoryIcon Angular Provider with the Quick Order widget.

    5.  Select **Save**.

5.  Add the categoryIcon directive to your Quick Order HTML template.

    1.  From the **Widget Editor**, open the Quick Order widget.

    2.  Replace the HTML template with the following script.

        ```
        <div class="panel panel-primary">
          <div class="panel-heading">Request an item from the catalog</div>
          <div class="panel-body">
            <input class="form-control" type="search" placeholder="Start typing here to search the list of catalog items" ng-model="c.data.keywords" ng-change="c.server.update()" ng-model-options="{debounce: 250}" />
            <h5 ng-if="!c.data.keywords">Showing the most popular items</h5>
            <ul class="list-group result-container">
              <li class="list-group-item" ng-repeat="item in c.data.items">
                <a href ng-click="c.select(item.sys_id)"><category-icon category="item.category" style="margin-right: 10px"></category-icon>{{item.name}}</a><span class="pull-right">{{item.price}}</span>
                <div class="catalog-item" ng-if="item.sys_id == c.openItem">
                    <sp-widget ng-if="c.catalogItemWidget" widget="c.catalogItemWidget" />
                  </div>
              </li>
            </ul>
          </div>
          <div class="panel-footer" ng-if="c.data.keywords">
            <ng-pluralize count="c.data.items.length"
                         when="{'0': 'No items found for ',
                             '1': 'One item matching ',
                             'other': 'Found {} items matching '}">
            </ng-pluralize>
            {{c.data.keywords}}
          </div>
        </div>
        
        ```

6.  Refresh your test page preview to view the changes.

    A category icon displays beside each result.

    ![](../image/category-icon.png)


