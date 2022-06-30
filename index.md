# Agile Brewing
![AppIcon](/assets/AppIcon.png)

Agile Brewing is an iOS, iPadOS and Mac Catalyst application for recording and hopefully improving your espresso shots.

Written in Swift 5.7 and SwiftUI 4, this project has a minimum OS requirement of the following:
- iOS/iPadOS 15.4
- macOS Monterey 12.4

To utilize all of the features available, please use iOS/iPadOS 16 or higher and macOS Venture 13.0 or higher.

## Getting Support
Please go to the [GitHub Issues](https://github.com/erikng/Agile-Brewing-Issues/issues) page to submit any potential issues you are experiencing.

## JSON Format
Agile Brewing saves all bean profiles, shots and shot templates as JSON files. If you use iCloud Drive it will save under `~/Library/Mobile\ Documents/iCloud\~Agile-Brewing/Documents` on macOS and on iOS/iPad OS under the Files app at the path `Skye-Design.Agile-Brewing`

Inside of the root path, there are three sub-folders to correspond with each JSON type.
- Skye-Design.Agile-Brewing/beans
- Skye-Design.Agile-Brewing/shot_templates
- Skye-Design.Agile-Brewing/shots

### Examples of the JSONs
The following are examples of the JSON structure

##### Bean
```json
{
  "id" : "CAB6B075-9F2C-4F32-910D-ECAD2AD6518E",
  "name" : "Example Bean Name",
  "origin" : "Example Origin Country",
  "roastDate" : 676602960,
  "roastDateEpoch" : 1655947003.8767362,
  "roaster" : "Example Roaster",
  "roastProfile" : "Light"
}
```

##### Shot Templates
```json
{
  "brewTemp" : 205,
  "desiredRatio" : 2,
  "doseWeight" : 18,
  "id" : "CB195692-68B9-45DC-B6E3-AC96BA8C849E",
  "selectedFilter" : "",
  "tampWeight" : 30,
  "templateName" : "Example Templates",
  "usedCoffeeDistributionTool" : true,
  "usedPuckScreen" : true,
  "usedRDT" : true,
  "usedWDT" : true
}
```

##### Shots
```json
{
  "appearanceRating" : 5,
  "aromaRating" : 5,
  "brewTemp" : 205,
  "cremaRating" : 5,
  "desiredRatio" : 2,
  "doseWeight" : 18,
  "grindSize" : 19,
  "groupHeadPreHeated" : true,
  "hasChanneling" : false,
  "id" : "820B31FF-7BBF-40B3-B927-3D85A8E9292E",
  "notes" : "Example Notes",
  "overallRating" : 5,
  "portafilterPreHeated" : true,
  "preInfusionTime" : 7,
  "puckConsistency" : "Dry",
  "resultingDrink" : "Espresso",
  "selectedBeanProfile" : {
    "id" : "CAB6B075-9F2C-4F32-910D-ECAD2AD6518E",
    "name" : "Example Bean Name",
    "origin" : "Example Origin Country",
    "roastDate" : 676602960,
    "roastDateEpoch" : 1655947003.8767362,
    "roaster" : "Example Roaster",
    "roastProfile" : "Light"
  },
  "selectedFilter" : "",
  "selectedNote1" : "Balanced",
  "selectedNote2" : "",
  "selectedNote3" : "",
  "selectedNote4" : "",
  "selectedNote5" : "",
  "selectedNote6" : "",
  "shotDate" : 678128713.73826003,
  "shotDateEpoch" : 1656435913.73826,
  "shotTime" : 23,
  "tampWeight" : 30,
  "tasteRating" : 5,
  "totalDissolvedSolids" : 0,
  "usedCoffeeDistributionTool" : true,
  "usedPuckScreen" : true,
  "usedRDT" : true,
  "usedWDT" : true,
  "yieldExtraction" : 0,
  "yieldWeight" : 36.0
}
```

## Screenshots
This is the current beta UI

![WelcomeScreen](/assets/WelcomeScreen.png)

![BeanProfile](/assets/BeanProfile.png)

![ShotTemplates-1](/assets/ShotTemplates-1.png)

![ShotTemplates-2](/assets/ShotTemplates-2.png)

![EspressoShot-1](/assets/EspressoShot-1.png)

![EspressoShot-2](/assets/EspressoShot-2.png)

![EspressoShot-3](/assets/EspressoShot-3.png)

![EspressoShot-4](/assets/EspressoShot-4.png)

![EspressoShot-5](/assets/EspressoShot-5.png)

![ShotHistory-1](/assets/ShotHistory-1.png)

![ShotHistory-2](/assets/ShotHistory-2.png)

![ShotHistory-3](/assets/ShotHistory-3.png)

![Settings-1](/assets/Settings-1.png)

![Settings-2](/assets/Settings-2.png)

![Settings-3](/assets/Settings-3.png)
