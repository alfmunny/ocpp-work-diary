---
layout: post
title:  
date: 2014-08-05 14:44:45
disqus: y
---

# Model Schema

## User Model

```
user:
  id: string
  firstName: string
  lastName: string
  verified: boolean
  expiryDate: date
  email: string
  company: string
  avatar: string
  vehicles: hasMany('vehicle')
  chargePoints: hasMany('chargePoint')
  transactions: hasMany('transaction')
```

## Charge Point Model

```
chargePoint:
  id: string
  idTag: string
  status: string
  location: string
  chargePointVendor: string
  chargePointModel: string
  chargePointSerialNumber: string
  chargeBoxSerialNumber: string
  firmwareVersion: string,
  iccid: string,
  imsi: string,
  meterType: string,
  meterSerialNumber: string
  users: hasMany('user')
  vehicles: hasMany('vehicle')
  heartbeatInterval: number(in seconds)
  transactions: hasMany('transaction')

```

## Connector Model

```
connector:
  id: string
  connectorId: string
  chargePoint: belongsTo('chargePoint')
```

## Vehicle Model

```
vehicle:
  id: string
  type:string
  name: string
  picture: string
  users: hasMany('user')
  transactions: hasMany('transaction')
```

## Tanscation Model

```
transaction:
  id: string
  transactionId: string
  status: string
  begin: date
  end: date
  energy: number
  bill: number
  user: belongsTo('user')
  chargePoint: belongsTo('chargePoint')
  vehicle: belongsTo('vehicle')
  records: hasMany('record')
```

## Record Model

```
record:
  id: string
  timestamp: data
  power: number
  current: number
  voltage: number

```
