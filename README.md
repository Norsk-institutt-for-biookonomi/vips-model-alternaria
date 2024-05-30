# AlternariaModel (TOMCAST)

<img src="src/main/resources/images/ef-20200421-altenaria.jpg" description="Photo: S. Abrahamsen, NLR"/>

_Photo: S. Abrahamsen, NLR_

TOMCAST is based on a model that was originally developed for leaf spot diseases in tomato. The model that is used here is tested and adapted to be used against early blight in potato in Denmark (Alternaria solani). The model calculates daily risk values (DSV: Disease Severity Values) based on temperature and leaf wetness the previous day. DSV represents the risk of attack of early blight the previous 24 hours. Daily values of DSV are accumulated until a threshold value is reached, and treatment is recommended. When a spray is performed and entered into the model, accumulation of DSV is reset and starts over at 0.


## Configurable parameters
### Lower temperature threshold for DSV
Default value: 13.0 (as in the original TOMCAST model)

### DSV (Daily Severity Value) Threshold for high infection risk
Default value: 20

## When to initiate the model
Potato plants vary in susceptibility during the season, and gradually become more susceptible. This means that the requirement for protection against early blight vary accordingly. The model is started when the first symptoms are visible, and first treatment is performed (below 0,1% attack).

## Interpretation of results
The model will be green (no risk) until it reaches 15. From this value the warning will be yellow (possible risk) until the threshold is reached, and the warning turns red (risk of infection).

## Development
Requirements:
* Maven
* Java 11

Clone Gitlab repository

```
$ git clone https://gitlab.nibio.no/VIPS/models/java/Model_ALTERNARIA.git
$ cd Model_ALTERNARIA
```

Build
```
$ mvn install
```