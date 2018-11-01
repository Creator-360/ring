# homebridge-ring-alarm
This [Homebridge](https://github.com/nfarina/homebridge) plugin provides a platform for the
 [Ring Alarm System](https://shop.ring.com/pages/security-system)
 
 ### Homebridge Configuration
 
 Add the `RingAlarm` platform in your homebridge `config.json` file.  The platform options are passed directly into 
 [ring-api](https://github.com/jimhigson/ring-api) (with `poll` set to `false` since it's not needed
 for alarms)
 
 ```json
{
  "bridge": {
    ...
  },
  "platforms": [
    {
      "platform": "RingAlarm",
      "email": "some.one@website.com",
      "password": "abc123!#"
    }
  ]
}
```

### Supported Devices
  * Security Panel
    * This is a software device that represents the alarm for a Ring location
    * Arm Home / Arm Away / Disarm alarm for Ring location.
  * Base Station
    * Set Volume (Not currently supported in Home, but works in other apps like Eve)
    * Battery status
  * Keypad
    * Set Volume (Not currently supported in Home, but works in other apps like Eve)
    * Battery status
  * Contact Sensor
    * Detect if sensor is open or closed
    * Tamper status
    * Battery status
  * Motion Sensor
    * Detect motion
    * Tamper status
    * Battery status