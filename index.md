## Agile Brewing
Agile Brewing is an iOS, iPadOS and Mac Catalyst application for recording and hopefully improving your espresso shots.

Written in Swift 5.7 and SwiftUI 4, this project has a minimum OS requirement of the following:
- iOS 16
- iPadOS 16
- macOS Ventura

### JSON Format
Agile Brewing saves all bean profiles, shots and shot templates as JSON files. If you use iCloud Drive it will save under `~/Library/Mobile\ Documents/iCloud\~Agile-Brewing/Documents` on macOS and on iOS/iPad OS under the Files app at the path `Skye-Design.Agile-Brewing`

- Skye-Design.Agile-Brewing/beans
- Skye-Design.Agile-Brewing/shot_templates
- Skye-Design.Agile-Brewing/shots

#### Examples of the JSONs
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
  "usedMDT" : true,
  "usedPuckScreen" : true,
  "usedRDT" : true
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
  "hasChannelling" : false,
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
  "usedMDT" : true,
  "usedPuckScreen" : true,
  "usedRDT" : true,
  "yieldExtraction" : 0,
  "yieldWeight" : 36.0
}
```