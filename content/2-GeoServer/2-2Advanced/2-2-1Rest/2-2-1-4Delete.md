---
title: "Delete"
date: 2021-01-26T15:51:05+01:00
draft: true
---

Remove a resource
You should have noticed that the layer countries is available twice now. The first one was created "manually" by the use of the GeoServer UI, the second one via the REST API. Because we don't want to unnecessarily publish a layer twice (and of course to learn how to delete a resource by means of REST), we will delete the countries_rest layer by using the HTTP operation DELETE.

Execute the following command to delete the feature type countries_rest and the corresponding layer by appending recurse=true to the request:
  $ curl \
    -v \
    -u admin:momo-ws \
    -XDELETE \
    http://localhost/geoserver/rest/workspaces/momo-rest/datastores/db_momo_ws_rest/featuretypes/countries_rest?recurse=true
After the above command has successfully executed with HTTP/1.1 200 OK try to find the layer in the GeoServer Layer configuration page and if anything worked fine, you shouldn't be able to find it :wink: