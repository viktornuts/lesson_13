Project in Allure TestOps with manual & automated tests
allure.autotests.cloud/project/%s (ask admin@qa.guru for access)

Jenkins job
jenkins.autotests.cloud/job/%s

USAGE examples
For run remote tests need fill remote.properties or to pass value:
browser (default chrome)
browserVersion (default 89.0)
browserSize (default 1920x1080)
browserMobileView (mobile device name, for example iPhone X)
remoteDriverUrl (url address from selenoid or grid)
videoStorage (url address where you should get video)
threads (number of threads)
Run tests with filled remote.properties:

gradle clean test
Run tests with not filled remote.properties:

gradle clean -DremoteDriverUrl=https://%s:%s@selenoid.autotests.cloud/wd/hub/ -DvideoStorage=https://selenoid.autotests.cloud/video/ -Dthreads=1 test
Serve report:

allure serve build/allure-results
For further development there are some example tests in src/test/java/cloud.autotests/tests/demowebshop
remove @Disabled("...") annotation to run tests
gradle clean demowebshop
