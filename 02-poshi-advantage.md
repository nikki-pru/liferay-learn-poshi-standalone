# Poshi Advantage

## WebDriver Extended

As mentioned previously, Poshi starts with WebDriver. Poshi implements and extends WebDriver methods to allow even more helpful functions that goes beyond the functionality provided by Selenium. This allows new methods that enable Liferay test writers to create tests that easily navigate through the Liferay DXP UI. Many Poshi methods will be familiar to any tester with Selenium experience. However, Selenium methods are usually basic (e.g. a mouse click) to allow a great degree of flexibility. These are intended to be used as building blocks for helpful web testing tools and functions.

## Page Objects Separated

Poshi uses the **Page Object** design pattern. However, unlike the traditional page object model, Poshi separates the page locators from the page interactions. Embracing the idea of test logic being separated from web elements, all page object locators are defined in a single layer. This single layer maintains all locators and contains a library of hundreds of DXP page element locators that can be used in any test case. The current Poshi pattern treats the product as a combination of elements, rather than a combination of pages. When a Poshi test writer needs to add a new test, it is likely that most of the objects are already defined and able to be referenced by an easy to read locator name. Also, when a UI change is made on the product, generally only one file needs to be updated instead of fixing all test cases.

## Simplified Syntax

In order to make it easier for less technical testers to read and write test automation, Poshi uses a simplified Groovy-like script syntax. It is less wordy than most programming languages and automatically handles the importing of other test files. Poshi is also written so that the test writer does not need to understand Java or JavaScript in order to write new tests, script new behaviors, define page objects, or even create new methods. Only the String data type is supported but string manipulation and math operations are still available.