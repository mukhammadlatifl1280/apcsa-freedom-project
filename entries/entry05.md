# Entry 5
##### 04/27/23

### Context

During the past few weeks I have gained more knowledge of learning my tool SwiftUI. Since I am finished with my MVP as in my minimum valuable product, I am now into tryhard MVP meaning I have to improve my app. Currently, I have so many in my mind about what to do next but I am thinking about the simplest ones such as creating a different page with different set of calculations of taxing. For example, I browsed through websites about taxes and I came across this website about [property tax](https://www.tax.ny.gov/pit/property/learn/proptaxcalc.htm) 
- The formula for the property tax is:

![image](https://info.bcassessment.ca/services-and-products/PublishingImages/Equation.jpg)

This information also varies on your budget, revenue, total taxable assessed value, and tax levy distribution among multiple municipalities but I am only considering to do the calculations part as part of the MVP. As I am learning a brand-new programming language, I would have to start from scratch and gradually improve my knowledge.

### Process

As far as it goes the code would basically be the same as I how I did in sales tax calculator but to showcase it this is how I did it:

```swift
 @IBOutlet weak var marketVal: UITextField!
    @IBOutlet weak var assessedVal: UITextField!
    @IBOutlet weak var taxRate: UITextField!
    @IBOutlet weak var total: UILabel!
 
@IBAction func calculatePropertyTax(_ sender: Any) {
        let market = Double(marketVal.text!)!
        let assessed = Double(assessedVal.text!)!
        let tax = Double(taxRate.text!)!
        
        let totalSalesTax = market * assessed * (5*0.0001)
                
        total.text = "$\(totalSalesTax)"
        
    }
```
The code defines four outlets meaning it will connect these variables to the storyboard: marketVal, assessedVal, taxRate, and total, which correspond to UITextField and UILabel objects in the user interface. The @IBAction function calculatePropertyTax is called when a user taps a button on the interface. Within the function, the code first extracts the values entered by the user from the marketVal, assessedVal, and taxRate text fields by using the text property to get their string values and then converting them to doubles. Next, the code calculates the total tax by multiplying the market and assessed values and then multiplying the result by 5 times 0.0001. This calculation represents a fixed tax rate of 0.0005 (5 times 0.0001), which is applied to the product of market and assessed. Finally, the calculated totalSalesTax value is displayed in the total label as a string with a dollar sign prefix, using string to embed the value into the string.

### Engineering Desing Process(EDP)

Planning, designing, creating, testing, and then improving are the seven steps of the engineering design process (EDP). As a result, the process never ends because there are always methods to make your design better. I intend to enable both testing and user feedback in order to make improvements. I'm now testing at stage 7 and 8 which is improve and communicate. To be specific, I am trying to test out new things and make new functions in my app such as the property tax as my beyond MVP. Maybe later on, I might add on something else if I have enough time.

### Skills

To the best of my knowledge, I am highly skilled in mathematics, and my upcoming project will require me to tackle challenging math problems. Therefore, one of my key abilities is proficiency in mathematics. Additionally, I have the skill of effective time management and careful planning of all tasks before I begin working on them. Above all, I have learned that it is crucial to ask questions when necessary and not hesitate to seek clarification. Currently, I aim to expand my knowledge of SwiftUI and its related programming languages, and subsequently use my best efforts to create a thorough blueprint for testing, making revisions along the way to ensure the best possible outcome.


[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
