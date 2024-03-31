# Mapbox-gl wrapper for Dart

Library to use Mapbox GL JS from Dart. Working examples here: https://andrea689.github.io/mapbox-gl-dart/

## Using this package

You must include [Mapbox GL JS](https://github.com/mapbox/mapbox-gl-js) into your `.html` file
to be able to use this package.

```html
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v2.5.1mapbox-gl.js'></script>
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v2.5.1/mapbox-gl.css' rel='stylesheet'/>
```

In the body add a container for the map.

```html
<body>
    <div id='map'></div>
</body>
```

In the dart file initialize the map.

```dart
import 'package:mapbox_gl_dart/mapbox_gl_dart.dart' as mapboxgl;

void main() {
  Mapbox.accessToken = 'YOUR_TOKEN_HERE';

  var map = MapboxMap(
    MapOptions(
      container: 'map',
      style: 'mapbox://styles/mapbox/dark-v10',
      center: LngLat(7.68227, 45.06755),
      zoom: 12,
    ),
  );
}
```

## Contribution

Install requirements

```bash
dart pub get
```

## Examples

You can find many examples in the [example](example) folder.

## Run example

Activate webdev

```bash
dart pub global activate webdev
```

Serve examples

```bash
webdev serve example:8081
```

Open browser to http://localhost:8081
