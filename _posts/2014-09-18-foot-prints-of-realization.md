---
layout: post
title: Foot Prints of Realization
date: 2014-09-18 17:56:00
disqus: y
---

# Charge Point Server

There are 10 actions, which will be initialized by Charge Point and sent to server. For every action is a REST-API on server available. 

## BootNotification:

#### API: available

#### Function: available
	
#### Verified Parameters:

Considering the convenience during development is only now one of them are verified:
	
1. ~~Charge Point Vendor~~
2. Charge Point Model
3. Firmware Version
4. Charge Point Serial Number
5. ICCID
6. IMSI
7. Meter Type
8. Meter Serial Number
9. Heartbeat Interval
10. Charge Box Serial Number

## Authorize:

#### API: available
#### Request: GET
#### Function: to be fulfilled

## HeartBeat

#### API: available
#### Request: GET
#### Function: available

## StartTransaction:

#### API: available
#### Request: PUT
#### Function: available
#### Verified Parameters:

1. id_tag: using id_tag to verified the user and it's expiry date


## StopTransaction:

#### API: available
#### Request: PUT
#### Function: available

#### Verified Parameters:

Mandatory Parameters:

1. ~~meterStop~~
2. ~~timestamp~~
3. ~~transactionId~~

Optional Parameters:

1. idTag
2. transactionData


## MeterValues

#### API: available
#### Request: PUT
#### Function: available

#### Verified Parameters:

Mandatory Parameters:

1. ~~connectorId~~
2. ~~transactionId~~
3. ~~values~~
	1. ~~power~~
	2. ~~current~~

Optional Parameters:






## FirmwareStatusNotification

## DiagnosticsStatusNotification

## DataTransfer

## StatusNotification






# Charge Point