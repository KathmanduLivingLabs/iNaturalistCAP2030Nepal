# iNaturalistAndroid ![https://github.com/inaturalist/iNaturalistAndroid/actions](https://github.com/inaturalist/iNaturalistAndroid/workflows/CI/badge.svg)

iNaturalistAndroid is an Android app for [iNaturalist.org](http://www.inaturalist.org). If you'd like to contribute code, please check out [Contributing Code to iNaturalist](https://github.com/inaturalist/inaturalist/blob/master/CONTRIBUTING.md) for general guidelines. If you'd like to contribute translations, please provide them through [our Crowdin project](https://crowdin.com/project/inaturalistios) (look for the `strings.xml` file to work on the Android app).

## New in this app
```
1. Nepali translation and language support
2. Quest feature
```

## Setup

1. Make sure you have the latest [Android Studio](https://developer.android.com/studio)
1. Download the iNaturalist source code and extract to a directory of your choosing
1. Go to `iNaturalist/src/main/res/values` and copy `config.example.xml` to `config.xml` (and change its values to match your GMaps, FB, etc. keys)
1. Go to `iNaturalist/` and copy `google-services.example.json` to `google-services.json`. This contains stub values that will allow the app to build but won't connect to Firebase or other Google Services.
1. From Android Studio: File -> Open -> Choose the root directory of the downloaded source code
1. Download and install [Android NDK](https://developer.android.com/ndk/downloads/index.html)
1. Make sure ANDROID_NDK_HOME environment variable points to the NDK root path.
1. If on Mac: Make sure the above env variable is passed to Android Studio's gradle system: https://stackoverflow.com/a/30128305/1233767
1. Clean & build

### Setup for quest

1. Add baato_access_token in string.xml; The token is obtained from https://baato.io. This app use baato maps for quest feature.
2. Setup firebase and obtain google-services.json

The quest can be created in spreadsheet.  The sheet format that quest directly support is found at: https://docs.google.com/spreadsheets/d/1ev51dz0O8flrLLjrBSkp36id_9e-Y4r6ODHGoXTzrmc/edit?usp=sharing

The column Header are as follows
```
id
created_at
valid_until
local_name
scientific_name
description
challange
image	
area
```
You can visit https://geojon.io for creating the area. Area is simply a polygon in geojson format.
