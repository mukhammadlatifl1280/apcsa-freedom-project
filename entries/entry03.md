# Entry 3
##### 02/19/23

## Context
During the past few weeks I have gained more knowledge of learning my tool SwiftUI. I have visited several links on how to use the tool for beginners. For example I have searched specifically "how to use swift UI to make front end examples" then I visited examples through github websites. This brought me to the [swiftUI tutorials](https://github.com/mrcflorian/swiftUI-tutorials) and basics functions(i.e. How to use Firebase with swiftUI) and I scrolled through to read and how to use it. I also browse through some examples and tutorials on basics about SwiftUI. The examples from github explained thoroughly on the basic steps on how to use functions of SwiftUI. After watching the examples and tutorials, I finally managed to make something that works. As I didn't know what they all meant, I found the swiftUI installation procedure to be incredibly confusing as there were so many functions to pick from. As I am learning a brand-new programming language, I would have to start from scratch and gradually improve my knowledge.

## Process

As I have mentioned early, this is what I made so far that is half way to making my MVP.

![Preview](https://github.com/mukhammadlatifl1280/apcsa-freedom-project/blob/master/screenshot1.png)

The screenshot above shows what I made using SwiftUI and has some back ends with swift code as shown below:

```swift
import UIKit

class ViewController: UIViewController {
    
    var beforeTaxPrice: Float = 0
    var salesTaxRate: Float = 0
    
    @IBOutlet weak var afterTaxPriceTextField: UITextField!
    
    override func viewDidLoad() {
        super.viewDidLoad()
    }
    
    func parseInputsToFloat(text: String) -> Float {
        if let value = Float(text) {
            return value
        }
        return 0
    }

    @IBAction func beforeTaxPriceChanged(_ sender: UITextField) {
        beforeTaxPrice = parseInputsToFloat(text: sender.text!)
    }
    
    @IBAction func salesTaxRateChanged(_ sender: UITextField) {
        salesTaxRate = parseInputsToFloat(text: sender.text!)
    }
    
    @IBAction func calculateButtonPressed(_ sender: Any) {
        let salesTax = beforeTaxPrice * salesTaxRate / 100
        let afterTaxPrice = beforeTaxPrice + salesTax
        afterTaxPriceTextField.text = String(afterTaxPrice)
    }
}
```

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
