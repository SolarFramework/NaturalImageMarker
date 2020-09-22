# SolAR Natural Image Marker

[![License](https://img.shields.io/github/license/SolARFramework/NaturalImageMarker?style=flat-square&label=License)](https://www.apache.org/licenses/LICENSE-2.0)

The SolAR **Natural Image Marker sample** show a SolAR pipeline for augmented reality based on a natural image.
 
This pipeline loads a reference image marker, then tries to detect it on real-time camera images and to estimate the pose of the camera in relation to the coordinate system of the image marker. If the marker is detected, the pipeline over the current camera image renders a 3D cube from a virtual camera which pose corresponds to the one estimated by the pipeline.


| ![](./StandAlone/standalone.jpg) | ![](./Plugin/plugin.jpg) |
|:-:|:-:|
| StandAlone/Multithread | Plugin | 


## How to run

* To run it, first print the marker [graf1.png](./StandAlone/graf1.png).

* If you want to change your natural image, you can edit the [grafMarker.yml](./StandAlone/grafMarker.yml).

* If you want to change the calibration parameters of the camera, edit the [camera_calibration.yml](./StandAlone/camera_calibration.yml).

* To change properties of the components of the natural pipeline, edit the [conf_NaturalImageMarker.xml](./StandAlone/conf_NaturalImageMarker.xml) file.

### StandAlone/Multithread

* Open a terminal and execute :
    * `./bin/Release/SolARNaturalImageMarkerSampleStandAlone.exe`  
    (showing a mono thread demonstration based on a natural marker).

    * `./bin/Release/SolARNaturalImageMarkerSampleMultiThread.exe`  
    (showing a multithread demonstration based on a natural marker).

    * `./bin/Release/TestNaturalImageMarkerPlugin.exe`  
    (showing an application loading the natural image marker pipeline embedded into a dedicated SolAR Module).

*  When the application is started, point the camera to the natural image marker (you can see a virtual cube on the marker). 
* Press `escape` to quit the application.

### Plugin

You should have bundle every required library in your Unity project (`./Assets/Plugins`). Then from Unity Gameobject *PipelineLoader* you can load your configuration file for the natural image pipeline. You can directly edit parameters from Unity Editor's inspector.

## Contact 
Website https://solarframework.github.io/

Contact framework.solar@b-com.com




