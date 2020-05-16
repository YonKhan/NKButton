# NKButton

[![Version](https://img.shields.io/cocoapods/v/NKButton.svg?style=flat)](http://cocoapods.org/pods/NKButton)
[![License](https://img.shields.io/cocoapods/l/NKButton.svg?style=flat)](http://cocoapods.org/pods/NKButton)
[![Platform](https://img.shields.io/cocoapods/p/NKButton.svg?style=flat)](http://cocoapods.org/pods/NKButton)
![Swift](https://img.shields.io/badge/%20in-swift%204.2-orange.svg)

A fully customizable UIButton

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

![NKButton](https://github.com/kennic/NKButton/blob/master/demo.gif)

## Installation

NKButton is available through `Swift Package Manager` (Recommended) and [CocoaPods](http://cocoapods.org):


```ruby
pod 'NKButton'
```

## Usage

Creation and basic customization:
```swift
let button = NKButton()
button.title = "Button"
button.setTitleColor(.black, for: .normal) // set title color for normal state
button.setTitleColor(.white, for: .highlighted) // set title color for highlight state
button.setTitleFont(normalFont, for: .normal)
button.setTitleFont(boldFont, for: .highlight)
button.setBackgroundColor(.blue, for: .normal) // set background color for normal state
button.setBackgroundColor(.green, for: .highlighted) // set background color for highlight state
button.spacing = 10.0 // space between icon and title
button.imageAlignment = .top // icon alignment
button.underlineTitleDisabled = true // no underline text when `Settings > Accessibility > Button Shapes` is ON
button.isRoundedButton = true
button.cornerRadius = 10.0
button.extendSize = CGSize(width: 50, height: 20) // size that will be included in sizeThatFits
```

Add border:
```swift
button.setBorderColor(.black, for: .normal) // set border color for normal state
button.setBorderColor(.white, for: .highlighted) // set border color for highlight state
button.setBorderSize(1.0, for: .normal) // border stroke size
button.setBorderSize(2.0, for: .highlighted)
```

Add shadow:
```swift
button.setShadowColor(.blue, for: .normal) // set shadow color for normal state
button.setShadowColor(.green, for: .highlighted) // set shadow color for highlight state
button.shadowOffset = CGSize(width: 0, height: 5)
button.shadowOpacity = 0.6
button.shadowRadius = 10
```

Add gradient color:
```swift
button.setGradientColor([UIColor(white: 1.0, alpha: 0.5), UIColor(white: 1.0, alpha: 0.0)], for: .normal) // set gradient color for normal state
button.setGradientColor([UIColor(white: 1.0, alpha: 0.0), UIColor(white: 1.0, alpha: 0.5)], for: .highlighted) // set gradient color for highlight state
```

Set loading state:

```swift
button.loadingIndicatorStyle = .ballBeat // loading indicator style
button.loadingIndicatorAlignment = .atImage // loading indicator alignment
button.hideImageWhileLoading = true
button.hideTitleWhileLoading = false

button.isLoading = true // show loading indicator in the button, and button will be disabled automatically until setting isLoading = false
```

Flashing:
```swift
button.startFlashing()
button.startFlashing(flashDuration: 0.25, intensity: 0.9, repeatCount: 10)
```

## Subscript syntax:
```swift
button.titleColors[.normal] = .black
button.titleFonts[.normal] = normalFont
button.titleFonts[.highlight] = boldFont
button.backgroundColors[.normal] = .white
button.backgroundColors[.highlight] = .yellow
button.borderColors[.normal] = .gray
button.borderColors[[.highlight, .selected]] = .black
button.shadowColors[.normal] = .black
```

## Dependency

NKButton uses [NVActivityIndicatorView](https://github.com/ninjaprox/NVActivityIndicatorView) for loading indicator, so it currently has 32 animation types.

NKButton uses [FrameLayoutKit](https://github.com/kennic/FrameLayoutKit) for content layout so you can customize the layout easily

## Author

Nam Kennic, namkennic@me.com

## License

NKButton is available under the MIT license. See the LICENSE file for more info.
