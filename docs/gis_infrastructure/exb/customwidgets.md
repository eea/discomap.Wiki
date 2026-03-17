# Custom widgets

## Add Group Content

The Add Group Content widget shows a list of layers that are shared with a specific group in ArcGIS Portal, allowing users to add them to the map.

_The version of this widget is: 1.17.0_

### Usage notes

This widget is essential for adding layers from a predefined group within ArcGIS Portal to your map. It is designed to be user-friendly and configurable through the Experience Builder interface or by importing/exporting a CSV file for advanced users.

#### Features:

- **List of Layers**: Displays layers shared with a specific group.
- **Add to Map**: Allows users to add layers to the map.
- **Categorization**: Supports categories displayed as an accordion menu for better organization.
- **Layer Details**: Configure layer details such as category, temporal coverage, SDI link, download link, and service URL.

### Settings

The Add Group Content widget includes the following settings:

- **Map Selection**: Choose the map to which the widget will be applied.
- **Use URL parameters**: Enable the use of URL parameters for configuration.
- **Group ID**: Enter the Group ID to pull the layers from the specific ArcGIS Portal group.
- **Import/Export**: Advanced layer configuration by importing/exporting a CSV file.
- **Sort alphabetically**: Option to sort the layers alphabetically.

## Add Data Simplified

A simplified widget that allows users to add data to the map by searching for layers in ArcGIS content, entering URLs, or uploading local files.

_The version of this widget is: 1.17.0_

### Usage notes

This widget provides a streamlined interface for users to bring their own data into the application. It supports three methods of adding data, which can be toggled in the settings.

### Settings

- **Map Widget**: Select the map to which the data will be added.
- **Way of adding data**: Enable or disable specific methods:
    - **Select from account**: Allow searching and adding layers from ArcGIS Online/Portal.
    - **Input URL**: Allow adding data via service URLs.
    - **Upload files**: Allow uploading local files (e.g., CSV, KML, GeoJSON).
- **Empty list message**: Customize the placeholder text shown when no data has been added.

## Dynamic Filter Widget

**The version of this widget is: 1.14.0**

The Dynamic Filter widget provides the ability to list the available values for predefined feature layer fields in order to filter an ArcGIS layer datasource.

### Usage notes

Dynamic filters can be configured using a single feature layer data source. A filter can contain multiple fields, noting that the available values for each field are not affected by the selected values for other fields.  
The field filters can be configured to allow single value or multiple value selection.

> ℹ️ **Tip**  
> The widget can publish one message that can be used to configure actions in Experience Builder (ExB).
>
> - Data source filter changes

### Layer Configuration

Each layer added through the widget can be configured with the following fields:

- **Category**: Assign a category to the layer to organize it within the accordion menu.
- **Temporal Coverage**: Specify the temporal range for the data, e.g., 1995-2012.
- **SDI URL**: Provide a SDI link for the layer.
  - **Hide SDI Link**: Option to hide the SDI link if not needed.
- **Download URL**: Provide a download link for the layer data.
  - **Hide Download Link**: Option to hide the download link if not needed.
- **Service URL**: Paste the service URL if necessary.

### Important Notes

- **Public Accessibility**: If the application is intended to be public, ensure that all layers are shared with everyone and the group is configured to be visible by everyone.

## EEA Gradient Legend Widget

The Gradient Legend widget creates an ArcGIS-style legend component for a single layer. This widget can be used to display multiple stand-alone legend elements for specific layers.

_The version of this widget is: 1.15.0_

### Usage notes

The widget layer configuration requires selecting:

- **A map widget**.
- **A map view** that belongs to the selected map widget.
- **A layer view**.

The legend can be configured to display horizontally or vertically. For best results, ensure that both **Bar width** and **Bar height** are set accordingly.

#### Features

- **Horizontal or Vertical Layout**: Configure the legend direction.
- **Automatic Sizing**: Recommended to set **Bar width** or **Bar height** to `auto` depending on the direction.

### Settings

The Gradient Legend widget includes the following settings:

- **Direction**: Choose between horizontal or vertical display.
- **Bar Width/Height**: Adjust the width and height for the legend bar to optimize display based on direction.
- **Rounding**: Option to round the values in the legend.
- **Precision**: Set the number of decimal places for the labels.

