# SJMeterStyleSliderView
The SJMeterStyleSliderView control is a completely customisable widget that can be used in any iOS app. It also plays a little victory fanfare.

### Prerequisites
*  XCode > 9.0
*  Swift > 4.0

# SJMeterStyleSliderView

[![Version](https://img.shields.io/cocoapods/v/SJMeterStyleSliderView.svg?style=flat)](http://cocoapods.org/pods/SJMeterStyleSliderView)
[![License](https://img.shields.io/cocoapods/l/SJMeterStyleSliderView.svg?style=flat)](http://cocoapods.org/pods/SJMeterStyleSliderView)
[![Platform](https://img.shields.io/cocoapods/p/SJMeterStyleSliderView.svg?style=flat)](http://cocoapods.org/pods/SJMeterStyleSliderView)

![](Sample1.gif?raw=true "SJMeterStyleSliderView screenshot")

# Overview
The SJMeterStyleSliderView control is a completely customisable widget that can be used in any iOS app. It also plays a little victory fanfare.

## Requirements
* ARC
* iOS8


## Installation

SJMeterStyleSliderView is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "SJMeterStyleSliderView"
```
## Usage
```Swift
//TODO: To import Slider View for use
import SJMeterStyleSliderView

<!--Now you can create an UI in your storyboard and assign class of a view to SJMeterStyleSliderView to use this UI Control for Meter Slider.-->
<!---->
<!--You can also use delegate to get selected index and use moveSliderToIndex method to move slider programeticaly.-->

<!--Ex. Code--->

import SJMeterStyleSliderView

class ViewController: UIViewController, SJMeterStyleSliderViewDelegate {

    @IBOutlet var sliderView : SJMeterStyleSliderView!
    @IBOutlet var stepper : UIStepper!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
        self.sliderView.delegate = self
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    @IBAction func valueChanged(_ sender: UIStepper) {
        self.sliderView.moveSliderToIndex(index: Int(sender.value), withAnimation: true)
        
    }
    func didChangeSelectedIndex(index: Int) {
        print("Selected Index : ", index)
        stepper.value = Double(index)
    }
}


```
## Built With
*  Swift
*  UIKit


## Contributing

Please read [CONTRIBUTING.md](https://github.com/sumitjagdev/SJMeterStyleSliderView/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.


## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [releases on this repository](https://github.com/sumitjagdev/SJMeterStyleSliderView/releases).


## Author

* **Sumit Jagdev**  ,  *sumitjagdev3@gmail.com*


## License

SJSwiftSideMenuController is available under the MIT license. See the LICENSE file for more info.
