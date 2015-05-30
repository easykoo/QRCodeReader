# QRCodeReader

A simple QRCode reader for Swift (based on [CDZQRScanningViewController](https://github.com/cdzombak/CDZQRScanningViewController))

[![Version](https://img.shields.io/cocoapods/v/QRCodeReader.svg?style=flat)](http://cocoapods.org/pods/QRCodeReader)

## Usage

```swift
let reader = QRCodeReaderViewController()
reader.resultCallback = {
    println($0)
    reader.dismissViewControllerAnimated(true, completion: nil)
}
reader.cancelCallback = {
    reader.dismissViewControllerAnimated(true, completion: nil)
}
presentViewController(reader, animated: true, completion: nil)
```

## Requirements

* iOS 8.0+
* Xcode 6.3 (Swift 1.2)

## Installation

QRCodeReader is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "QRCodeReader", :git => 'https://github.com/ricardopereira/QRCodeReader.git'
```

You will also need to make sure you're opting into using frameworks:

```ruby
use_frameworks!
```

Then run `pod install` with CocoaPods 0.36 or newer.

## Author

Ricardo Pereira, [@ricardopereiraw](https://twitter.com/ricardopereiraw)

## License

QRCodeReader is available under the MIT license. See the LICENSE file for more info.
