# What is Solarzon?

The Solarzon is motorized shade controller connected to Internet
- Remote controlled by smartphone
- Multiple devices can be grouped and settings easy
- 7-day Schedule
- No limit on the motor that can be controlled simultaneously
- Smart shading by tracks the location of the sun in real time

For more details see [Solarzon Brochure](http://resource.one-scape.com/solarzon-en.pdf).

# API

The Solarzon API is an interface for querying information from and enacting change in a Solarzon device.

[NOTICE] You'll need to obtain the access token with [OAuth Document](https://onescape.github.io/oauth) 

## YAML

You can use the YAML at [https://swaggerhub.com/apis/onescape/solarzon](https://swaggerhub.com/apis/onescape/solarzon)

## Supported

| Supported actions | Supported events | Supported conditions |
| --- | --- | --- |
| - Up<br/>- Down<br/>- Stop<br/>- Tilt Up<br/>- Tilt Down | N/A | N/A |

## Functions

- Get information for all devices and groups owned by the user
- Get information for all devices owned by the user
- Get information for all groups owned by the user
- Set control state of device
- Set control state of group

## Model

### Device/Group control state

| Type | Enum |
| --- | --- |
| string | - Up<br/>- Down<br/>- Stop<br/>- Tilt Up<br/>- Tilt Down |

### View type

| Type | Enum |
| --- | --- |
| number | - 1<br/>- 2<br/>- 3<br/>- 4 |

| Enum | Display Name | Action | Preview |
| --- | --- | --- | --- |
| 1 | Roll blind | up/down/stop | ![alt text](https://github.com/onescape/solarzon/blob/master/viewtype1.png?raw=true) |
| 2 | Shutter blind | up/down/stop/tiltUp/tiltDown | ![alt text](https://github.com/onescape/solarzon/blob/master/viewtype2.png?raw=true) |
| 3 | Awning | up/down/stop | ![alt text](https://github.com/onescape/solarzon/blob/master/viewtype3.png?raw=true) |
| 4 | Curtain | up/down/stop | ![alt text](https://github.com/onescape/solarzon/blob/master/viewtype4.png?raw=true) |

## How-to

### Step 1 - Obtain the access tokens

You'll need to obtain the access token with [OAuth Document](https://onescape.github.io/oauth) 

### Step 2 - Using access tokens

The tokens awarded to your app can be used in requests to the API.

```markdown
https://api.onescape.io/solarzon
```

The best way to communicate your access tokens, also known as bearer tokens, is by presenting them in a request's Authorization HTTP header:

```markdown
GET /RESOURCE_NAME
Authorization: Bearer ACCESS_TOKEN
```

This approach is required when using application/json with a write method.

![alt text](https://github.com/onescape/oauth/blob/master/swaggerhub.jpeg?raw=true)

![alt text](https://github.com/onescape/oauth/blob/master/postman.jpeg?raw=true)
