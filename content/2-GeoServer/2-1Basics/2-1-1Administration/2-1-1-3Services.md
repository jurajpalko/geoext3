---
title: "Services"
date: 2021-01-26T15:42:10+01:00
draft: true
---

Services
The Services section is for configuring the services published by GeoServer, where we can manage:

The metadata, resource limits, and SRS availability for WCS.
The metadata, feature publishing, service level options, and data-specific output for WFS.
The metadata, resource limits, SRS availability, and other data-specific output for WMS.
The following exercises will give you a brief introduction in the most important administration options available here.

For further instructions please have a look at the official GeoServer documentation.

Limit SRS output list
The default GetCapabilities document contains a comprehensive list of all available spatial reference systems (SRS) of your GeoServer WMS server instance. Generally it is not needed, that you list all supported systems as you typically want to publish data in an limited list of projections only. Furthermore limiting this list will reduce the file size of the responding GetCapabilites document!

Exercise
Open the following URL in your browser to open the GetCapabilites document of your GeoServer instance: GetCapabilities
In the resulting XML document find the element Layer which contains the large list (~6000 lines) of all supported EPSG projections.
In the next step we'll limit this list to contain the systems EPSG:4326, EPSG:3857 and EPSG:900913 only.

Navigate to Services ❭ WMS.
Find the description field entitled with Limited SRS list and fill in 4326, 3857, 900913.


Click Submit.
Reopen the GetCapabilites document and you will note, that the document is reduced by a huge amount of lines.
Disable WFS-T
GeoServer is configured to act as a fully transactional Web Feature Service server per default. A transactional WFS allows creation, deletion, and updating of features. This implies, that each published feature type can be edited by any client. Generally you don't want to allow clients to edit your data published with GeoServer (unless you really want to allow it), especially if your GeoServer is accessible globally through the Internet. In the next iteration we're going to disable the WFS-T functionality.

Exercise
Navigate to Services ❭ WFS.
Find the checkbox group entitled with Service Level and select the level Basic to disable WFS-T compatibility.


Click Submit.
Optional: Import a given WMS layer into QGIS and try to edit it.