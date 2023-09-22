# homebridge-http-fan
Homebridge Plugin to control a Fan. This is a fork of homebridge-http-fancontrol with added readme/example and changed manufacturer data.
### Example config:
```
{
  "accessory": "HTTP-FAN",
  "name": "Bathroom fan",
  "active": {
      "onUrl": "http://192.168.0.23?on",
      "offUrl": "http://192.168.0.23?off",
      "statusUrl": "http://192.168.0.23?status"
  }
}
```

### Expected response
On and off urls have to respond with code 200, the statusurl has to have code 200 and either a 1 or a 0 in "text/html" (1 is on, 0 is off).
