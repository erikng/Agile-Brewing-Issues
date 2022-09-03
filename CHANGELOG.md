# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2022-09-13
### Added
- TODO

### Changed
- TODO

### Fixed
- TODO

## [1.0.8] - 2022-08-21
### Fixed
- Refactored all selectors that use Decimals to only initialize once, greatly improving the rendering speed.

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
- Show UI toggles were saving inverted boolean values.
  - If you were hiding UI options, it is likely you will need to hide them again
- "Grind Size" automatically moves to current value when using beta iOS. This was a regression when improving iOS 15 behavior

## [1.0.8] - 2022-08-21
### Fixed
- Refactored all selectors that use Decimals to only initialize once, greatly improving the rendering speed.

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
- Show UI toggles were saving inverted boolean values.
  - If you were hiding UI options, it is likely you will need to hide them again
- "Grind Size" automatically moves to current value when using beta iOS. This was a regression when improving iOS 15 behavior

### Notes
- iOS 16 Beta releases have some minor issues when scrolling on the "Drink" tab. This will be resolved with the upcoming Xcode 14 GA release

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
- Implemented newer/faster SwiftUI Picker menus from upcoming v1.1 release.

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