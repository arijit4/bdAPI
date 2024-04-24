# bdAPI

This repository aims at making a public and free API to access sorted data of all 64 districts of Bangladesh.

### Usage

Load this following URL with your prefered system and environment. This URL returns the raw JSON of all details I've currently managed to gather.
``` url
https://raw.githubusercontent.com/arijit4/bdAPI/master/all_districts.json
```

### Response structure

``` javascript
[
    {
        "name": String ,      // english name of district
        "bn_name": String,    // bangla name with unicode (for support with UTF-8)
        "district_id": Int,   // district ID used by the gov (can be among 1 to 64)
        "url": String,        // official website of the district
        "sub_districts": {
            "total": Int,     // total number of sub-districts in the district
            "list": [         // list of all sub-districts in the district
                {
                    "id": Int,           // sub-district ID used by the gov
                    "district_id": Int,  // district ID used by the gov (can be among 1 to 64)
                    "name": String,      // english name of the district
                    "bn_name": String,   // bangla name with unicode (for support with UTF-8)
                    "url": String        // official website of the sub-district
                }
            ]
        }
    }
]
```

### Future

I plan to extend the API to a database. I will try to add fields like `division`, `year_establised`, `historical_places`, `famous_for` and many more whenever I find enough resources to do so.

I know most of the info I plan to include are already available in the official websites of the respective districts. But inputting them one by one manually seems real difficult for me.

But yes, you can help me just right here. You can volunteer the fields just for your own district (at least) to get the `database` completed within a very little time. You can also help by providing me with some simplified website (or something like that) so that I can write an automation program and get the information fast without manual labour.

To help me out with this project, please contact me via [this Telegram Group](t.me/bdAPI_chat)
