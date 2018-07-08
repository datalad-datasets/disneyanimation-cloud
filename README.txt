Walt Disney Animation Studios Cloud Data Set


PACKAGE CONTENTS:

wdas_cloud.vdb : a heterogeneous volumetric cloud model containing density data
wdas_cloud_*.vdb : lower-resolution versions at half, quarter, eighth, and sixteenth resolution
wdas_cloud_hyperion_render.[exr|png] : an image of the volumetric cloud rendered in Disney's Hyperion renderer
wdas_cloud_mitsuba_scene.xml : an example Mitsuba scene for rendering the volumetric cloud
wdas_cloud_mitsuba_scene.[exr|png] : the rendered image produced using the Mitsuba scene


INSTRUCTIONS FOR MITSUBA:

To render the included example Mitsuba scene, compile Mitsuba with the following modification. In src/integrators/path/volpath_simple.cpp, line 288 (as of this writing), change the maximum value of the Russian-roulette survival probability from 0.95f to 1.0f to avoid overly aggressive termination of paths that results in high variance and fireflies. The scene requires the "mitsuba-vdb" plugin to load the data set. Mitsuba does not implement the algorithms and acceleration structures necessary to render high-albedo heterogeneous volumes efficienty; the included scene is intended as a reference.


LICENSING:

The contents of this package are Copyright 2017 Disney Enterprises, Inc. and are licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License. A copy of this license is available at http://creativecommons.org/licenses/by-sa/3.0/. The volumetric cloud model used for reference is a photograph by Kevin Udy provided on the Colorado Clouds Blog at https://coclouds.com/436/cumulus/2012-07-26/ and licensed under the Creative Commons Attribution-ShareAlike 3.0 Unported License.
