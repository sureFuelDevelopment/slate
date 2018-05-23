---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - Shell

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
includes:
  - errors

search: true
---

# Welcome to SureFuel!

Welcome to the SureFuel Javascript API!

SureFuel features a small and dynamic development team, aimed at quick, iterative deployments.

##Request

All server requests require an Authorization Bearer Token.

Parameter |  Description
--------- | -----------
Authorization Bearer Token |  firebase_user_token


# Scheduling API

The SureFuel scheduling API is responsible for setting up automated routing calls. In general, we require information on the asset we are looking to fill, alongside the scheduled interval.

##New Schedule Item



> Example Request:

```shell
curl --request POST \
  --url http://localhost:3000/scheduler/newitem \
  --header 'Content-Type: application/json' \
  --data '{
"asset_id": "7R4977M2Vb3mK73HFwXr",
"owner_uid": "7R4977M2Vb3mK73HFwXr",
"asset_name": "example_item",
"asset location": {
"lat": -34.397,
"lng": 150.644
},
"asset_capacity": "500",
"fill_frequency": "weekly",
"starting_date": 1527032210
}'
```


Add a scheduled item to the database.

Parameter |  Description
--------- | -----------
asset_uid |  Asset Unique UID
owner_uid |  UID of the owner
asset_location |  Location of the Asset
asset_capacity |  Capacity of the Asset in Liters
fill_frequency | Type Of: `weekly`, `daily`, `monthly`
starting_date |  Start date of Recurrence in Unix Timestamp




<aside class="notice">
<code>All Parameters are required for successful call </code>
</aside>

##Get Scheduled Items

> Example Request:

```shell
curl --request GET \
  --url http://localhost:3000/scheduler/getitems \
  --header 'Content-Type: application/json'
```

Get a list of the currently scheduled items from the DB.








##Delete Scheduled Item

> Example Request:

```shell
curl --request GET \
  --url 'http://localhost:3000/scheduler/deleteitem?asset_uid=7R4977M2Vb3mK73HFwXr' \
  --header 'Content-Type: application/json'
```

Delete a scheduled item from the DB based on "asset_uid"

Query Parameter |  Description
--------- | -----------
asset_uid |  Asset Unique UID

<aside class="notice">
<code>All Parameters are required for successful call </code>
</aside>



# Routing API

##Add location to Routing Queue
Add a location to the current `Daily` Routing Queue.

##Get Routing Queue
See the current `Daily` routing queue as existing.

##Optimize Routes
<aside class="warning">Get updated Routes does not send routes to drivers and is used for querying only.</aside>

##Deploy Optimized Routes
Deploy updated routes to drivers.

##Deploy Optimized Route to Driver
Deploy updated routes to specific driver.

# Inventory API

##Update Driver Inventory.

##Reset Driver Inventory

##Reset All Drivers Inventory

##Get Driver Inventory
Get inventory for specific driver.

##Get All Inventories
Get inventories for all drivers.



