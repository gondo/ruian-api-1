
#ruian-api

RÚIAN API Client for Node JS. It supports the **REST API**.

Methods available are:
- Geocode (get coordinate of address place) - address id / fulltext / parametric search
- CompileAddress (build address) - address id / fulltext / parametric search
- FullTextSearch (fulltext address search)
- Validate (validate address) - parametric search
- ValidateAddressId (validate address id)
- NearByAddresses (search for the nearest places)

#Installing

```
npm install ruian-api
```

##Usage:

```javascript


#ruian-api

##`var ruianapi = require('ruian-api');`

Create a `ruianapi` instance that can be used to make requests to RÚIAN's APIs.

```

 // 'some address id'
var AddressPlaceId = '26188511';

// parametric search
// 'some address parts'
var Street,
    HouseNumber,
    RecordNumber,
    OrientationNumber,
    OrientationNumberCharacter,
    ZIPCode,
    Locality,
    LocalityPart,
    DistrictNumber = '';

// fulltext search
// 'some address'
var SearchText = 'Habrová 128 25066 Zdiby';
```

Fill address values to variables.

```

var currentAddress = ruianapi.methodX(params);

```

Call methods as async to receive response. As methodX you can choose one of following:

```

Geocode(AddressPlaceId) { ... }
Geocode(SearchText) { ... }
Geocode(Street, HouseNumber, RecordNumber, OrientationNumber, OrientationNumberCharacter, ZIPCode, Locality, LocalityPart, DistrictNumber) { ... }  // you can fill only some
CompileAddress(AddressPlaceId) { ... }
CompileAddress(SearchText) { ... }
CompileAddress(Street, HouseNumber, RecordNumber, OrientationNumber, OrientationNumberCharacter, ZIPCode, Locality, LocalityPart, DistrictNumber) { ... }  // you can fill only some
FullTextSearch(SearchText) { ... }
Validate (Street, HouseNumber, RecordNumber, OrientationNumber, OrientationNumberCharacter, ZIPCode, Locality, LocalityPart, DistrictNumber) { ... }
ValidateAddressId (AddressPlaceId) { ... }
NearByAddresses (JTSKY, JTSKX, Distance) // JTSK is Czech coordinate system (https://epsg.io/5514)

```

-------

## License

The MIT License

Copyright (c) 2016 by David Kocich <dkocich@gmail.com>. All rights reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

## Changelog

###0.0.1

  * first commit and testing version release