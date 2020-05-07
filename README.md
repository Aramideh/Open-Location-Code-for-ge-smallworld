# GE Smallworld Magik Implementation of Open-Location-Code


### Introduction

Open Location Code is a technology that gives a way of encoding location into a form that is
easier to use than latitude and longitude. The codes generated are called plus codes, as their
distinguishing attribute is that they include a "+" character.

The technology is designed to produce codes that can be used as a replacement for street addresses, especially
in places where buildings aren't numbered or streets aren't named.

Plus codes represent an area, not a point. As digits are added
to a code, the area shrinks, so a long code is more precise than a short
code.

Codes that are similar are located closer together than codes that are
different.

A location can be converted into a code, and a code can be converted back
to a location completely offline.

There are no data tables to lookup or online services required. The
algorithm is publicly available and can be used without restriction.

### Author Notes
This repository is the Magik implementation of Google's Open Location Code ( Plus Code ).



### Getting Started

* Compile the Module
* run below code


##### Encoding
```
Using method OpenLocationCode.new ( latitude , longitude , _optional codeLength , debug?)

for Example :

_block 
	_local oc << OpenLocationCode.new ()
	write ( oc.encode( -37.797491 , 144.9581174) )
_endblock 
$

```

##### Decoding
```
using method OpenLocationCode.decode(code)
for Example:

_block 
	_dynamic !print_float_precision! << 10
	_local bbox << OpenLocationCode.decode( "4RJ68X35+26" )
	write ( "Latitude:",%tab, OpenLocationCode.getCenterLatitude(bbox))
	write ( "Longitude:",%tab, OpenLocationCode.getCenterLongitude(bbox))
_endblock 
$

```



### Author Notes
* This repository is the Magik implementation of google Open Location Code ( Plus Code ).
* This repository is under development.


### Authors

* [**Sadeq Aramideh**](https://github.com/Aramideh)


### License

Please Contact the author for more information.


