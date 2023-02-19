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
The swift code above shows many different types of variables, functions and in my opinion it looks similar to **Java** or **JavaScript**. Looking back at the preview, you have so many options to change from such as colors, fonts, how big the text box can be and whatever you want to have on the screen. After getting this step done, I have accomplished something on my MVP because my mission is to make a app that calculates how much tax you need to pay by the end of the year. This example that I made is useful for single item. For example if a user inputs $59 in the "before tax price" and inserts the percantages as 8.875% in the "Sales Tax Rate" and then click the button Calculate it will appear as how much it will be in total after the tax prices.

## Engineering Design Process [(EDP)](https://hstatsep.github.io/students/#edp)

Planning, designing, creating, testing, and then improving are the seven steps of the engineering design process (EDP). As a result, the process never ends because there are always methods to make your design better. I intend to enable both testing and user feedback in order to make improvements. I'm now testing at stage 4 and 5 which is **plan** and **create**. In terms of aim, my "Tax Calculator App" project will contain features that improve quality of life and make taxation simpler and more programmable. However, in terms of a Minimum Viable Product, I simply need to write a program that accepts user input, processes that information, and then outputs the outcome. Although I have accomplished user input and output, I have not finished my MVP yet.

## Skills

During this past week, the skill I gained was that I got better at learning what I am looking for. I think I am proficient at researching on my tool since I discovered many things about swift just by searching examples on github, looking for videos, visiting links to tutorials etc. Coding is made more efficient and simple in many ways, but it may be made much simpler if you know what you're doing. I've put up a short playlist with materials to help me learn Swfit. Additionally, I'll focus on how to take user input about other information of all the items a user spent over 1 year and calculate all the tax they will pay.


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
