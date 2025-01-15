# Katalon Studio Framework

## Overview
This repository contains an **automation testing framework** built using **Katalon Studio**, a leading test automation platform. The framework focuses on automating **web and API testing** with minimal coding, leveraging Katalon’s built-in tools for ease of use and integration with CI/CD pipelines.

## Key Features:
- **Katalon Studio** for cross-browser, mobile, web, and API testing
- **Built-in Test Execution** for easy creation and running of test cases
- Seamless integration with **Jenkins** for continuous integration
- Detailed **HTML Reports** for clear test execution results
- Supports both **manual and automated tests** in a single framework

## Project Structure:
- **Tests**: Contains test cases and test suites.
- **Keywords**: Custom reusable functions created within Katalon Studio.
- **Data Files**: CSV or Excel files containing test data.
- **Reports**: Folder for storing detailed test execution reports.
- **Katalon Project Settings**: Contains configurations for browsers, execution environments, and reporting.

## Getting Started:
1. Clone this repository:  
   `git clone https://github.com/yourusername/katalon-framework.git`
2. Open the project in **Katalon Studio**.
3. Install necessary dependencies through **Katalon Studio's interface**.
4. Run tests directly from the Katalon Studio UI.

## Example Test Case:
```groovy
import static com.kms.katalon.core.testobject.ObjectRepository.findTestObject
import com.kms.katalon.core.webui.keyword.WebUiBuiltInKeywords as WebUI

WebUI.openBrowser('http://example.com')
WebUI.setText(findTestObject('Object Repository/InputField'), 'Test Data')
WebUI.click(findTestObject('Object Repository/SubmitButton'))
WebUI.verifyTextPresent('Success', false)
WebUI.closeBrowser()
