---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - Javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
includes:
  - errors

search: true
---

# Introduction

Welcome to the SureFuel Javascript API!

SureFuel features a small and dynamic development team, aimed at quick, iterative deployments. As a SureFuel developer and to make the best use of these documents, you will need to be familiar with:

-   NodeJS
-   Firebase API
-   Firebase Cloud Functions

##Request

> Example request:

```javascript

```

Server accepts requests with the next required parameters:

Parameter |  Description
--------- | -----------
Authorization |  firebase_user_token


# Scheduling API

The SureFuel scheduling API is responsible for setting up automated routing calls. In general, we require information on the asset we are looking to fill, alongside the scheduled interval.

##New Schedule Item

> To authorize, use this code:

```javascript
const kittn = require('kittn');

```

Create a scheduled item.

<aside class="notice">
<code>meowmeowmeow</code>
</aside>

##Get Scheduled Items
Get a list of the currently scheduled items from the DB.

##Delete Scheduled Item
Delete a scheduled item from the DB based on `uid`.

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



