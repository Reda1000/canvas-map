# canvas-map
HTML5 Canvas map for showing isometric and cartesian maps. 

__Currently under development / testing / documentation. and therefore not fully available yet.__

## Depends
HTML5 Canvas

## Usage
Render a map in your Browser in simple JS:

    <script src="http://cdn.jsdelivr.net/gh/Reda1000/canvas-map/canvasmap.bundle.min.js"></script>
    <script src="http://cdn.jsdelivr.net/gh/Reda1000/canvas-map/example.map.js"></script>
    <script>
        config = undefined; // use internal standard config
        map = defaultMap
        mapInstance = new canvasmap.IsoMap({
            window: { nativeElement: window },
            parent: { nativeElement: document.getElementById('parent') },
            cnvs: { nativeElement: document.getElementById('canvas') }
        }, config, map);
        mapInstance.setSelectedCB((a) => console.log(a));
    </script>

Hint: In case you are interesting in an Angular2+ Typescript Port please have a look at ngx-canvas-map in NPM - planning on porting to ReactJS as well.

## Demo
Panning ![alt text](https://github.com/Reda1000/canvas-map/blob/master/localhost_8080_test-iso_index.html%20-%20Google%20Chrome%2017.06.2019%2022_17_12.mp4)
Zooming ![alt text](https://github.com/Reda1000/canvas-map/blob/master/localhost_8080_test-iso_index.html%20-%20Google%20Chrome%2017.06.2019%2022_17_00.mp4)

## Documentation
<!-- 
@startuml

interface CoordResolverInterface
abstract class CoordResolver
class CartCoordResolver
class IsoCoordResolver

CoordResolverInterface <|-- CoordResolver
CoordResolver <|-- CartCoordResolver
CoordResolver <|-- IsoCoordResolver

interface CanvasConfig
class Config

CanvasConfig <|-- Config : default of <

interface CanvasSettings

interface CanvasLayer

class CanvasRenderer
class Controller
Controller -left- CanvasRenderer : controls >
CanvasRenderer -left- CoordResolver : renders via >
Controller .. CanvasSettings : Memory
Controller .. CanvasLayer : LayerSetup
Controller .. CanvasConfig : Configuration

interface MapConfig
interface Map<T>
interface Tile<T>
MapConfig <|-right- Map
Map -right- Tile : contains n >
Map -- Controller

enum ORRIENTATION {
WEST,
NORTH,
EAST,
SOUTH
}

@enduml
-->
![alt text](https://github.com/Reda1000/canvas-map/blob/master/diagram.png)

## Installing
npm install canvas-map

## Tests
Not yet available
License

## Contribution
Very thankful for the assets that are being used in the examples from https://github.com/BulloRosso/isoplant

## License
MIT, see LICENSE.txt
