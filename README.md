# ion-select-picker

An ionic/angular select drawer to be used with strings or objects which is developed in web technologies but looks similar to native.

## Requirements

- Angular 1.*

## ScreenShots
![alt tag](/screenshots/screenshot1.gif)
![alt tag](/screenshots/screenshot2.png)

## Usage

- Add CSS and JS to project:

```html
<link rel="stylesheet" href="wherever-you-put-it/ionSelectPicker.min.css">

<script type="text/javascript" src="wherever-you-put-it/ionSelectPicker.min.js"></script>
```

Add dependencies on the `ion-select-picker` AngularJS module:

```javascript
angular.module('myApp', ['ion-pickers']);
```

You can now use the directive, add the attribute to your existing DOM element in HTML:
```html
<input type="text" ng-model="value" items="myItems" ion-select-picker>
```

## Directive Attributes

- `items` - an array of items to display as options
- `id (optional)` - Give a unique id to the bound element and drawer will be named {{id}}-drawer
- `ng-model` (optional) - Define the model to bind the selected value to. the value of the model is displayed once drawer is open
- `ng-value` (optional) - If using objects instead of string values in the component define attribut of object that will be displayed as an option and as ngModel value
- `ng-change` (optional) - method called after the value has been set
- `sensitivity (optional)` - Define the scroll sensitivity
- `ngDefault` (optional) - if ng-model is null then the selector drawer opens on this item as selected
- `isClickSelect` (optional) - if set to true, when user clicks element it will be selected and drawer closed. Default is false
- `control` (optional) - control element to control directive from outside (see notes for details)
- `hasClear` (optional) - Whether drawer has clear button or not, if does value set to zero
- `onSet` (optional) - event fired when set button clicked, model is set value. Has two params oldValue and newValue, If returning false from method set canceled. IMPORTANT: only pass method name without brackets
- `onCancel` (optional) - event fired when cancel button clicked. IMPORTANT: only pass method name without brackets
- `onClear` (optional) - event fired when clear button clicked. IMPORTANT: only pass method name without brackets

## Example with objects

```javascript
$scope.myitems = [
    { id: 90210 stringValue: "Beverly Hills"},
    { id: 42 stringValue: "The answer to life"}
];
```

and in html:

```html
<input type="text" ng-model="myModel" items="myItems" ng-value="stringValue" ion-select-picker>
```

## Notes

Valid values:
- Make sure you if using objects to set ng-Value to an existing property of items
- `items` attribute is mandatory, make sure to set it to a valid collection
- Control methods which can be called:
 * `openDrawer` - opens the drawer
 * `closeDrawer` - closes the drawer
 * `getCurrentSelection` - returns the current value displayed as selected in select drawer
 * `isDrawerOpen` - is the drawer currently open or not

## Purchase Link
[ion-select-picker](https://gum.co/vFEVL)

## What's included
Upon purchase you'll receive a minimized js file and minimized css for immediate use

## License
Use only by person/business specified in payment for one or more end products
TODO
