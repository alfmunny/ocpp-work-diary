---
layout: post
title: Incharge Model Schema
date: 2014-08-05 14:44:45
disqus: y
---

# Model Schema

## User Model

```
user:
  √ id: string
  √ name: string
  id_tag
  verified: boolean
  √ expiry_date: date
  √ email: string
  √ company: string
  avatar: string
  √vehicles: hasMany('vehicle')
  √chargePoints: hasMany('chargePoint')
  √transactions: hasMany('transaction')
```

## Charge Point Model

```
chargePoint:
  √id: string
  idTag: string
  √status: string|Accepted, Rejected
  location: string
  √chargePointVendor: string
  √chargePointModel: string
  √chargePointSerialNumber: string
  √chargeBoxSerialNumber: string
  √firmwareVersion: string,
  √iccid: string,
  √imsi: string,
  √meterType: string,
  √meterSerialNumber: string
  √heartbeatInterval: number(in seconds)
  
  √users: hasMany('user')
  √vehicles: hasMany('vehicle')
  √transactions: hasMany('transaction')

```

## Connector Model

```
connector:
  √id: string
  connectorId: string
  √name: string
  √chargePoint: belongsTo('chargePoint')
  √trades: hasMany('trade')
```

## Vehicle Model

```
vehicle:
  √ id: string
  √ type:string
  √ name: string
  picture: string
  √users: hasMany('user')
  √transactions: hasMany('transaction')
  √chargePoints: hasMany('chargePoint')
```

## Transcation Model

```
transaction:
  √id: string
  √transactionId: string
  √status: string
  √energy: number
  √bill: number
  begin: date
  end: date
  √user: belongs_to('user')
  √chargePoint: belongs_to('chargePoint')
  √vehicle: belongs_to('vehicle')
  √records: hasMany('record')
```

## Record Model

```
record:
  √id: string
  √power: number
  √current: number
  √voltage: number
```

## Reservation

```
reservation:
  id: integer
  belongsTo('user')
  belongsTo('vehicle')
  belongsTo('chargePoint')
  belongsTo('connector')
  begin_time: date
  end_time: date
```
