# Ember-cli-bing-map

Simple bing map component for ember-cli

## Installation

```
ember install ember-cli-bing-map
``` 

## Usage

The component should take the style properties from its parent.

```
<div style="position: relative; width: 700px; height: 700px">
  {{bing-map lat=lat lng=lng zoom=zoom mapTypeId=mapTypeId markers=markers polygonLocation=polygonObject}}
</div>

```
Add reference to the map control in the index.html.

```
<script charset="UTF-8" type="text/javascript" src="http://ecn.dev.virtualearth.net/mapcontrol/mapcontrol.ashx?v=7.0"></script>
```
Add Bing API to environment.js.

```
bingAPI: 'API-KEY',
```

## Entities

Current available entities:

`lat` - `number value` 

`lng` - `number value`

`zoom` - `integer up to 20`

`mapTypeId` - `string value: 'a' for aerial view, 'r' for road view `

`markers` - `array of objects with lat and lng values`

example:

```
markers: [
  {
    lat: 18.35570,
    lng: -66.004951
  }
]
```

`polygonLocation`

example:

```
  polygonLocation: {
    location1:{
      lat: 18.5,
      lng: -66.3
    }, 
    location2:{
      lat:18.5,
      lng:-65.9
    },
    location3:{
      lat: 18.15,
      lng: -65.9
    },
    location4:{
      lat: 18.15,
      lng: -66.3
    },
  }
```

## Demo

[Demo](http://cometaworks.github.io/ember-cli-bing-map/)