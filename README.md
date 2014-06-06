#Currencies

A JSON List of Currency Formats &amp; Information


## What It Contains

```javascript
"JPY": {
    "name": "Japanese Yen",
    "iso": {
        "code": "JPY",
        "num": 392
    }
    "symbol": {
        "default": {
            "display": "¥",
            "code": "&#xa5;"
        },
        "native": {
            "display": "円",
            "code": "&#x5186;"
        }
    },
    "units": {
        "decimal": 0,
        "sub": 0,
        "name": {
            "major": "Yen",
            "minor": null
        }
    },
    "format": "-###,###,###円"
}
```

#### ```name```
The name of the currency

#### ```iso```
The three-letter ISO-4217 currency code

#### ```isoNumeric```
The three-digit ISO-4217 numeric currency code

#### ```format```
A DecimalFormat style string for displaying positive and negative currency amounts, with symbols (see below for a gist that works with these)

#### ```symbol.default.display```
The default symbol, used globally, for this currency

#### ```symbol.default.code```
HTML Hex value for this symbol

#### ```symbol.native```
If a currency is displayed differently natively (eg. A different symbol for Yen is commonly used in Japan), an object will be returned. Otherwise ```null```

#### ```symbol.native.display```
The native display symbol, used in local territories, for this currency

#### ```symbol.native.code```
HTML Hex value for this symbol

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
