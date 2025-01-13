# Cesium in VR with Local Data

This repository contains a Unity VR project demonstrating how to visualize a locally hosted GeoTIFF on a Cesium globe within a VR environment. The local GeoTIFF is provided via a GeoServer instance and served through a Web Map Service (WMS). The example highlights best practices for integrating custom geospatial data into VR applications using Cesium for Unity. The GeoServer instance is not part of this repository.

## Overview

- **Local Data Visualization**: Displays a global GeoTIFF (“Natural Earth I with Shaded Relief”) served by GeoServer in Unity’s VR environment. (Must be set up seperately)
- **Cesium for Unity**: Leverages Cesium’s capabilities to handle and render geospatial data on a 3D globe.  
- **VR Interaction**: Uses Unity’s VR Template, OpenXR framework, and the XR Interaction Toolkit for interactive features such as rotating the globe in VR.  

## Features

- **Cesium Globe**: A fully navigable and interactable 3D globe in Unity.  
- **Local WMS Integration**: Connects to a WMS endpoint (GeoServer) at `http://localhost:8080/geoserver/geovisdemo/wms` to load the `NE1_50M_SR_W` layer.  
- **Real-Time VR Interaction**: Spin, zoom, and explore the globe using VR controllers.  
- **Minimal Scene Setup**: Focuses on geovisualization by removing extraneous interaction elements.

## Getting Started

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/cesium-in-vr-with-local-data.git
   ```
   Open the project in Unity (using the Unity version compatible with the VR Template).

2. **Set Up GeoServer**  
   - Install and run [GeoServer](https://geoserver.org/) (or similar WMS).  
   - Publish or configure the “Natural Earth I with Shaded Relief” (or your own) GeoTIFF.  
   - Ensure it is accessible via WMS at `http://localhost:8080/geoserver/geovisdemo/wms` (Layer name `NE1_50M_SR_W`).

## Usage

- **Interact with the Globe**: Use your VR controllers to point at and grab the globe. The XRKnob Interactable will let you rotate it.  
- **Explore Terrain**: If you have Cesium World Terrain configured, move around to see how terrain data integrates with your custom imagery.  

## Acknowledgments

- **Cesium** for the powerful 3D geospatial engine and integration.  
- **Natural Earth** project for the “Natural Earth I with Shaded Relief” dataset.  
- **GeoServer** for providing an open-source WMS solution.  
