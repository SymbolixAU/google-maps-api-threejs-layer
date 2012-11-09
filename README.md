# Three.js Layer for the Google Maps API

Google Maps API layer that uses [Three.js](http://mrdoob.github.com/three.js/) to for super fast animation.

### Usage

```js
new ThreejsLayer(options, completeCallback);
```

### Example


```js
new ThreejsLayer({ map: map }, function(layer){
  
  var geometry = new THREE.Geometry(),
    location = new google.maps.LatLng(lat, lng),
    vertex = layer.fromLatLngToVertex(location);

  geometry.vertices.push( vertex );

  var particles = new THREE.ParticleSystem(geometry, material);
  layer.add(particles);
});

```

### About

Developed by [Martin Kleppe](https://plus.google.com/103747379090421872359/) at [Ubilabs](http://www.ubilabs.net). 

Released under the MIT Licence.