# md-date-picker
angular material customizable date picker directive/component  

[![npm version](https://badge.fury.io/js/md-date-picker.svg)](http://badge.fury.io/js/md-date-picker)

## Demo

- `clone repository`
- `npm install`
- `gulp serve`

### Dependencies
angularjs, angular material

### usage
```shell
bower install md-date-picker --save
//or
npm install md-date-picker --save
```
```javascript
//module
var app = angular.module('app', ['md-date-picker']);
```
```javascript
//options
$scope.specialDaysClass['8/5/2017'] = 'blue-day'; // blue color on saturday 
$scope.specialDaysClass['1/1/2017'] = { // red color on new years day with title
  class: 'red-day',
  title: 'New Year',
};
```
```scss
// sample custom css
.blue-day {
  color: blue;
}
.red-day {
  color: blue;
}
```
```html
<!--default-->
<md-date-picker ng-model="date" on-change="date = $date" placeholder="Select Date"></md-date-picker>
<!--show only days on current month view-->
<md-date-picker current-month-view-dates-only="true" ng-model="date" on-change="date = $date"></md-date-picker>
<!-- with special days calss and promise handling -->
<md-date-picker loading="loading" date-class="specialDaysClass" on-render="onRenderDatePicker($month, $year)" ng-model="date" on-change="date = $date"></md-date-picker>
<!-- customizable date format -->
<md-date-picker ng-model="custom" format="EEE, MMM dd, yyyy" on-change="custom = $date"></md-date-picker>
```

```
clone repository and run gulp for demo http://localhost:3000
```

![md-date-picker Screenshot](https://raw.githubusercontent.com/appfoundations/md-date-picker/master/preview.png "md-date-picker Screenshot")

### Todos

 - Enhancements
 - Optimizations
 - Unit Tests

License
----

MIT


**Version 0.0.1**
