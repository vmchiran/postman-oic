# OIC Start/Stop
The following guide applies to OIC Gen-1.

## Manually
Using the Console


## Using PSM CLI
```
psm OICINST start-service -s ExampleInstance
psm OICINST stop-service -s ExampleInstance
```


## Using REST APIs

Oracle Support Document 2588158.1 (REST API's for managing OIC instance): https://support.oracle.com/epmos/faces/DocumentDisplay?id=2588158.1

Example:
```
curl -X POST -u 'myuser':'mypassword' -H 'X-ID-TENANT-NAME: idcs-a566XXXXXXXXeca' 'https://psm.europe.oraclecloud.com:443/paas/api/v1.1/instancemgmt/idcs-a566XXXXXXXXeca/services/OICINST/instances/ExampleInstance/start'

curl -X GET -u 'myuser':'mypassword' -H 'X-ID-TENANT-NAME: idcs-a566XXXXXXXXeca' 'https://psm.europe.oraclecloud.com:443/paas/api/v1.1/activitylog/idcs-a566XXXXXXXXeca/job/184284931'
```

Requests are included in the [Postman collection](../blob/master/REST%20API%20for%20OIC%20-%20CSM%20Workshop.postman_collection.json)