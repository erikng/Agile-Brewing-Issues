# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

# App Store
https://apps.apple.com/us/app/agile-brewing/id1630297854

# Form for Pricing Feedback
https://docs.google.com/forms/d/e/1FAIpQLSeMkMTS8B6eoP-z8_0b02EV8Qau7Xw7OAoqiLkCFr3zyuHV0g/viewform?usp=sf_link

## [1.1.1] - 2022-09-12
### Added
- New "Helper UIs" to inform user on pour over timing and weights during an active pour over session
  - Dynamic Guide for pour progress
  - Prepare user 5 seconds before next component
- Affogato drink type
- Add a new "Pour Over Delay" UI when starting a pour over
  - User changable in Settings tab
  - Defaults to 5 seconds

### Changed
- New Icon!
  - Reduction in App Size due to new icon and better png compression: Download 27% reduction, Install 10% reduction
- Some header texts have been slightly changed in the Settings tab
- Removed bean selector in pour over history view since there is now search
- Refactored Pour Over UI to dynamically hide fields when in an active recipe

### Fixed
- When selecting a bean with a small name, the bean selection text will now take up all horizontal width
- All "Custom" fields now have proper user input sections
- Lots of small bug fixes with Pour Overs that made it kind of annoying

## [1.1.0] - 2022-09-12
### Notes
- This release only supports iOS 16 and higher.
  - v1.0.8 is the last supported release for iOS 15
- If you would like the new pour over views to be ported over to the espresso side, please let me know

### Added
- New User changes
  - An example bean, two espresso templates, five pour over templates and one example espresso shot are pre-installed, allowing the user to fully interact with all tabs
- Welcome screen changes
  - New users get a more detailed report of what the application does
  - Upgraded users get a new informational section on "pour overs"
- Pour Over support!
  - With a radically different UI than the Espresso views, the pour over design is created around replicating your favorite recipes, time and time again
  - Customize the pour over background with millions of colors
  - Don't waste ground coffee! Increase or decrease your dosage and all of your water weight pours will be re-calculated according to your desired ratio
  - Pre-Installed pour over recipes (templates) for v60, Kono Tripper and Tricolate brewers
  - Multiple brew methods: "V60", "Espro Bloom", "Hario Switch", "Kono" and "Tricolate" with the option to input any custom method
  - Custom templates
  - Built-in timer
  - Up to six components
  - Multiple agitation types: "Light Swirl", "Medium Swirl", "Aggressive Swirl", "Shake", and "Stir" with the option to input any custom method
  - Bloom and drip times
  - During an active pour session, pour sections will be highlighted during active pours and bloom/drip times
  - New folders in the Files.app for "pours" and "pour_templates"
  - Pour Over History view allowing you to compare your pour time to the expected time (or recipe time) and a graphical representation of your overall rating of the drink
- Duplicate a drink
  - Take any previous pour over or espresso and use this as the basis of your next shot
  - This greatly reduces the amount of selections to input, allowing you to speed up your pre and post pour process
  - ^ IS MY FAVORITE NEW FEATURE
 Disable the Screen Idle Timer
  - When preparing your espresso shot or more importantly using the new pour over feature, you can now prohibit iOS from turning off your screen
  - This is enabled by default
- Redesign of "Drink History" page
  - Powered by SwiftUI 4 Gauges and Charts, there is now rich content about your drinks, both for espresso and pour over drink types. Track your favorite drinks and see how close you are to your desired yield
  - Search through your drinks and go back in time for that favorite shot
- Enable/Disable Pour Over and Espresso views
  - If you only use the application for one drink type, you can remove the other
  - When using both, the top Navigation Bar will have a different behavior
  - By default, both views are enabled for new and upgrading users
- Disable Drink Ratings
  - Some users have reported that they only track "great" shots and don't need a rating system. This is now an option in the "Settings" tab
- Added "Channeling" and "Additional Notes" to "Drink History" page
- Temperature gauges now show F/C to better differentiate current selection
- Many text fields can now dynamically change their font size to fit the available space
- Added SwiftUI 4 "Scroll Dismisses Keyboard Immediately" logic
- Hidden Long Press views are now in the "Drinks", "Templates" and "Settings" tabs
- Automatically convert templates and drinks "Brew Temp" when changing from Farenheit to Celcius and Celcius to Farenheit

### Changed
- "Reset" and "Submit" buttons in the Espresso Drink, Espresso Template and Bean views have been re-designed
  - New warnings are now shown when the user has not fulfilled all requirements to using the submission button
