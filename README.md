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

## YAML

You can use the YAML at [https://swaggerhub.com/apis/onescape/solarzon](https://swaggerhub.com/apis/onescape/solarzon)

## Supported

| Supported actions | Supported events | Supported conditions |
| --- | --- | --- |
| - Set device's control state to {up, stop, down, tiltUp, tiltDown, retract, extract, open, close}<br/>- Set group's control state to {up, stop, down, tiltUp, tiltDown, retract, extract, open, close} | N/A | N/A |

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
| string | {up, stop, down, tiltUp, tiltDown, retract, extract, open, close} |

### Controller view type

| Type | Enum |
| --- | --- |
| string | {roll, shutter, awning, curtain} |

Definition

| Value | Action | Preview |
| --- | --- | --- |
| roll | {up, stop, down} | ![alt text](roll.png?raw=true | width=320) |
| shutter | {up, stop, down, tiltUp, tiltDown} | ![alt text](shutter.png?raw=true | width=320) |
| awning | {retract, stop, extract} | ![alt text](awning.png?raw=true | width=320) |
| curtain | {open, stop, close} | ![alt text](curtain.png?raw=true | width=320) |

## How-to : OAuth2

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

### Sample screenshot

![alt text](https://github.com/onescape/oauth/blob/master/swaggerhub.jpeg?raw=true)

![alt text](https://github.com/onescape/oauth/blob/master/postman.jpeg?raw=true)

## How-to : API key

The API key awarded to your app can be used in requests to the API.

```markdown
https://api.onescape.io/solarzon
```

The best way to communicate your API key, is by presenting them in a request's X-API-Key HTTP header:

```markdown
GET /RESOURCE_NAME
X-API-Key: API_KEY
```

This approach is required when using application/json with a write method.

### Sample screenshot

![alt text](swaggerhub.jpeg?raw=true)

![alt text](postman.jpeg?raw=true)
