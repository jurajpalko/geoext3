---
title: "Setup"
date: 2021-01-25T17:03:31+01:00
draft: true
---

Workshop Linux Mint Setup
The provided workshop Linux image is just a Linux Mint with pre-installed and configured programs and tools. This page lists the changes to the default system configuration only and is no integral part of the workshop.

Operating system:
Linux Mint 17.3 Cinnamon Edition (32bit)
Additionally installed software:
Apache 2
Installed from package manager
Linked home directory /home/momo to http://localhost:80/momo
Added to autostart
Apache Tomcat 8
Installed from here
Added to autostart
GeoServer 2.8.2
Installed from here
Installed plugins:
pyramid-plugin
wps-plugin
oracle-plugin
importer-plugin
Published via Apache 2 on port 80
http://localhost:80/geoserver
Atom Editor
Installed from here
Chrome
Installed from here
PostgreSQL / PostGIS
Installed from package manager
Added to autostart
git
Installed from package manager
nvm
Installed from here
bash-git-prompt
Installed from here
QGIS
Installed from here
GDAL
Installed from package manager
Removed packages:
  $ sudo apt-get remove thunderbird vlc vlc-plugin-notify vlc-plugin-pulse \
    vlc-data vlc-nox totem-common brasero banshee gimp hexchat pidgin totem \
    seahorse cowsay mint-backgrounds-qiana mint-backgrounds-rafaela \
    mint-backgrounds-rebecca mint-backgrounds-rosa sox ttf-indic-fonts-core \
    ttf-punjabi-fonts ttf-wqy-microhei fonts-kacst fonts-kacst-one \
    fonts-khmeros-core fonts-lao fonts-lklug-sinhala fonts-thai-tlwg \
    fonts-tibetan-machine fonts-tlwg-garuda fonts-tlwg-kinnari fonts-tlwg-loma \
    fonts-tlwg-norasi fonts-tlwg-purisa fonts-tlwg-sawasdee fonts-wqy-microhe \
    fonts-noto fonts-sil-abyssinica fonts-sil-padauk fonts-takao-pgothic \
    fonts-tlwg-umpush fonts-tlwg-waree gimp-help-en firefox firefox-locale-en \
    simple-scan transmission-common transmission-gtk mintwelcome
Removed remaining dependencies no longer needed
  $ sudo apt-get autoremove
Updated and upgraded packges to latest version
  $ sudo apt-get -y update && sudo apt-get -y upgrade
In case you didn't receive a bootable USB with the above system, you can grab an image under the following URL: http://files.terrestris.de/momo-master.tar.gz This file is roughly 2.2 GB big, and once it is decompressed it will have a size of 16GB.
Data used in the workshop:
Natural Earth Large scale data, 1:10m
Cultural
Download here
Physical
Download here
Raster (Ocean bottom)
Download here
Extracted to ~/materials/natural_earth
OSM sample export Mongolia
Download here
Extracted to ~/materials/osm_mongolia