- Small redesign of "future purchase" UI
- Removed all back-ported SF Symbols from the application, reducing overall app size
- Removed all dynamic if conditions for iOS 15/16 and Xcode 13/14 dynamic compiling logic
- "Desired Ratio" has been limited to 1:5 ratio from 1:15 for espresso.
- "Drink History" lists now contain "Brew Temp" and "Additional Notes"
- Espresso Templates now include portafilter prep fields
- Brew times can now max at F/C boiling points
- Selection text views now follow accessibility rules
- All text fields now have a keyboard dismiss button added to the toolbar in case of SwiftUI keyboard bugs
- Most text views no longer have hardcoded framing, increasing usability in landscape mode for iOS and iPadOS
- Removed "ObservableObject" logic and replaced with "State" and "Binding" logic
- Moved to "NavigationStack" since "NavigationView" is now deprecated
- Increased "minimumScaleFactor" to thousandths for all modifiers
- Redesigned "Star Ratings" with gradients and better spacing
- Redesigned "Tasting Notes" in "Drink History" to flexible vertical grid, improving UI
- Bottom link in "Settings" uses the new "Presentation Detents" option in SwiftUI 4
- "Total Dissolved Solids" tappable area is now the entire horizontal row
- Removed UIKit hack for wheel pickers as they are no longer an input method
- Small changes to the Settings sub-sections
- Moved to SwiftUI 4 built-in gradients

### Fixed
- "Grind Size", "Dosage" and "Actual Yield" selectable areas are now the full horizontal width
- Improved "Actual Yield" calculation (dosage * ratio)
- Fixed known bugs for calculating "Actual Yield" automatically from previous drinks and templates
- Corrected yield discrepancy between "drink" and "drink history" espresso views
- On iOS 15, depending on where the user's field of view is when tapping a selector, the list items may have been in a reverse order
- Refactored "Drink" tab to resolve many performance issues when using Espresso mode
- Refactored significant portions of the "Espresso" logic, increasing performance, decrease compilation time and decreasing repeated code
- Refactored many SwiftUI views into separate components, increasing performance and decreasing code
- Removed all "Lists" from "Form" views, increasing performance

## [1.0.8] - 2022-08-21
### Fixed
- Refactored all selectors that use Decimals to only initialize once, greatly improving the rendering speed

## [1.0.7] - 2022-08-21
### Added
- iOS 15 Improvements
  - Add keyboard toolbar for easily closing keyboard
  - Force "Grind Size" and "Desired Ratio" inputs to menu picker

### Changed
- General User Experience Improvements
  - Redesign "Total Dissolved Solids (TDS)" input from dual wheel pickers to a decimal keyboard
  - Redesign "Dosage" and "Actual Yield" inputs from dual wheel sliders to menu picker
  - Attempt to speed up UI even more when quick scrolling
- Beta iOS Improvements
  - Use enhanced TextField for "Additional Notes"
- Remove all remaining "close keyboard" icons with keyboard toolbar improvement
- Allow drinks to be edited up to 365 days

### Fixed
- Show UI toggles were saving inverted boolean values
  - If you were hiding UI options, it is likely you will need to hide them again
- "Grind Size" automatically moves to current value when using beta iOS. This was a regression when improving iOS 15 behavior

## [1.0.8] - 2022-08-21
### Fixed
- Refactored all selectors that use Decimals to only initialize once, greatly improving the rendering speed

## [1.0.7] - 2022-08-21
### Notes
- iOS 16 Beta releases have some minor issues when scrolling on the "Drink" tab. This will be resolved with the upcoming Xcode 14 GA release

### Added
- iOS 15 Improvements
  - Add keyboard toolbar for easily closing keyboard
  - Force "Grind Size" and "Desired Ratio" inputs to menu picker

### Changed
- General User Experience Improvements
  - Redesign "Total Dissolved Solids (TDS)" input from dual wheel pickers to a decimal keyboard
  - Redesign "Dosage" and "Actual Yield" inputs from dual wheel sliders to menu picker
  - Attempt to speed up UI even more when quick scrolling
- Beta iOS Improvements
  - Use enhanced TextField for "Additional Notes"
- Remove all remaining "close keyboard" icons with keyboard toolbar improvement
- Allow drinks to be edited up to 365 days

### Fixed
- Show UI toggles were saving inverted boolean values
  - If you were hiding UI options, it is likely you will need to hide them again
- "Grind Size" automatically moves to current value when using beta iOS. This was a regression when improving iOS 15 behavior

## [1.0.6] - 2022-08-20
### Changed
- Refactors some selectors that were confusing

### Fixed
- Fixes on automatic settings

## [1.0.5] - 2022-08-17
### Added
- Icon Themes
  - Option for monochrome icon colors
  - Option for borderless icons
  - Options can be combined
- Add degree symbol and F or C on Brew Temp sliders

### Changed
- "Hide UI" is now "Show UI"

### Fixed
- Fix bug when changing from Fahrenheit to Celsius

## [1.0.4] - 2022-08-15
### Added
- Back port some upcoming v1.1 features

### Changed
- Make tappable areas bigger on all sub-menu items

### Fixed
- More speed improvements

## [1.0.3] - 2022-08-15
### Added
- Implemented newer/faster SwiftUI Picker menus from upcoming v1.1 release

## [1.0.2] - 2022-08-15
### Changed
- Remove in-app purchase requirement until more feedback is given around current pricing model

## [1.0.1] - 2022-08-13
### Added
- Showcase UI for "Beans" and "Templates" when you have not purchased a subscription
- Re-assess subscription state when moving from TestFlight to App Store releases

## [1.0] - 2022-08-12
### Added
- Original release
- Espresso, Espresso History, Beans, Templates and Settings
