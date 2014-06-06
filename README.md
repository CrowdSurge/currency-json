#Currencies

A JSON List of Currency Formats &amp; Information


## What It Contains

```javascript
"GBP": {
    "name": "Pound Sterling",
    "iso": "GBP",
    "isoNumeric": 826,
    "format": "-£###,###,###.##",
    "symbol": {
        "default": "£",
        "native": "£",
        "hex": "00A3",
        "decimal": 163
    },
    "units": {
        "decimal": 2,
        "sub": 100,
        "name": {
            "major": "Pound",
            "minor": "Pence"
        }
    }
}
```

#### ```name```
The name of the currency

#### ```iso```
The three-digit ISO-4217 Currency code

#### ```isoNumeric```
The ISO-3166-1 numeric country code for the parent country of the currency (eg. US Dollar = 840, for USA)

#### ```format```
A DecimalFormat style string for displaying positive and negative currency amounts, with symbols (see below for a gist that works with these)

#### ```symbol.default```
The default symbol, used globally, for this currency

#### ```symbol.native```
The native symbol, used in the local territory, for the currency

#### ```symbol.hex```
Hex value (if available) for the native symbol

#### ```symbol.decimal```
Decimal value (if available) for the native symbol

#### ```units.decimal```
Number of decimal units used in the currency

#### ```units.sub```
Number of sub-units used in the currency. eg: 100 Pence GBP = 1 Pound GBP

#### ```units.name.major```
The name for the major unit. eg. GBP: Pound

#### ```units.name.minor```
The name for the minor unit eg. GBP: Pence


## Formatting String
The ```format``` value can be used to display the currency in a format familiar to local users. For example, GBP uses decimal points to indicate decimals, where EUR uses commas.

The location of negative value indicators also changes dependent on currency.

The following gist will format a number using the format string supplied in the JSON: 
https://gist.github.com/benhodgson87/becf5884a53d90f86b6e


## Contribute
If a currency is missing, or you've noticed some mistakes, please submit a pull request. Any help keeping this as complete and up-to-date as possible is greatly appreciated.

Please ensure when submitting a PR that you stick to the existing formatting (4-space tabs, etc.)
