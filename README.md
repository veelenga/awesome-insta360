# Awesome Insta360

A curated list of open source software, tools, and resources for Insta360 cameras.

Covers the GO series (GO, GO 2, GO 3, GO 3S, GO Ultra), X series (ONE X, X2, X3, X4, X5), ONE R/RS, Ace, and Pro/Titan. Insta360 Link webcams are intentionally out of scope.

## Contents

- [Camera control](#camera-control)
  - [WiFi and protocol](#wifi-and-protocol)
  - [Bluetooth remotes](#bluetooth-remotes)
  - [Live streaming](#live-streaming)
- [Media transfer and management](#media-transfer-and-management)
- [File format and metadata](#file-format-and-metadata)
  - [INSV tools](#insv-tools)
  - [GPS and telemetry export](#gps-and-telemetry-export)
  - [Viewers and integrations](#viewers-and-integrations)
- [Stabilization and telemetry overlays](#stabilization-and-telemetry-overlays)
- [Conversion and stitching](#conversion-and-stitching)
- [Official SDKs](#official-sdks)
  - [SDK wrappers](#sdk-wrappers)
- [Linux and macOS support](#linux-and-macos-support)
- [Firmware and reverse engineering](#firmware-and-reverse-engineering)
- [Robotics and research](#robotics-and-research)
- [Cloud](#cloud)
- [Contributing](#contributing)

## Camera control

### WiFi and protocol

- [insta360-wifi-api](https://github.com/RigacciOrg/insta360-wifi-api) - Python scripts to talk to Insta360 action cameras using the WiFi API.
- [insta360-go-ultra-sdk](https://github.com/Daiki-Iijima/insta360-go-ultra-sdk) - Unofficial Python toolkit for the GO Ultra: live stream and camera control over WiFi (TCP 6666, protobuf), with protocol docs.
- [insta360ctl](https://github.com/xaionaro-go/insta360ctl) - CLI written in Go to manage an Insta360 camera. Work in progress.
- [insta360](https://github.com/TomasHubelbauer/insta360) - Research notes on the ONE X protocol used by the mobile app.

### Bluetooth remotes

- [insta360_ble_esp32](https://github.com/pchwalek/insta360_ble_esp32) - Control Insta360 cameras via BLE using an ESP32.
- [insta360_m5StickC_remote](https://github.com/theserialhobbyist/insta360_m5StickC_remote) - Remote based on the M5StickC, M5StickC Plus, and Plus2.
- [ESP32-Insta360-Remote](https://github.com/rayje/ESP32-Insta360-Remote) - ESP32-based BLE remote.
- [Insta360-BLE-REMOTE](https://github.com/sagarmakhija1994/Insta360-BLE-REMOTE) - BLE remote implementation in C++.
- [Insta360-Remote-CIQ](https://github.com/arsfabula/Insta360-Remote-CIQ) - Garmin Connect IQ remote for Insta360 cameras.
- [WunderLINQ-Insta360-iOS](https://github.com/blackboxembedded/WunderLINQ-Insta360-iOS) - WunderLINQ motorcycle remote for iOS.
- [WunderLINQ-Insta360-Android](https://github.com/blackboxembedded/WunderLINQ-Insta360-Android) - WunderLINQ motorcycle remote for Android.
- [insta360-ble-gps-spec](https://github.com/TheAngryRaven/insta360-ble-gps-spec) - BLE protocol notes, confirmed working on an X4 with GPS.
- [CyberWand_Insta360](https://github.com/DLLSTART/CyberWand_Insta360) - Hardware remote wand.

### Live streaming

- [Insta360-Livestream](https://github.com/NiklasVoigt/Insta360-Livestream) - Get the camera livestream on a computer without a phone in between.
- [Insta360-X3-Streamer](https://github.com/hacknride/Insta360-X3-Streamer) - RTMP streaming from an X3.
- [insta360_rtsp_streamer](https://github.com/careyer/insta360_rtsp_streamer) - Transcode Insta360 Air video and serve it over RTSP.
- [insta360-gstreamer](https://github.com/ravijo/insta360-gstreamer) - GStreamer-based streaming tool for Insta360 cameras.

## Media transfer and management

- [insta360-go-ultra-transfer](https://github.com/veelenga/insta360-go-ultra-transfer) - Browse, preview, and copy media from the GO Ultra over WiFi.
- [insta360-go3s-mac-import](https://github.com/Cedric-Hsu/insta360-go3s-mac-import) - macOS app and CLI to wirelessly import GO 3S videos via Quick File Transfer.
- [mmt](https://github.com/KonradIT/mmt) - Media Management Tool for importing videos and photos from GoPro, Insta360, and other action cameras.
- [arkiv](https://github.com/vulture-s/arkiv) - Local-first media asset manager with AI semantic search that reads pro-camera metadata.
- [insta360-nas](https://github.com/iliakonnov/insta360-nas) - NAS integration for Insta360 media.
- [insta360-auto-converter](https://github.com/whmou/insta360-auto-converter) - Pick up insv/insp files from Google Drive, convert to 360 mp4/jpg, and upload to Google Photos.
- [Insta360CreateDates](https://github.com/smci1000/Insta360CreateDates) - Fix creation dates of files exported from Insta360 Studio.

## File format and metadata

### INSV tools

- [telemetry-parser](https://github.com/AdrianEddy/telemetry-parser) - Parse real-time metadata (gyro, accelerometer, GPS) embedded in video files, with an Insta360 module. Powers Gyroflow.
- [insvtools](https://github.com/alex-plekhanov/insvtools) - Java toolkit for working with Insta360 `.insv` files.
- [insvdump](https://github.com/ke4ukz/insvdump) - Dump metadata from INSV videos.
- [Insv-Marker-Extractor](https://github.com/arismelachroinos/Insv-Marker-Extractor) - Windows utility to extract timeline markers from `.insv` files.
- [Insta360-INSV-Repair](https://github.com/JimWas/Insta360-INSV-Repair) - Repair broken INSV files.
- [finsta360](https://github.com/kichiki/finsta360) - Finalize incomplete MP4 files from the ONE X.
- [insv-to-audio-transcribe](https://github.com/chessset5/insv-to-audio-transcribe) - Extract audio from an insv file and transcribe it.

### GPS and telemetry export

- [exiftool-insta360-gpx](https://github.com/miguel-coppiloto/exiftool-insta360-gpx) - Extract GPX tracks from Insta360 files with ExifTool.
- [insta360-gpx-extract](https://github.com/rabejens/insta360-gpx-extract) - GPX extraction tool written in F#.
- [Insta360-2-ODM](https://github.com/lectrician1/Insta360-2-ODM) - Convert a GPS-tracked video into a GPS-tagged image sequence for OpenDroneMap.
- [Insta360toBlackBoxCSV](https://github.com/nivim/Insta360toBlackBoxCSV) - Export Insta360 telemetry as Betaflight BlackBox CSV.
- [Insta360GyroExport](https://github.com/sweebee/Insta360GyroExport) - Export gyro data from Insta360 files.
- [insta360pro-gps](https://github.com/javiersanp/insta360pro-gps) - Convert GPS data extracted from an Insta360 Pro to GPX.
- [Vision360-Toolbox](https://github.com/GHSLAB/Vision360-Toolbox) - Desktop toolbox to convert `.insv` files and extract GPS data, built on the official SDK.

### Viewers and integrations

- [insta360-quicklook](https://github.com/faeton/insta360-quicklook) - Native macOS Quick Look extension for `.insv`, `.insp`, and `.lrv` files.
- [immich-insta360-viewer](https://github.com/inirin/immich-insta360-viewer) - Browser-based `.insv` viewer for Immich.
- [pano-album](https://github.com/robert-mcdermott/pano-album) - Create image gallery websites for 360 degree panoramic images.
- [Immuch360](https://github.com/freeKC/Immuch360) - App for Android, Android TV, Meta Quest and Windows that plays raw `.insv` and `.insp` files with the calibration stored in each file, with experimental gyroscope stabilisation on Android.

## Stabilization and telemetry overlays

- [gyroflow](https://github.com/gyroflow/gyroflow) - Video stabilization using gyroscope data, with native Insta360 support.
- [OVRLEY](https://github.com/spirokai/OVRLEY) - Telemetry overlay for sports, drone, and motorsport videos.
- [kart-telemetry-experiment](https://github.com/caezium/kart-telemetry-experiment) - Use a GO 3S as a combined IMU and video sensor for karting telemetry.

## Conversion and stitching

- [insta360-cli-utils](https://github.com/syncom/insta360-cli-utils) - Automate 360 video processing tasks without a GUI.
- [insta360-autostitcher](https://github.com/jagjordi/insta360-autostitcher) - Monitor a folder and automatically stitch Insta360 videos.
- [insv-to-yt](https://github.com/peterbraden/insv-to-yt) - Convert `.insv` videos to YouTube-ready mp4.
- [insv-stitch](https://github.com/BenjaminHenriksson/insv-stitch) - Linux stitching pipeline for raw X5 footage: fisheye dewarp, IMU stabilization, rolling shutter correction.
- [Insta-360-INSV-to-MP4-3D-Converter](https://github.com/bitopsy/Insta-360-INSV-to-MP4-3D-Converter) - INSV to MP4 converter as an alternative to Insta360 Studio on Linux.
- [Insta360Convert-GUI](https://github.com/stechdrive/Insta360Convert-GUI) - Extract perspective views (pitch, yaw, FOV) from equirectangular videos as MP4 clips.
- [insta360sdk](https://github.com/pdxmusic/insta360sdk) - Convert insv to equirectangular frames.
- [batchstitcher](https://github.com/MantisSub/batchstitcher) - Batch stitch Pro 2 recordings with shared settings.
- [360cams-PTGui-Templates](https://github.com/andreasbrett/360cams-PTGui-Templates) - PTGui templates for stitching `.insp` photos.
- [Insta360-One-2-Shotcut-filter](https://github.com/paahtola/Insta360-One-2-Shotcut-filter) - Shotcut filter for stitching ONE video files.
- [mapillary_360onex](https://github.com/SQ6NTI/mapillary_360onex) - Mapillary processing scripts for the ONE X.

## Official SDKs

- [Desktop-CameraSDK-Cpp](https://github.com/Insta360Develop/Desktop-CameraSDK-Cpp) - C++ library to control Insta360 cameras.
- [Desktop-MediaSDK-Cpp](https://github.com/Insta360Develop/Desktop-MediaSDK-Cpp) - C++ library for stitching and editing media from 360 cameras.
- [Android-SDK](https://github.com/Insta360Develop/Android-SDK) - Android SDK for camera control and media management.
- [iOS-SDK](https://github.com/Insta360Develop/iOS-SDK) - iOS SDK for camera control and media management.
- [Insta360_OSC](https://github.com/Insta360Develop/Insta360_OSC) - Open Spherical Camera API support for Insta360 360 cameras.
- [ProCameraApi](https://github.com/Insta360Develop/ProCameraApi) - Protocols to control the Pro, Pro 2, and Titan.

### SDK wrappers

- [Insta360CameraSDKPythonWrapper](https://github.com/gureckyfrantisek/Insta360CameraSDKPythonWrapper) - pybind11 wrapper for the Camera SDK.
- [insta360_sdk_python](https://github.com/ruu413/insta360_sdk_python) - Python bindings for the SDK.
- [insta360sdk](https://github.com/abraverm/insta360sdk) - Nix package for the Insta360 SDK.
- [insta360-mediasdk-server](https://github.com/Techt-Dev/insta360-mediasdk-server) - Docker-based MediaSDK server for converting `.insp` files to leveled panoramas.
- [Insta360_OSC-Utils](https://github.com/trundev/Insta360_OSC-Utils) - Python and HTML/JS utilities for the OSC API.

## Linux and macOS support

- [Insta360-Studio-Linux](https://github.com/NiklasVoigt/Insta360-Studio-Linux) - Run Insta360 Studio with Wine on Ubuntu and Arch.
- [insta360-linux](https://github.com/EdenCoder/insta360-linux) - Linux tooling for Insta360 cameras.
- [insta360_linux](https://github.com/caioquirino/insta360_linux) - Linux tooling for Insta360 cameras written in Rust.
- [insta360-one-rs-1-inch-360-edition-linux-info](https://github.com/frostworx/insta360-one-rs-1-inch-360-edition-linux-info) - Linux notes for the ONE RS 1-Inch 360 Edition.

## Firmware and reverse engineering

- [insta360-go-firmware-tool](https://github.com/enekochan/insta360-go-firmware-tool) - Unofficial firmware tool for the GO 2, GO 3, and GO 3S.
- [Insta360-X3-Firmware-Tools](https://github.com/nneonneo/Insta360-X3-Firmware-Tools) - Unpack and repack X3 firmware images.
- [OpenGO_360](https://github.com/Fire18Parrot/OpenGO_360) - Reverse engineering of the original GO (2019) software with a Python desktop app.

## Robotics and research

- [insta360_ros_driver](https://github.com/ai4ce/insta360_ros_driver) - ROS driver for real-time image capture and publishing.
- [insta360_ros2](https://github.com/hzlbbfrog/insta360_ros2) - ROS 2 driver for Insta360 cameras.
- [insta360_x5_ros2](https://github.com/asa-naki/insta360_x5_ros2) - ROS 2 driver for the X5.
- [insta360_camera_ros](https://github.com/RobotiXX/insta360_camera_ros) - ROS integration for Insta360 cameras.
- [insta360_air_ros](https://github.com/FengyuGuo/insta360_air_ros) - ROS wrapper for the Insta360 Air.
- [AnyCam2Ros](https://github.com/ly-geming/AnyCam2Ros) - Turn any camera, including Insta360, into ROS 2 image topics.
- [omni-sfm](https://github.com/Vincentqyw/omni-sfm) - Structure-from-Motion pipeline for omnidirectional imagery.
- [EasyGaussianSplatting](https://github.com/MapMindAI/EasyGaussianSplatting) - From Insta360 footage to Gaussian Splatting.
- [Insta360-BEVFormer](https://github.com/jeho-lee/Insta360-BEVFormer) - BEVFormer-based 3D object detection using a single Insta360 camera.
- [CurbScout](https://github.com/ParkWardRR/CurbScout) - Local-first pipeline that ingests daily GO 3S bike footage and extracts car sightings.
- [ambisonics-for-insta360-pro](https://github.com/AppliedAcousticsChalmers/ambisonics-for-insta360-pro) - Experimental 4th-order ambisonic microphone array for the Pro.

## Cloud

- [insta360-cloud-mcp](https://github.com/alfari16/insta360-cloud-mcp) - MCP server to access Insta360 cloud assets from LLMs.
- [Insta360-Community](https://github.com/AlecAnthonyGarcia/Insta360-Community) - Unofficial web app for the Insta360 community.

## Contributing

Contributions welcome. Open a pull request with a link, a one-line description, and keep the entry in the matching section.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
