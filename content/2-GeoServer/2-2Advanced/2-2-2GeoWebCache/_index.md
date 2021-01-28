---
title: "GeoWebCache"
date: 2021-01-26T15:54:09+01:00
draft: true
geekdocCollapseSection: true
---

GeoWebCache
The most common request to GeoServer is to provide an OGC-compliant WMS interface and thus generating maps in raster format. For this reason, caching of these WMS requests may have a decisive influence to the performance of the server and should be carried out on each (productive) system wherever possible. For caching map tiles there is a variety of good open source caching engines available, but here we'll use the GeoServer integrated GeoWebCache (GWC), which acts as a proxy between the client and GeoServer.

GeoWebCache as proxy, source: http://geowebcache.org/docs/current/_images/how_it_works.png
GeoWebCache as proxy, source: http://geowebcache.org/docs/current/_images/how_it_works.png
In the following sections we'll initiate all required steps to generate a cache for the layer momo:countries:

Prerequisites
Configure a new gridset
Configure a cached layer
Generate map tiles.
Check cache directory
Check cache-headers