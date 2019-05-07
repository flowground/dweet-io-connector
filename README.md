# ![LOGO](logo.png) dweet.io **flow**ground Connector

## Description

A generated **flow**ground connector for the dweet.io API (version 2.0).

Generated from: https://api.apis.guru/v2/specs/dweet.io/2.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:18+03:00

## API Description

Dweet.io allows users to share data from mobile, tablets, and pcs, and them to other devices and accounts across social media platforms. Dweet.io provides an API to access the different functionality of the Dweet.io service. Users can make REST calls to read and create dweets, lock and unlock things, and perform other calls. The API returns JSON and JSONP.

## Authorization

This API does not require authorization.

## Actions

### Create an alert for a thing. A thing must be locked before an alert can be set.

*Tags:* `alerts`

#### Input Parameters
* `who` - _required_ - A comma separated list of Email addresses to send the alert to.
* `thing` - _required_ - A unique name of a thing. It is recommended that you use a GUID as to avoid name collisions.
* `condition` - _required_ - A condition that returns a string or a true value if a condition is met.
* `key` - _required_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Create a dweet for a thing.

*Tags:* `dweets`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing. It is recommended that you use a GUID as to avoid name collisions.
* `key` - _optional_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Create a dweet for a thing.  This method differs from /dweet/for/{thing} only in that successful dweets result in an HTTP 204 response rather than the typical verbose response.

*Tags:* `dweets`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing. It is recommended that you use a GUID as to avoid name collisions.
* `key` - _optional_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Get the alert attached to a thing.

*Tags:* `alerts`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _required_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Read the last 5 cached dweets for a thing.

*Tags:* `dweets`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _optional_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Read the latest dweet for a thing.

*Tags:* `dweets`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _optional_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Read all the saved alerts for a thing from long term storage.  You can query a maximum of 1 day per request and a granularly of 1 hour.

*Tags:* `storage`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _required_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.
* `date` - _required_ - The calendar date (YYYY-MM-DD) from which you'd like to start your query.  The response will be a maximum of one day.
* `hour` - _optional_ - The hour of the day represented in the date parameter in 24-hour (00-23) format.  If this parameter is included, a maximum of 1 hour will be returned starting at this hour.
* `responseType` - _optional_ - Current valid parameters for this are 'csv' and 'json'.  If this parameter is left blank, all responses default to hapi-json dweet-speak.

### Read all the saved dweets for a thing from long term storage.  You can query a maximum of 1 day per request and a granularly of 1 hour.

*Tags:* `storage`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _required_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.
* `date` - _required_ - The calendar date (YYYY-MM-DD) from which you'd like to start your query.  The response will be a maximum of one day.
* `hour` - _optional_ - The hour of the day represented in the date parameter in 24-hour (00-23) format.  If this parameter is included, a maximum of 1 hour will be returned starting at this hour.
* `responseType` - _optional_ - Current valid parameters for this are 'csv' and 'json'.  If this parameter is left blank, all responses default to hapi-json dweet-speak.

### Listen for dweets from a thing.

> Sorry, this function uses HTTP chunked responses and cannot be tested here. Try something like: <pre>curl --raw https://dweet.io/listen/for/dweets/from/{thing}</pre>

*Tags:* `dweets`

#### Input Parameters
* `thing` - _required_

### Reserve and lock a thing.

*Tags:* `locks`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `lock` - _required_ - A valid dweet.io lock.
* `key` - _required_ - A valid dweet.io master key.

### Remove an alert for a thing.

*Tags:* `alerts`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _required_ - A valid key for a locked thing. If the thing is not locked, this can be ignored.

### Remove a lock from thing.

*Tags:* `locks`

#### Input Parameters
* `lock` - _required_ - A valid dweet.io lock.
* `key` - _required_ - A valid dweet.io master key.

### Unlock a thing.

*Tags:* `locks`

#### Input Parameters
* `thing` - _required_ - A unique name of a thing.
* `key` - _required_ - A valid dweet.io master key.

## License

**flow**ground :- Telekom iPaaS / dweet-io-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
