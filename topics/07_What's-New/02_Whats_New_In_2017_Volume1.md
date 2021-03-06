﻿<!--
|metadata|
{
    "fileName": "whats-new-in-2017-volume1",
    "controlName": [],
    "tags": []
}
|metadata|
-->

# What's New in 2017 Volume 1

This topic presents the controls and the new and enhanced features for the Ignite UI™ 2017 Volume 1 release.


## What’s New Summary

The following summarizes what’s new in 2017 Volume 1. Additional details follow.

### igSpreadsheet

Feature | Description
---|---
[New control igSpreadsheet](#spreadsheet)| The igSpreadsheet is a jQuery widget that visualize excel documents in all modern browsers.

### igScheduler

Feature | Description
---|---
[New control igScheduler](#scheduler)| The igScheduler is a jQuery widget that provides a common scheduling solution for presenting and managing time periods and the associated activities.

### igDataSource

Feature | Description
---|---
[Filter By Text](#filterbytext)| The igDataSource component provides a way to search for a specific words or phrases in all of its fields.

### igGrid

Feature | Description
---|---
[Date Handling](#griddatehandling)| The igGrid provides a way to control the display and edit of date values for clients in different time zones.
[More Flexible Caption](#gridcaption)| igGrid's new caption is designed to be more flexible and customizable.
[GroupBy Summaries](#groupSummaries)| The GroupBy feature now allows a summary row to be displayed below and/or above each group data island.

### igCombo

Feature | Description
---|---
[Knockout Disable Handler](#comboKnockoutDisable)| Knockout Disable binding handler has been implemented for the combo.

### Editors

Feature | Description
---|---
[Knockout Disable Handler](#editorsKnockoutDisable)| Knockout Disable binding handler has been implemented for the editors.


### igNumericEditor

Feature | Description
---|---
[Round Decimals](#roundDecimals)| The numeric editor introduces new option [`roundDecimals`](ui.ignumericeditor#options:roundDecimals) that allows to round values with decimal point.

### igDateEditor/igDatePicker

Feature | Description
---|---
[Date Handling](#dateHandling)| New editors' settings are needed when handling date transfers.

### igDatePicker

Feature | Description
---|---
[Date Picker Options MVC wrapper](#pickerOptionsWrapper) | When using DatePicker MVC wrapper, now additional wrapper for the date picker options is available.

### igDataChart

Feature | Description
---|---
[Zoom Enabling Options](#zoomEnablingProperties) | New options called [`isHorizontalZoomEnabled`](%%jQueryApiUrl%%/ui.igDataChart#options:isHorizontalZoomEnabled) and [`isVerticalZoomEnabled`](%%jQueryApiUrl%%/ui.igDataChart#options:isHorizontalZoomEnabled) have been added which control whether zooming is allowed on either the horizontal or vertical axis.

### igMap

Feature | Description
---|---
[OpenStreet Tile Path](#tilePathProperty) | The option called [`tilePath`](%%jQueryApiUrl%%/ui.igMap#options:backgroundContent.tilePath) has been added to the [`backgroundContent`](%%jQueryApiUrl%%/ui.igMap#options:backgroundContent) option for the OpenStreet tile source.

### igRadialGauge, igLinearGauge, igBulletGraph
Feature | Description
---|---
[Design Changes](#gaugeDesignChanges) | The visuals for the gauges have been updated.


## <a id="spreadsheet"></a>igSpreadsheet

In version 2017.1 we introduce the igSpreadsheet control. It is a jQuery widget that visualize excel documents in all modern browsers. For MVP version, the control has the following areas and features available:

-   Configurable component areas
    -   Formula Bar
    -   Context Menu
    -   Tab Bar Area
    -   Headers

-   Control manipulations

    -   Selection
    -   Resizing
    -   Hiding
    -   Freezing Panes
    -   Splitting Panes
    -   Zooming

-   Data manipulations
    -   Inserting and Deleting Cells, Columns and Rows
    -   Undo and Redo
    -   Copy and Paste
    -   Data Validation
    -   Worksheets
    -   Hyperlinks

-   Visual configurations
    -   Gridlines
    -   Cell Alignment
    -   Cell Borders
    -   Font Styles


![](images/spreadsheet.png)

#### Related Topics
-   [igSpreadsheet Overview](igspreadsheet-overview.html)
-   [Adding igSpreadsheet](adding-igspreadsheet.html)
-   [Configuring igSpreadsheet](igspreadsheet-configuring.html)


#### Related Samples
-   [Overview](%%SamplesUrl%%/spreadsheet/overview)
-   [View Configuration](%%SamplesUrl%%/spreadsheet/create-view-save)
-   [Import Data From Excel File](%%SamplesUrl%%/spreadsheet/loading-data)

## <a id="scheduler"></a> igScheduler
### New Control

The `igScheduler`™ control provides a common scheduling solution for presenting and managing time periods and the associated activities.

### Supported features:
-   Creating, editing and deleting of appointment.
    -   Configurable appointments display mode in the month view calendar (indicator or event subject).
    -   Assigning appointments to color themed resources.
-   Using different views (month and agenda view).
    -   Month and agenda views switching support
    -   Agenda view in month view support.
    -   Configurable agenda view days display range.
-   All day events supported.
-   Desktop, tablet and phone layout.
-   Responsive design.
    -   Desktop environment optimized UI.
-   Resources color scheme support.
-   Keyboard navigation support.
-   Localization support.

![](../02_Controls/igScheduler/images/scheduler.png)

#### Related Topics
-   [igScheduler Overview](igScheduler-Overview.html)
-   [Configuring igScheduler](igscheduler-configuring.html)
-	[Adding igScheduler](igscheduler-adding-igscheduler.html)
-	[Configuring igScheduler](igscheduler-Configuring.html)
-	[Styling igScheduler](igscheduler-using-themes.html)
-	[Accessibility Compliance (igScheduler)](igscheduler-accessibility-compliance.html)
-	[Known Issues and Limitations (igScheduler)](igscheduler-known-limitations.html)

#### Related Samples

-   [igScheduler Agenda View](%%SamplesUrl%%/scheduler/agenda-view)
-   [igScheduler Appointment Indicators](%%SamplesUrl%%/scheduler/appointment-indicators)

## igDataSource

### <a id="filterbytext"></a> Filter By Text

The igDataSource component provides a way to search for a specific words or phrases in all of its fields via the [`filterByText`](%%jQueryApiUrl%%/ig.datasource#methods:filterByText) method.

#### Related Topics
-   [igDataSource Overview](igdatasource-igdatasource-overview.html)


#### Related Samples
-   [Simple Filtering](%%SamplesUrl%%/grid/simple-filtering)

## igGrid

### <a id="griddatehandling"></a> Date Handling

The [`enableUTCDates`](%%jQueryApiUrl%%/ui.iggrid#options:enableUTCDates) now have new function. It affects only the dates serialization. Dates are now serialized as [UTC ISO 8061](https://en.wikipedia.org/wiki/ISO_8601#UTC) string instead of using the local time and zone values.

In order to handle the displaying of the dates a new option [`dateDisplayType`](%%jQueryApiUrl%%/ui.iggrid#options:columns.dateDisplayType) is introduced in the grid column's definition and it works only for columns of type `date`. 

#### Related Topics
-   [Migrating enableUTCDates option after 17.1](migrating-enableutcdates-option-in-17-1.html)


### <a id="gridcaption"></a> Grid's Caption

The igGrid's caption now provides the ability to render HTML elements in it in order to give the user more customizability and flexibility. It also comes with useful events for full control of its initialization.

### <a id="groupSummaries"></a> GroupBy Summaries

The GroupBy Summaries feature allows an additional summary row to be displayed below and/or above each group data island that displays summary information for the data columns in that island. The summary row is visible only when the related group is expanded.

![](images/group-summaries.png)

#### Related Topics
-   [GroupBy Summaries Feature Overview (igGrid)](igGrid-GroupBy-Summaries.html)

#### Related Samples
-   [Grouping with summaries](%%SamplesUrl%%/grid/grouping)


## igCombo

### <a id="comboKnockoutDisable"></a> Knockout Disable Handler

If a developer wants to apply the Knockout [`disabled`](http://knockoutjs.com/documentation/disable-binding.html) binding handler to the combo control, it will not work and will not automatically enables/disables it. This is because combo has a special logic that handles enabling/disabling of the control. For that purpose additional `igComboDisable` binding handler is created, which implements the behavior, expected, when using the Knockout `disabled` handler.

#### Related Topics
-   [Configuring Knockout Support (igCombo)](igCombo-KnockoutJS-Support.html#)

## Editors

### <a id="editorsKnockoutDisable"></a> Knockout Disable Handler

If a developer wants to apply the Knockout [`disabled`](http://knockoutjs.com/documentation/disable-binding.html) binding handler to the editors, it will not work and will not automatically enables/disables them. This is because editors have a special logic that handles enabling/disabling of the control. For that purpose additional `igEditorDisable` binding handler is created, which implements the behavior, expected, when using the Knockout `disabled` handler.

#### Related Topics
-   [Configuring Knockout Support (Editors)](Configuring-Knockout-Support-%28Editors%29.html)


## igNumericEditor

### <a id="roundDecimals"></a> Round Decimals

In previous versions of the product, if user sets or enters a value in a numeric editor that has more decimal places than the one defined in the `maxDecimals` option, then the value was truncated. E.g. If an editor with defined 'maxDecimals' to `3`, receives a value `123.4567`, then it will be truncated to `123.456`. With version 17.1 of the product, a new option [`roundDecimals`](ui.ignumericeditor#options:roundDecimals) is introduced, which is enabled by default and rounds the numeric values, using the JavaScript `Math.round()` function. This means that the value of `123.4567` will be rounded and displayed in the editor as `123.457`. If the [`roundDecimals`](ui.ignumericeditor#options:roundDecimals) is disabled, then it will truncate the value and will show it as `123.456`, like in the old versions.

## igDateEditor/igDatePicker

### <a id="dateHandling"></a> Date Handling

When the dates in the editors are transferred from the client to the server аnd vice versa, the options [`enableUTCDates`](%%jQueryApiUrl%%/ui.igdateeditor#options:enableUTCDates) and [`displayTimeOffset`](%%jQueryApiUrl%%/ui.igdateeditor#options:displayTimeOffset) can be used to configure the editоrs and to properly handle date transfer.

#### Related Topics
-   [Migrating date handling in 17.1](igDateEditor-migrating-date-handling-in-17-1.html)
-   [Ignite UI controls in different time zones](Using-IgniteUI-controls-in-different-time-zones.html)

## igDatePicker

### <a id="pickerOptionsWrapper"></a> Date Picker Options MVC wrapper

The DatePicker MVC wrapper is extended to allow the definition of the date picker options, using additional MVC wrapper. The new wrapper contains all the jQuery UI datepicker options that can be applied to our igDatePicker. Here is an example of how it can be configured in MVC:

```
@(Html.Infragistics()
	.DatePicker()
	.DropDownAnimationDuration(1000)
	.DatePickerOptions(options => {
		 options.DefaultDate("+8");
		 options.MinDate("-5d");
		 options.MaxDate("+10d");

		 options.FirstDay(FirstWeekDay.Monday);
		 options.ShowWeek(true);

		 options.ShowOtherMonths(true);
		 options.SelectOtherMonths(true);

		 options.ChangeMonth(true);
		 options.ChangeYear(true);
		 options.AddClientEvent("onChangeMonthYear", "onChangeMonthYearHandler");

		 options.ShowButtonPanel(true);
		 options.GoToCurrent(true);

		 options.ShowAnim(AnimationEffect.Show);

		 options.AddClientEvent("onSelect", "onSelectHandler");
		 options.AddClientEvent("onClose", "onCloseHandler");
	})
	.Render())
```

## </a>igDataChart
### <a id="zoomEnablingProperties"></a> Zoom Enabling Options

New options called [`isHorizontalZoomEnabled`](%%jQueryApiUrl%%/ui.igDataChart#options:isHorizontalZoomEnabled) and [`isVerticalZoomEnabled`](%%jQueryApiUrl%%/ui.igDataChart#options:isVerticalZoomEnabled) were added, deprecating the existing [`horizontalZoomable`](%%jQueryApiUrl%%/ui.igDataChart#options:horizontalZoomable) and [`verticalZoomable`](%%jQueryApiUrl%%/ui.igDataChart#options:verticalZoomable) options respectively.  The older options are being left as-is in this release for backwards compatibility with existing applications.

## igMap
### <a id="tilePathProperty"></a> OpenStreet Tile Path

Open Street Map can now accept custom tile source by re-purposing the [`tilePath`](%%jQueryApiUrl%%/ui.igMap#options:backgroundContent.tilePath) option off of the [`backgroundContent`](%%jQueryApiUrl%%/ui.igMap#options:backgroundContent) object.

**In JavaScript**

	$(function () {
            $("#map").igMap({
                width: "700px",
                height: "500px",
                windowRect: { left: 0.1, top: 0.1, height: 0.7, width: 0.7 },
                // specifies imagery tiles from OpenStreetMap
                backgroundContent: {
                    type: "openStreet",
                    tilePath: "tile.openstreetmap.org/{Z}/{X}/{Y}.png"
                }
            });
        });

Before this change [`tilePath`](%%jQueryApiUrl%%/ui.igMap#options:backgroundContent.tilePath) was only relevant to the Bing Map. After the change it is applicable to the Open Street Map as well.

Omitting the protocol specifier (*http:* or *https:*) in the URL allows for the control to detect and use the protocol of the hosting web site. It is also possible to force the control into desired protocol by explicitely setting it in the *tilePath* option:

**In JavaScript**

    tilePath: "https://tile.openstreetmap.org/{Z}/{X}/{Y}.png"

*{Z}*, *{X}*, and *{Y}* tokens are replaced during tile rendering by Zoom, Horizontal location, and Vertical location of each tile respectively.


## igRadialGauge, igLinearGauge, igBulletGraph
### <a id="gaugeDesignChanges"></a> Design Changes

The igRadialGauge, igLinearGauge and igBulletGraph have new styling provided when you include `infragistics.theme.css`.  The new styling looks as follows:

#### igRadialGauge:
![](images/radialgauge_igtheme_17_1.png)

#### igLinearGauge:
![](images/lineargauge_igtheme_17_1.png)

#### igBulletGraph:
![](images/bulletgraph_igtheme_17_1.png)