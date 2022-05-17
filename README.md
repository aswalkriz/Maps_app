# react-native-maps [![npm version](https://img.shields.io/npm/v/react-native-maps.svg?style=flat)](https://www.npmjs.com/package/react-native-maps)

React Native Map components for iOS + Android


## Contributing
This project is being maintained by a small group of people, and any help with issues and pull requests are always appreciated. If you are able and willing to contribute, please read the [guidelines](./CONTRIBUTING.md).



## Component API

[`<MapView />` Component API](docs/mapview.md)

[`<Marker />` Component API](docs/marker.md)

[`<Callout />` Component API](docs/callout.md)

[`<Polygon />` Component API](docs/polygon.md)

[`<Polyline />` Component API](docs/polyline.md)

[`<Circle />` Component API](docs/circle.md)

[`<Overlay />` Component API](docs/overlay.md)

[`<Heatmap />` Component API](docs/heatmap.md)

[`<Geojson />` Component API](docs/geojson.md)




### MapView Events

The `<MapView />` component and its child components have several events that you can subscribe to.
This example displays some of them in a log as a demonstration.

![](http://i.giphy.com/3o6UBpncYQASu2WTW8.gif) ![](http://i.giphy.com/xT77YdviLqtjaecRYA.gif)



### Location

![](http://i.giphy.com/3o6UBoPSLlIKQ2dv7q.gif) ![](http://i.giphy.com/xT77XWjqECvdgjx9oA.gif)




### Changing Region

One can change the mapview's position using refs and component methods, or by passing in an updated
`region` prop.  The component methods will allow one to animate to a given position like the native
API could.

![](http://i.giphy.com/3o6UB7poyB6YJ0KPWU.gif) ![](http://i.giphy.com/xT77Yc4wK3pzZusEbm.gif)


### Change the style of the map

![](http://i.imgur.com/a9WqCL6.png)



### React Views as Markers

![](http://i.giphy.com/3o6UBcsCLoLQtksJxe.gif) ![](http://i.giphy.com/3o6UB1qGEM9jYni3KM.gif)



### Using the MapView with the Animated API

The `<MapView />` component can be made to work with the Animated API, having the entire `region` prop
be declared as an animated value. This allows one to animate the zoom and position of the MapView along
with other gestures, giving a nice feel.

Further, Marker views can use the animated API to enhance the effect.

![](http://i.giphy.com/xT77XMw9IwS6QAv0nC.gif) ![](http://i.giphy.com/3o6UBdGQdM1GmVoIdq.gif)

Issue: Since android needs to render its marker views as a bitmap, the animations APIs may not be
compatible with the Marker views. Not sure if this can be worked around yet or not.

Markers' coordinates can also be animated, as shown in this example:

![](http://i.giphy.com/xTcnTelp1OwGPu1Wh2.gif) ![](http://i.giphy.com/xTcnT6WVpwlCiQnFW8.gif)



### Polygon Creator

![](http://i.giphy.com/3o6UAZWqQBkOzs8HE4.gif) ![](http://i.giphy.com/xT77XVBRErNZl3zyWQ.gif)



### Other Overlays

So far, `<Circle />`, `<Polygon />`, and `<Polyline />` are available to pass in as children to the
`<MapView />` component.

![](http://i.giphy.com/xT77XZCH8JpEhzVcNG.gif) ![](http://i.giphy.com/xT77XZyA0aYeOX5jsA.gif)



### Gradient Polylines (iOS MapKit only)

Gradient polylines can be created using the `strokeColors` prop of the `<Polyline>` component.

![](https://i.imgur.com/P7UeqAm.png?1)



### Default Markers

Default markers will be rendered unless a custom marker is specified. One can optionally adjust the
color of the default marker by using the `pinColor` prop.

![](http://i.giphy.com/xT77Y0pWKmUUnguHK0.gif) ![](http://i.giphy.com/3o6UBfk3I58VIwZjVe.gif)



### Custom Callouts

Callouts to markers can be completely arbitrary react views, similar to markers.  As a result, they
can be interacted with like any other view.

Additionally, you can fall back to the standard behavior of just having a title/description through
the `<Marker />`'s `title` and `description` props.

Custom callout views can be the entire tooltip bubble, or just the content inside of the system
default bubble.

To handle press on specific subview of callout use `<CalloutSubview />` with `onPress`.
See `Callouts.js` example.

![](http://i.giphy.com/xT77XNePGnMIIDpbnq.gif) ![](http://i.giphy.com/xT77YdU0HXryvoRqaQ.gif)



### Image-based Markers

Markers can be customized by just using images, and specified using the `image` prop.

![](http://i.imgur.com/mzrOjTR.png)



### Draggable Markers

Markers are draggable, and emit continuous drag events to update other UI during drags.

![](http://i.giphy.com/l2JImnZxdv1WbpQfC.gif) ![](http://i.giphy.com/l2JIhv4Jx6Ugx1EGI.gif)

### Lite Mode ( Android )

Enable lite mode on Android with `liteMode` prop. Ideal when having multiple maps in a View or ScrollView.

![](http://i.giphy.com/qZ2lAf18s89na.gif)

### On Poi Click (Google Maps Only)

Poi are clickable, you can catch the event to get its information (usually to get the full detail from Google Place using the placeId).

![](https://media.giphy.com/media/3480VsCKnHr31uCLU3/giphy.gif)



### Zoom to Specified Markers

Pass an array of marker identifiers to have the map re-focus.

![](http://i.giphy.com/3o7qEbOQnO0yoXqKJ2.gif) ![](http://i.giphy.com/l41YdrQZ7m6Dz4h0c.gif)

### Zoom to Specified Coordinates

Pass an array of coordinates to focus a map region on said coordinates.

![](https://cloud.githubusercontent.com/assets/1627824/18609960/da5d9e06-7cdc-11e6-811e-34e255093df9.gif)

