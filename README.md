# Flutterbase taxi

A large variety of apps depend on map services. The purpose of this project was to test Google Map Services in connection with Flutter on Android, iOS and Web platforms. Here is what I got:


![App Demo Images](https://github.com/YakivGalkin/flutterbase-taxi/raw/main/docs/taxi_demo_image.png)


### [Click to open Online Web Demo](https://taxi.flutterbase.com)

## Real life taxi app

The Real taxi app requires development of a scalable server/cloud side storage and logic, authentication, payments, a much more complex workflow/state management, automated testing and deployment, etc. This is just a proof of concept - the sources of this prototype were not used in the production code.

## Installation instruction

Clone the flutterbase taxi application source code repository:

```
git clone https://github.com/YakivGalkin/flutterbase-taxi
cd flutterbase-taxi
```

Install Flutter dependencies

```
flutter pub get
```

### Web

Create Google Cloud API key with the following APIs enabled:

* Maps Javascript API
* Places API
* Directions API
* Geocoding API

Replace the __FLUTTERBASETAXI_API_KEY__ text placeholder with your Google API key in the following files: 
* lib/api/google_api.dart
* web/index.html

Google Places APIs and Directions API cannot be used in browsers due to the CORS rules violation. As a workaround I deployed a simple CORS proxy server running in the google cloud. Path to this server s sored in 'prodApiProxy' variable declared in the 'lib/api/google_api.dart' file.


### Android & iOS

Replace the __FLUTTERBASETAXI_API_KEY__ text placeholder with your Google API key in the /ios/* and /android/* project folders, make sure the following APIs are enabled:


* Maps SDK for Android
* Maps SDK for iOS
* Places API
* Directions API
* Geocoding API