### Important Notes

- The widget only supports **color-based** `classBreakInfos` and/or `visualVariables`.
- **Direction Setting**: Setting the appropriate width or height to `auto` depending on the chosen direction is recommended.
- **Renderer Support**: Only layers using the **ClassBreaksRenderer** are supported (https://developers.arcgis.com/javascript/latest/api-reference/esri-renderers-ClassBreaksRenderer.html).
- **Color-based Only**: The widget does not support non-color-based class breaks or visual variables.

## Layer List

The Layer List widget provides a list of the layers added to a map. It allows users to manage the visibility and order of layers interactively.

_The version of this widget is: 1.17.0_

### Usage notes

The Layer List widget enhances user interaction with the map layers by providing several convenient features. Users can easily reorder layers, adjust transparency, toggle visibility, zoom to specific layers, and remove layers as needed.

#### Features:

- **Change drawing order**: Change the drawing order of the layers.
- **Transparency**: Adjust the transparency of each layer using a slider or by typing a number (percentage).
- **Toggle Visibility**: Switch on/off the visibility of each layer.
- **Zoom to Layer**: Quickly zoom to the extent of a specific layer.
- **Remove Layer**: Remove a layer from the map using the red trash can button.

### Settings

- **Do not list sublayers**: Checkbox option to hide sublayers from the list.

> ℹ️ **Tip** 
> 
> - **Interactivity**: Utilize the drag and drop feature to reorder layers easily, making the most important layers visible on top.

## EEA Legend

Customizable Legend used to give experience owner some flexibility in customizing the legend because the out-of-the-box one is not customizable.

_The version of this widget is: 1.10.0_

### Features

- **Inherits Advanced Options** from the original widget (Font color and Background color)
- **Customizable from settings panel** from Super Advanced Customization section as follows:
  - **webMapentry** contains customization options for WebMap as follows:
    - **show**: used to show/hide title
    - **color**: used to select the appropriate title color
    - **titleReplacement**: used in case you'd like to change the title
    - and more can be added like font size, etc.
  - **maps**: entry contains the set of maps (map services) within the web map, each map has set of layers as follows:
    - **layers**: entry contains the layers within each map service, customization options:
      - **showInLegend**: used to show/hide the entire layer in legend
      - **layer > show**: used to show/hide layer title
      - **layer > titleReplacement**: used in case you'd like to change the layer title
      - **legend > show**: used to show/hide legend title, which is the alias of the field used in defining the color ranges
      - **legend > titleReplacement**: used in case you'd like to change the legend title
      - **legend > reverse**: used to reverse the color ranges of the legend

## Linked Button Widget

**The version of this widget is: 1.17.0**

### Settings

- **Embedded (iframe) link target**: Option to open the link in a new tab specifically when the app is embedded in an iframe.

The Linked Button widget is based on the existing Experience Builder Button widget, adding the ability to enable/disable the button, link to multiple data sources, and other features.

### Usage notes

The Linked Button widget can be linked with multiple data sources, and its state (enabled/disabled) can be set to match feature selection.  
Matching the widget state with feature selection — i.e., enabling the widget only when at least one feature is selected — can be configured to work with any features, or features that satisfy a specific condition.  
When the widget is configured to open a URL, the configured URL can be opened in the same tab or a new window. It can also be configured to open in a new window only if the app is running inside an iframe.

## EEA Matomo Detailed Tracking

Widget used to track statistics & metrics into the EEA Matomo software.

_The version of this widget is: 1.17.0_

### Settings

The parameter necessary for use this widget it's:

- **Matomo site Url**: The URL of your Matomo instance (e.g., `https://matomo.eea.europa.eu/`).
- **Matomo site Id**: The ID of the site in Matomo (e.g., `7`).
- **Page title**: Optional custom title for the tracked page.
- **Include search parameters**: Checkbox to include URL search parameters in tracking.
- **Include hash fragments**: Checkbox to include URL hash fragments in tracking.
- **Measure time spent on page**: Switch to enable tracking of time spent on the page.

### Usage notes

The detailed widget allows to get statistics per page and also measuring the time spent on each page.

## Multilevel Layer Filter

The Multilevel Layer Filter widget provides the ability to list the available values for predefined feature layer fields in order to select a subset of features for further processing. This widget affects the record selection across the app, so that other widgets can use the selected data.

_The version of this widget is: 1.17.0_

### Usage notes

Multiple filters can be configured using different feature layer datasources. A new tab is introduced for each filter. The tab color and text can be configured.
A filter can contain multiple fields, noting that the available values for each field will be affected by the selected values for all preceding fields. Changing the selected value for any field can be configured to trigger a record selection change or an extent change or both.

### Settings

- **Layout**: Choose between **Horizontal** or **Vertical** layout for the filter tabs.
- **Hide Title**: Option to hide the widget title.
- **Deselect on inactive**: Option to clear selection when the filter becomes inactive.
- **Field Settings**:
    - **Zoom to features**: Automatically zoom to features upon selection.
    - **Hide feature count**: Hide the total count of features.
    - **Set selection**: detailed selection options.

#### Warning:

- In case of using multiple instances of this widget, note that the active tab and selected values will be synchronized across all instances, and that multiple instances are meant to be used in tandem.
- Only "Single selection" is currently supported for filter type. "Multiple selection" is unsupported.

## EEA Nested Section Menu

A responsive section menu widget that detects nested page structures, displays child pages in a horizontal or hamburger menu, and allows customization of spacing, font size, and color.

_The version of this widget is: 1.15.0. Working and tested on Experience Builder 1.15._

### Features

This widget dynamically detects whether the current page is part of a nested page structure with a parent and child pages. When such a structure is identified, the widget renders a horizontal section menu displaying all child pages.

- **Automatic Detection:** Recognizes if the page has a parent and child relationship.
- **Responsive Design:**
    - Displays a horizontal menu on screens wider than 980px.
    - Switches to a hamburger menu on narrower screens for mobile-friendly navigation.
- **Customizable Styles:**
    - **Link Spacing:** Adjust the space between menu items.
    - **Font Size:** Define the size of the text for menu items.
    - **Font Color:** Set a custom color for the menu text.

This enables a clear, user-friendly navigation experience within hierarchically organized content, with full control over visual styling.

## Non-interactive Map Widget

The Non-interactive Map widget provides the ability to include a static map in the application that cannot be modified by the user. The map center and scale shall remain unchanged during usage, unless changed through other widgets (i.e., interaction with data lists). The user is not able to pan the map using the mouse or touch events, or zoom in/out using the scroll button or pinch gestures.

_The version of this widget is: 1.14.0_

### Usage notes

You can show a single map or include the option to switch between two maps. You can include multiple maps in an app by adding more Map widgets.
The Map widget requires a data source, including web maps and web scenes. When you include tools, they are automatically positioned on the map based on the size of the widget in both design mode and the final app.

This widget can be configured similar to the out-of-the-box Map widget. Please refer to the Map widget documentation for more information.

> ℹ️ **Tip**  
>
> - Zoom buttons can be enabled/disabled using widget configuration. Which can allow limited interactivity with the map.
>
> - Feature pop-up can be enabled/disabled using widget configuration.

#### Warning:

- Scroll zooming is always disabled, even if enabled in widget configuration.

## EEA Login

This is a sign-in widget that supports both simple and advanced login options.

_The version of this widget is: 1.19.0_

### Settings

- **Login Type**:
    - **Popup Window**: Opens login in a popup.
    - **Redirect**: Redirects the current page for login.
- **Post Sign-In Settings**:
    - **Redirect after login**: Configure a link to redirect after successful login.
    - **Redirect after logout**: Configure a link to redirect after logout.
- **Login Options**:
    - **Simple Login**: Basic login button.
    - **Advanced Login**: Includes extended options like Username, User Avatar, User Profile, User Settings, and custom links (e.g., "Forgot Password").
- **Appearance**: Customize icons and styles (Regular/Hover active states).

## EEA Dropdown

Generic EEA-style drop-down widget with configurable title and options.

_The version of this widget is: 1.15.0_

### Settings

- **General Options**:
    - **Open by default**: Checkbox.
    - **Group ID**: For grouping multiple dropdowns.
    - **Title box color**: Color picker for the dropdown header.
- **Dropdown Title**: Set the main title text.
- **Title Icon**:
    - **Same icon for both states**: Toggle.
    - **Icon size/gap**: Numeric inputs.
    - **Select Icon**: Choose images for collapsed/expanded states.
- **Font Sizes**:
    - **Title/Option size**: Numeric inputs.
    - **Size unit**: px or rem.
    - **Maintain proportions**: Lock aspect ratio between title and options.
- **Dropdown Content**:
    - **Add option**: Add new items to the list.
    - **Option Name**: Text label.
    - **Link**: Link selector for the option.
    - **Open by default**: Pre-select option.

## EEA Feature Switch

A widget that allows navigating through features of a layer one by one, acting as a feature switcher or paginator. It works with a selected data source and can push the current feature to other widgets.

_The version of this widget is: 1.15.0_

### Settings

- **Data Source**: Select the feature layer to navigate.
- **Layer Query**:
    - **Distinct fields**: Select fields to ensure distinct values (optional).
    - **Feature selection**: Checkbox "**Select current feature**". If enabled, the currently visible feature in the switcher will be automatically selected (highlighted) on the map.

## EEA Popup filter

EEA Popup filter is an Experience Builder widget where Map popup appears on map click, popup will contain list of features comes from webmap data source. On click on any item in the list appeared in the popup, the dataframe got filtered as well.

_The version of this widget is: 1.11.0_

### Usage notes

Widget works exactly like ESRI's Table widget. It needs a datasource and it can filter the dataframe, it has visual list, it has UI controls to trigger clear filter.

To use the widget, drag it and configure the settings as follows...

1. Select map from map selector dropdown. Selected webmap's datasource will be the data sources.
2. Select New sheet exactly like in Table widget.
3. Configure message Action/Trigger.

### How does it work

1. Using the webmap that has been set in setting widget, enable click on map and select clicked feature.

   - Get the map service behind the webmap.
   - Add invisible feature layer using the same URL of the map service.
   - Add graphics layer to map.
   - Define hittest function to allow users to select feature from the newly created feature layer.
   - Draw the selected feature on the graphics layer.

2. On Map feature selection via map click, filter list with the table.
   - After clicking on map get the selected feature geometry, and filter the table with it.
   - Once table records are filtered, the dataframe will also be filtered (given that Action/Trigger defined previously).


## EEA Simple Navigation

A customizable link widget that supports styling for default, hover, and active states.

_The version of this widget is: 1.15.0. Working and tested on Experience Builder 1.15._

### Features

The widget generates a hyperlink element with customizable visual states, including:

- **Default**
- **Hover**
- **Active**

This customization capability allows developers to apply specific styles to the link, independent of the theme's default settings. Without this feature, styling would be constrained to the theme’s predefined text formats, limiting personalization and design flexibility.

## EEA TimeLine

The Timeline widget allows you to view temporal data from web maps, feature layers, and map service layers to see how data changes over time. Using this widget, you can animate data with play and pause buttons and manually view changes using a slider, and zoom in and out on a timeline.

_The version of this widget is: 1.10.0, Working on Experience Builder 1.14_

### Usage notes

This widget requires a data source that includes temporal and time-enabled data. The data source can be a web map, one or multiple map services, or one or multiple feature layers. The Timeline widget updates the data source universally, meaning it affects other widgets using the same data. For example, you can connect a Timeline, Map, List, and Table widget to the same feature layer and use the Timeline widget to filter the others. The data source may include a time offset. An offset allows you to display time-enabled data using time values that are offset from the time values recorded in the data. Applying a time offset does not affect the date and time information stored in the source data. For example, you can use an offset of one year to make data for a hurricane display as if it occurred at the same time as a different hurricane from the previous year. If a data source includes an offset, the Timeline widget honors the offset.

#### Note:

Notes necessary for understanding the widget.

> ℹ️ **Tip** 
> 
> To enable time settings on a layer, the layer must be published to ArcGIS Online with a date field.
>
> When you include this widget in an app, the widget provides users with the following options:
> 
> - **Overall time extent**—Click the information button to display the entire extent of time represented by the timeline and view the following setting:
> - **Timeline filtering applied**—When this option is turned on, the Timeline widget filters the connected data source at the framework level, meaning it affects any other widgets using the same data source.
> - **Zoom in and Zoom out**—Zoom in or zoom out on the slider.
> - **Previous and Next**—Move the slider one step forward or backward.
> - **Play and Pause**—Play or pause the time animation.
> - **Speed**—Choose a play speed from five levels: Slowest, Slow, Medium, Fast, or Fastest.

### Settings

The Timeline widget includes the following settings:

- **Source**—Select data source with temporal data to analyze with the widget.
- **Time settings**—Configure the timeline's settings. Time settings include start time, end time, length of time steps, and more.

  - **Synchronize with the time settings in the web map** (Only available for web maps)—Synchronize the widget's time settings with settings configured in Map Viewer.
  - **Configure time**—Modify the timeline's start time, end time, length of time steps, and more.
    - **Time span**—Set the length of time represented by the timeline. The layer bar or bars show the total amount of time represented in the connected layers. You can drag both ends of the Overall time extent bar to set the timeline's time span relative to the layer bar or bars.
    - **Start time and End time**—Set the lower and upper limits for the widget. You can define the start and end times in the following four ways:
      - **Minimum of all and Maximum of all**—Use the minimum and maximum points from the selected data for the start and end time.
      - **Today**—Anchor the start or end time to the current date. Optionally, add an offset number of years, months, or days. For example, if you choose Today for the start time and provide an offset of -6 days, the start time will always be 6 days before the current date. If you provide an offset of 6 days, the start time will always be 6 days after the current date.
      - **Now**—Anchor the start or end time to the current minute. This option is the same as Today, except the offset adds hours and minutes as available units.
      - **Custom**—Choose a specific date and time from a calendar interface.
    - **Set the minimum time accuracy**—Provide the minimum interval between notches on the timeline. Each unit is only provided in the drop-down menu when the Time span value is long enough to contain at least one of them.
  - **Date format**—Type of date format in which it is displayed in the widget.
    - **Default**
    - **Seasons**—Format sss
    - **July 2015**—Format MMMM YYYY
    - **Jul 2015**—Format MMM YYYY
    - **Jul 21, 2015**—Format MMMM D, YYYY
    - **Tue Jul 21, 2015**—Format dddd MMM DD, YYYY
    - **7/21/2015**—Format M/DD/YYYY
    - **2015/7/21**—Format YYYY/M/DD
    - **7/21/15**—Format M/DD/YY
    - **2015**—Format YYYY
    - **7/21/2015 8:00 am**—Format M/DD/YYYY h:mm a
    - **Tue Jul 21 8:00 am**—Format ddd MMM DD h:mm a
    - **Custom**—Any date format that supports the library link: [momentjs](https://momentjs.com/)
  - **Shows one timestep**—If enabled, only one date will be displayed.
  - **Configure play rate**—Controls the speed of play by default.
  - **Time step**—Select one of two modes for dividing the timeline into steps:

    - **Length of one step**—Use natural time units, such as months or days, to define the steps. You can only choose units that are the same or greater than the unit you provide for the minimum time accuracy. If you choose this mode, the user can use the Previous and Next buttons to move the slider one step at a time based on the minimum time accuracy you provide.
    - **Total time divided into equal steps**—Divide the time extent into an equal number of steps. If you choose this mode and provide 5 as the number of equal steps, the user can move the slider 1/5 of the total length at a time using the Previous and Next buttons. For example, if you choose this mode and provide 5 as the number of equal steps, the user can move the slider one-fifth of the total length at a time.

    #### Note:

    Users can click and hold the time slider to drag it freely forward and backward.

  - **Time display**—Choose a method for visualizing data:
    - **Show current window**—Only show data associated with each step. For example, you can show a hurricane's position every day for one month.
    - **Show data cumulatively**—Add data to the display cumulatively. Data from previous steps stays when the widget moves to the next step. For example, you can show a hurricane's path over one month by adding its daily positions together chronologically.

- **Style**—Choose a layout style for the widget, either Classic or Modern.
- **Appearance**—Customize the widget's foreground, background, and slider colors.
- **Display options**—Choose to include play control and autoplay.
  - **Enable play control**—Include the Play, Pause, and Speed buttons.
  - **Autoplay**—Play the time animation automatically when the widget loads.

## EEA URL Filter

The URL Filter widget provides the ability to interact with multiple datasources using URL parameters. The user can provide custom values to perform the following operations:

- Filter one or more datasources using a preconfigured field for each datasource
- Zoom to a subset of features
- Filter datasources and zoom to features

_The version of this widget is: 1.14.0_

### Settings

- **Use data source**: Select the data source(s) to filter.
- **Filter configuration** (per data source):
    - **Filter name**: Define a friendly name for the filter.
    - **Filter field**: Select the specific field to apply the filter on.

### Usage notes

To configure the widget, the user can introduce multiple datasources, set a reference name for each datasource, and select the field to be used for filter. Once configured, the URL parameters can be set as follows `application_url/?url-filter=<datasource_name>;<values_list>;<operation>`. The `operation` parameter value can be:

- filter
- filterZoom
- zoom

Multiple datasources configurations can be separated by double semicolon `;;`, as seen here.

#### Warning:

It is recommended to apply the zoom operation to a single datasource to avoid publishing multiple extent changes messages, which may lead to unexpected behaviour.

## EEA URL Filter Layer

Widget that gives user full control on finding a certain feature by URL query parameters.

_The version of this widget is: 1.7.0_

### Capabilities

- **Find** any layer from any map service within any webmap.
- Use standard **Where clause** to get the required feature. For example, `NUT0='DE'`, `NUTS_NAME='Germany'`, `OBJECTID=79`...etc. exactly as you type in REST API Query feature.
- **Highlight**: Can highlight selected feature.
- **Zoom**: Can zoom selected feature.
- **Filter**: Can filter (map will be filtered and only selected feature will be on map).
- **Center**: Can center the map on the selected feature.
- Any or all the above operators can be combined together to give the user the maximum flexibility.

### URL Format

`<experience_url>?find=FISE/FISEPercentages/MapServer/0:NUTS0='IS':highlight:filter:center:zoom`

Where:
- `find` is the query parameter
- `FISE/FISEPercentages/MapServer/0` is the service to search in format `folder/service_name/service_type/layer_id`
- `NUTS0='IS'` is the standard REST API Where clause
- `highlight` is an operator to get the selected feature highlighted
- `filter` is an operator to get get the map filtered by the selected feature
- `center` is an operator to center the map around the selected feature
- `zoom` is an operator to zoom the map to the selected feature

## EEA Zoom to selection

**The version of this widget is: 1.14.0**

### Overview

Widget used to find a layer, select a feature, center the map around it, zoom to it, and/or highlight it.

### Usage notes

To use the widget, drag it into the app and configure the settings by selecting the map from the map selector dropdown.  
The selected web map’s data source will be used as the widget’s data source.

### How does it work

To make it work, simply add parameters to the URL.

The widget supports the following capabilities:

- **Find** any layer from any map service within any web map.
- Use standard **`where`** clause syntax to get the required feature.  
  _Examples:_ `NUT0='DE'`, `NUTS_NAME='Germany'`, `OBJECTID=79` — same syntax as used in REST API feature queries.
- **Highlight** the selected feature by including `highlight` as an operation.
- **Zoom** to the selected feature with the `zoom` operation.
- **Filter** the map so that only the selected feature is visible using the `filter` operation.
- **Center** the map on the selected feature using the `center` operation.
- Any or all the above operations can be combined for maximum flexibility.

#### URL Format
##### URL Parameter Breakdown
- `find` — the main query parameter
- `FISE/FISEPercentages/MapServer/0` — the service path, in the format:  
  _folder/service_name/service_type/layer_id_
- `NUTS0='IS'` — a standard REST API `where` clause to find the feature
- `highlight` — highlights the selected feature
- `filter` — filters the map to show only the selected feature
- `center` — centers the map on the selected feature
- `zoom` — zooms to the selected feature