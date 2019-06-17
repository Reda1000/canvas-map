# canvas-map
HTML5 Canvas map for showing isometric and cartesian maps. 

''Currently under development / testing / documentation. and therefore not fully available yet.''

## Usage
Render a map in your Browser:

        <script src="../canvasmap.bundle.js"></script>
        <script>
            console.log(document.getElementById('canvas'), document.getElementById('canvas').addEventListener, canvasmap);

            var test = new canvasmap.IsoMap({
                window: {
                    nativeElement: window
                },
                parent: {
                    nativeElement: document.getElementById('parent')
                },
                cnvs: {
                    nativeElement: document.getElementById('canvas')
                }
            }, {
                quality: 1,
                zoomStepTap: 0.5,
                zoomStepScrollDebouncer: 100,
                maxZoom: 6,
                maxSize: 16000,
                maxOffset: 300,
                topOffset: 0.58375,
                topOffsetCenterCalcModification: true,
                refresh: 'automatic',
                style: {
                    map: {
                        backgroundColor: 'grey',
                        borderColor: 'lightgrey',
                        borderWidth: 0
                    },
                    tile: {
                        backgroundColor: '#4f4f4f',
                        borderColor: 'darkgrey',
                        borderWidth: 0,
                        fontSize: 0.16739,
                        fontFamily: 'Arial',
                        fontColor: 'black',
                        textAlign: 'center'
                    },
                    selectedTile: {
                        backgroundColor: 'yellow',
                        borderColor: 'grey',
                        borderWidth: 2,
                        fontSize: 0.26739,
                        fontFamily: 'Arial',
                        fontColor: 'black',
                        textAlign: 'center'
                    }
                },
                cheat: {
                    imgTileHeightAdjustment: -21,
                    imgTileHeightOffsetAdjustment: 0.07
                }
            }, {
                "size": [10, 7],
                "tiles": [{
                    "coord": [0, 0],
                    "layers": ["wall_u_l", "wall_u_r"],
                    "name": [{
                        "zoom": 1,
                        "text": "Office"
                    }, {
                        "zoom": 3,
                        "text": "Entrance"
                    }],
                }, {
                    "coord": [0, 1],
                    "layers": ["wall_u_l"],
                }, {
                    "coord": [0, 2],
                    "layers": ["wall_u_l"],
                    "name": [{
                        "zoom": 3,
                        "text": "Sales"
                    }],
                }, {
                    "coord": [0, 3],
                    "layers": ["wall_u_l"],
                }, {
                    "coord": [0, 4],
                    "layers": ["wall_u_l"],
                    "name": [{
                        "zoom": 3,
                        "text": "QA"
                    }],
                }, {
                    "coord": [0, 5],
                    "layers": ["wall_u_l"],
                }, {
                    "coord": [0, 6],
                    "layers": ["wall_u_l"],
                    "name": [{
                        "zoom": 3,
                        "text": "Planning"
                    }],
                }, {
                    "coord": [1, 0],
                    "layers": ["wall_u_r", "wall_b_r", "door_west_east"],
                }, {
                    "coord": [1, 1],
                    "layers": ["wall_b_r"],
                }, {
                    "coord": [1, 2],
                    "layers": ["wall_b_r"],
                }, {
                    "coord": [1, 3],
                    "layers": ["wall_b_r"],
                }, {
                    "coord": [1, 4],
                    "layers": ["wall_b_r"],
                }, {
                    "coord": [1, 5],
                    "layers": ["wall_b_r"],
                }, {
                    "coord": [1, 6],
                    "layers": ["wall_b_r"],
                }, {
                    "coord": [2, 0],
                    "layers": ["wall_u_r"],
                }, {
                    "coord": [2, 1],
                    "layers": ["door_north_south"],
                }, {
                    "coord": [2, 2],
                    "layers": ["machine"],
                    "name": [{
                        "zoom": 1,
                        "text": "Machining"
                    }, {
                        "zoom": 2,
                        "text": "Machine 1"
                    }],
                }, {
                    "coord": [2, 3],
                    "layers": ["machine"],
                    "name": [{
                        "zoom": 2,
                        "text": "Machine 2"
                    }],
                }, {
                    "coord": [2, 4],
                    "layers": ["machine"],
                    "name": [{
                        "zoom": 2,
                        "text": "Machine 3"
                    }],
                }, {
                    "coord": [2, 5],
                    "layers": ["machine"],
                    "name": [{
                        "zoom": 2,
                        "text": "Machine 4"
                    }],
                }, {
                    "coord": [2, 6],
                    "layers": ["machine"],
                    "name": [{
                        "zoom": 2,
                        "text": "Machine 5"
                    }],
                }, {
                    "coord": [3, 0],
                    "layers": ["wall_u_r"],
                }, {
                    "coord": [3, 1],
                    "layers": ["road_crossroad_south"],
                }, {
                    "coord": [3, 2],
                    "layers": ["road_up"],
                }, {
                    "coord": [3, 3],
                    "layers": ["road_up"],
                }, {
                    "coord": [3, 4],
                    "layers": ["road_up"],
                }, {
                    "coord": [3, 5],
                    "layers": ["road_crossroad_east"],
                }, {
                    "coord": [4, 0],
                    "layers": ["wall_u_r", "warehouse"],
                }, {
                    "coord": [4, 1],
                    "layers": ["road_down"],
                }, {
                    "coord": [4, 2],
                    "layers": ["warehouse"],
                }, {
                    "coord": [4, 3],
                    "layers": ["workcenter_01"],
                }, {
                    "coord": [4, 4],
                    "layers": ["warehouse"],
                }, {
                    "coord": [4, 5],
                    "layers": ["road_down"],
                }, {
                    "coord": [4, 6],
                    "layers": ["warehouse"],
                }, {
                    "coord": [5, 0],
                    "layers": ["wall_u_r", "warehouse"],
                    "name": [{
                        "zoom": 2,
                        "text": "Warehouse 1"
                    }],
                }, {
                    "coord": [5, 1],
                    "layers": ["road_down"],
                }, {
                    "coord": [5, 2],
                    "layers": ["warehouse"],
                }, {
                    "coord": [5, 3],
                    "layers": ["workcenter_01"],
                }, {
                    "coord": [5, 4],
                    "layers": ["warehouse"],
                    "name": [{
                        "zoom": 2,
                        "text": "Warehouse 2"
                    }],
                }, {
                    "coord": [5, 5],
                    "layers": ["road_down"],
                }, {
                    "coord": [5, 6],
                    "layers": ["warehouse"],
                }, {
                    "coord": [6, 0],
                    "layers": ["wall_u_r", "warehouse"],
                }, {
                    "coord": [6, 1],
                    "layers": ["road_down"],
                }, {
                    "coord": [6, 2],
                    "layers": ["warehouse"],
                }, {
                    "coord": [6, 3],
                    "layers": ["workcenter_01"],
                }, {
                    "coord": [6, 4],
                    "layers": ["warehouse"],
                }, {
                    "coord": [6, 5],
                    "layers": ["road_down"],
                }, {
                    "coord": [6, 6],
                    "layers": ["warehouse"],
                }, {
                    "coord": [7, 0],
                    "layers": ["wall_b_r", "wall_u_r", "road_crossroad_south"]
                }, {
                    "coord": [7, 1],
                    "layers": ["wall_b_r", "road_crossroad_w_n_e"]
                }, {
                    "coord": [7, 2],
                    "layers": ["wall_b_r", "road_crossroad_east"]
                }, {
                    "coord": [7, 3],
                    "layers": ["wall_b_r"]
                }, {
                    "coord": [7, 4],
                    "layers": ["wall_b_r", "road_crossroad_south"]
                }, {
                    "coord": [7, 5],
                    "layers": ["wall_b_r", "road_crossroad_w_n_e"]
                }, {
                    "coord": [7, 6],
                    "layers": ["wall_b_r", "road_crossroad_east"]
                }, {
                    "coord": [8, 0],
                    "layers": ["door_north_south"],
                    "name": [{
                        "zoom": 1,
                        "text": "Delivery"
                    }, {
                        "zoom": 3,
                        "text": "Zone 4"
                    }],
                }, {
                    "coord": [8, 1],
                    "layers": [],
                }, {
                    "coord": [8, 2],
                    "layers": ["door_north_south"],
                    "name": [{
                        "zoom": 3,
                        "text": "Zone 3"
                    }],
                }, {
                    "coord": [8, 3],
                    "layers": [],
                }, {
                    "coord": [8, 4],
                    "layers": ["door_north_south"],
                    "name": [{
                        "zoom": 3,
                        "text": "Zone 2"
                    }],
                }, {
                    "coord": [8, 5],
                    "layers": [],
                }, {
                    "coord": [8, 6],
                    "layers": ["door_north_south"],
                    "name": [{
                        "zoom": 3,
                        "text": "Zone 1"
                    }],
                }]
            });
            test.setSelectedCB((a) => console.log(a));
        </script>
        
## Depends
HTML5 Canvas

## Installing
npm install canvas-map

## Tests
Not yet available
License

MIT, see LICENSE.txt
