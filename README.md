# webdriverio-appium-app-browserstack
[WebdriverIO](http://webdriver.io/) Integration with BrowserStack.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

<img src = "http://webdriver.io/images/webdriverio.png" height = "100">

## Setup
* Clone the repo
* Install dependencies `npm install`
* Update `*.conf.js` files inside the `conf/` directory with your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings)

## Running your tests
- Upload your Native App (.apk file) to BrowserStack servers using upload API:

  ```
  curl -u "username:accesskey" -X POST "https://api.browserstack.com/app-automate/upload" -F "file=@/path/to/app/file/Application-debug.apk"
  ```

- If you do not have an .apk file and looking to simply try App Automate, [you can download our sample app and upload](https://www.browserstack.com/app-automate/sample-apps/android/WikipediaSample.apk)
to the BrowserStack servers using the above API.
- Update the desired capability "app" with the App URL returned from the above API call
- To run a single test, run `npm run single`
- To run parallel tests, run `npm run parallel`
- To run local tests, run `npm run local`

## Notes
* You can view your test results on the [BrowserStack automate dashboard](https://www.browserstack.com/automate)
* Refer [Get Started](https://www.browserstack.com/app-automate/get-started#getting-started) document to configure the capabilities
* You can export the environment variables for the Username and Access Key of your BrowserStack account
  
  ```
  export BROWSERSTACK_USERNAME=<browserstack-username> &&
  export BROWSERSTACK_ACCESS_KEY=<browserstack-access-key>
  ```
  
## Additional Resources
* [Getting Started with App Automate](https://www.browserstack.com/app-automate/get-started)
