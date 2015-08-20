# ionic-sidetabs

This module creates side tabs for Ionic. Side tabs are useful to organize a lot of information that wouldn't fit in smaller screen devices.
It is also an easy way to reveal information that can be easily expanded/collapsed when scrolling is not desirable.

- Tabs are easily customized
- Uses hardware accelerated CSS - great performance!
- Integrates with Ionic's themes
- Multiple tabs are automatically stacked vertically - see examples below
- Exposes interface for expand/collapse events

## Install module

To get you started you can simply install via bower

```bower install ionic-sidetabs```


Then include ```ion-sidetabs.js``` in your HTML
````
 <script src="js/ion-sidetabs.js"></script>
````

## Add dependencies to your App

```
angular.module('starter', ['ionic', 'starter.controllers', 'ionic-sidetabs'])
```

## Directives

### ion-side-tabs
Defines a group of tabs to be stacked vertically. It also exposes the onExpand and onCollapse callbacks.

````
<ion-side-tabs on-expand="tabExpand(index)" on-collapse="tabCollapse(index)">
...
</ion-side-tabs>
````


### ion-side-tab
Defines a single tab. Tabs can be customized using Ionic's theme classes. Special styling such as rounded corners must
be specified via inline styles

````
<ion-side-tab class="dark-bg" style="border-radius: 10px;">
  <ion-side-tab-handle width="40" height="50" toggle="ion-chevron-left ion-chevron-right" class="dark-bg stable" style="border-radius: 10px 0 0 10px"><i class="icon ion-chevron-left"></i></ion-side-tab-handle>
  <div class="list card">
    <div class="item item-divider">Upcoming</div>
    <div class="item item-body item-stable">
      <div>
        You have <b>229</b> meetings on your calendar tomorrow.
      </div>
    </div>
  </div>
  <div class="list card">
    <div class="item item-divider">Upcoming</div>
    <div class="item item-body item-stable">
      <div>
        You have <b>21</b> meetings on your calendar tomorrow.
      </div>
    </div>
  </div>
</ion-side-tab>
````

### ion-side-tab-handle
Defines the handle that triggers expand and collapse events. It also supports dragging to open the tab manually.
Use ```width``` and ```height``` to control the handle size. To include text or icons, simply add them as child elements.
If using Ionicons, the ```toggle``` parameter can be used to show a specific icon for each state.

````
<ion-side-tab-handle width="40" height="50" toggle="ion-chevron-left ion-chevron-right" class="dark-bg stable" style="border-radius: 10px 0 0 10px">
    <i class="icon ion-chevron-left"></i>
</ion-side-tab-handle>
````