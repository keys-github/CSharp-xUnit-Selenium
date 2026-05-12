# Run Selenium Tests With xUnit — TestMu AI (Formerly LambdaTest)

![TestMu AI Logo](https://user-images.githubusercontent.com/70570645/171429042-610e8f3d-d2a4-4896-8bdb-8aeed87e0ce7.png)

*Learn how to run C# scripts using the xUnit framework.*

<p align="center">
  <a href="https://www.testmuai.com/blog/" target="_bank">Blog</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/support/docs/" target="_bank">Docs</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/learning-hub/" target="_bank">Learning Hub</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/newsletter/" target="_bank">Newsletter</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.testmuai.com/certifications/" target="_bank">Certifications</a>
  &nbsp; &#8901; &nbsp;
  <a href="https://www.youtube.com/@TestMuAI" target="_bank">YouTube</a>
</p>
&emsp;
&emsp;
&emsp;

[<img height="58" width="200" src="https://user-images.githubusercontent.com/70570645/171866795-52c11b49-0728-4229-b073-4b704209ddde.png">](https://accounts.lambdatest.com/register)


## Table of Contents:

* [Prerequisites](#prerequisites)
* [Run Your First Test](#run-your-first-test)
* [Parallel Testing With xUnit](#running-your-parallel-tests-using-xunit-testing-framework)
* [Local Testing With xUnit](#testing-locally-hosted-or-privately-hosted-projects)


## Prerequisites

Before you start performing **C#** automation testing with **Selenium** using xUnit, you need to:

* Download and install **Selenium WebDriver** from its [official website](https://www.selenium.dev/downloads/).
* Ensure you have the latest version of C#.
* **.NET** framework for guidelines while developing a range of applications using C#.
* Download [Selenium WebDriver Language Binding](https://www.selenium.dev/downloads/) for C# and extract them to the appropriate folder. Require a [.NET Core SDK](https://dotnet.microsoft.com/en-us/download) of 8.0 or greater version.

### Installing Selenium Dependencies And Tutorial Repo

**Step 1:** Clone the TestMu AI CSharp-xUnit-Selenium GitHub repository and navigate to the code directory:

```
git clone https://github.com/LambdaTest/CSharp-xUnit-Selenium
cd CSharp-xUnit-Selenium
```

### Setting up Your Authentication

Ensure you have your TestMu AI credentials to run C# automation scripts. Obtain these credentials from the [TestMu AI Automation Dashboard](https://automation.lambdatest.com/login) or your TestMu AI Profile.

**Step 2:** Set your TestMu AI Username and Access Key in environment variables.

**For Linux/macOS:**

```sh
export LT_USERNAME="YOUR_USERNAME" 
export LT_ACCESS_KEY="YOUR_ACCESS_KEY"
```

**For Windows:**

```sh
set LT_USERNAME="YOUR_USERNAME"
set LT_ACCESS_KEY="YOUR_ACCESS_KEY"
```


## Run Your First Test

> **Test Scenario**: Check out the sample SingleTest.cs file. This xUnit Selenium script tests a sample to-do list app by marking a couple of items as done, adding a new item to the list, and finally displaying the count of pending items as output.

**Step 3:** Navigate to [config.json](https://github.com/LambdaTest/CSharp-xUnit-Selenium/blob/master/XUnit-LambdaTest/config.json/) using VSCode. Replace this code in the config.json file in your project.

### Configuration of Your Test Capabilities

**Step 4:** In the config, update your test capabilities. We are passing browser, browser version, and operating system information, along with TestMu AI Selenium grid capabilities via the capabilities object. 

Example capabilities object:


```json
{
  "server": "hub.lambdatest.com",
  "user": "LT_USERNAME",
  "key": "LT_ACCESS_KEY",

  "capabilities": {
    "lt:options": {
      "buildName": "xunit build",
      "sessionName": "lambdatest xunit sample test",
      "visual": "true",
      "plugin": "xunit:sample"
    }
  },

  "environments": [
    {
      "browserName": "chrome"
    },
    {
      "browserName": "firefox"
    },
    {
      "browserName": "safari"
    }
  ],

  "TunnelOptions": {
    "tunnel": false
  }
}

```

**Note:** Generate capabilities for your test requirements with the help of the **[Desired Capability Generator](https://www.testmuai.com/capabilities-generator/)**.

### Executing the Test

**Step 5:** Build the solution in Visual Studio.

**Step 6:** Run the

 tests from the Test Explorer in Visual Studio.

### Executing in Linux/macOS

* Clean and rebuild the project.

```sh
dotnet clean
```
* Execute Single Test 

```sh
dotnet test --filter "profile=single"
```


## Running Your Parallel Tests Using xUnit Testing Framework

**Executing Parallel tests in Windows**

Run all tests from the Test Explorer in Visual Studio for parallel execution.

**Executing parallel tests in Linux/MacOS**

```sh
dotnet test --filter "profile=parallel"
```


## Testing Locally Hosted Or Privately Hosted Projects

For testing locally hosted or privately hosted projects with TestMu AI Selenium grid using TestMu AI Tunnel, follow the [TestMu AI Tunnel documentation](https://www.testmuai.com/support/docs/testing-locally-hosted-pages/).

Download the TestMu AI Tunnel binary for your OS and run the following command:

```bash
LT -user {user’s login email} -key {user’s access key}
```

**Tunnel Capability**

```json
"lt:options": {
      "buildName": "xunit build",
      "sessionName": "lambdatest xunit sample test",
      "visual": "true",
      "plugin": "xunit:sample",
      "tunnel": "true"
    }
```


## Tutorials 📙

*coming soon*

Subscribe To Our [TestMu AI YouTube Channel 🔔](https://www.youtube.com/@TestMuAI) for the latest video tutorials.


## Documentation & Resources :books:

* [TestMu AI Documentation](https://www.testmuai.com/support/docs/)
* [TestMu AI Blog](https://www.testmuai.com/blog/)
* [TestMu AI Learning Hub](https://www.testmuai.com/learning-hub/)    


## TestMu AI Community :busts_in_silhouette:

Join the [TestMu AI Community](https://community.testmuai.com/) to interact with tech enthusiasts. Connect, ask questions, and learn from professionals worldwide.


## What's New At TestMu AI ❓

Stay updated with the latest features and product add-ons at [Changelog](https://changelog.testmuai.com/).


## 🚀 [LambdaTest is Now TestMu AI](https://www.testmuai.com/lambdatest-is-now-testmuai/)

👋 Welcome to TestMu AI, the next evolution of LambdaTest. As of January 2026, LambdaTest has officially rebranded to TestMu AI. We have evolved from a cross-browser testing cloud into a unified, AI-native quality engineering platform designed for the modern DevOps era.

Whether you have been part of the LambdaTest community for years or are just discovering TestMu AI, our mission remains the same: to help you ship faster with high-scale test execution, autonomous testing, and deep quality analytics.

**🔄 Our Rebrand Journey**

We chose the name TestMu AI to reflect our shift towards intelligent, autonomous testing. While our identity has changed, our core technology and commitment to the testing community stay the same.

**✨ Specialties**

- 🤖 AI-Native Test Execution (Formerly LambdaTest)
- ⚡ Autonomous Test Automation
- 🌐 Cross-Browser & Mobile Testing
- 📊 Unified Quality Intelligence

👉 Find [LambdaTest's New Home](https://www.testmuai.com/).

## We Are Here to Help You :headphones:

* Have a query? We are available 24x7 to help. [Contact Us](mailto:support@testmuai.com)
* For more info, visit [TestMu AI](https://www.testmuai.com/)
