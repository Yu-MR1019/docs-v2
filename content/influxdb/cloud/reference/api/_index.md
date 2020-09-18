---
title: InfluxDB v2 API
description: >
  The InfluxDB v2 API provides a programmatic interface for interactions with InfluxDB.
  Access the InfluxDB API using the `/api/v2/` endpoint.
menu: influxdb_cloud_ref
weight: 3
influxdb/cloud/tags: [api]
---

The InfluxDB v2 API provides a programmatic interface for interactions with InfluxDB.
Access the InfluxDB API using the `/api/v2/` endpoint.

## Authentication
InfluxDB uses [authentication tokens](/influxdb/cloud/security/tokens/) to authorize API requests.
Include your authentication token as an `Authorization` header in each request.

```sh
curl --request POST \
  --url https://cloud2.influxdata.com/api/v2/write?org=my-org&bucket=example-bucket \
  --header 'Authorization: Token YOURAUTHTOKEN'
```

## View InfluxDB v2 API Documentation
<a class="btn" href="/v2.0/api/">InfluxDB v2.0 API documentation</a>

## InfluxDB client libraries
InfluxDB client libraries are language-specific packages that integrate with the InfluxDB v2 API.
For information about supported client libraries, see [InfluxDB client libraries](/influxdb/cloud/tools/client-libraries/).