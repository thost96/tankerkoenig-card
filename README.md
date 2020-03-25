# Tankerkoenig Lovelace Card for ioBroker


## Installation
1. Install this component by copying the `tankerkoenig-card.js` to your Lovelace adapter Custom Cards tab.
2. Reload the Lovelace adapter.
3. Also upload the icons as `*.png` for the brands using the Custom Cards upload tab.

```yaml
cards:
   - type: 'custom:tankerkoenig-card'
     name: Benzinpreise
     show_header: true
     show:
       - e5
       - e10
     stations:
       - name: Kölner Str.
         brand: ARAL
         e5: sensor.aral_kolner_str_e5
         e10: sensor.aral_kolner_str_e10
       - name: Untergath
         brand: ARAL
         e5: sensor.aral_untergath_e5
         e10: sensor.aral_untergath_e10
```

### Options
| key          | values            | required | description
|--------------|-------------------|----------|---
| `name`       | String            | yes      | Name of the card that should be shown in the frontend
| `show`       | [e5, e10, diesel] | yes      | What should be shown
| `show_header`| true or false     | yes      | Show header name or remove it
| `stations`   | List of stations  | yes      | List of stations

#### Stations
| key      | value  | required | description
|----------|--------|----------|---
| `name`   | String | yes      | The name of the station (for example the street)
| `brand`  | String | yes      | The brand of the station used for the icon
| `e5`     | Sensor | no*      | Sensor for the E5 price
| `e10`    | Sensor | no*      | Sensor for the E10 price
| `diesel` | Sensor | no*      | Sensor for the diesel price

*only required if it should be shown

## Icons
The icons must be in `*.png` format and the filename must be all lowercase. The Icons can be uploaded using the lovelace adapter custom cards tab. A reload is needed after the upload. 

