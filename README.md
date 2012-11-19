# jenkins-automation
===
###Jenkins Testing Integration

jenkins-automation is a toolbox for automated test coverage of iOS apps using the continuous integration server [Jenkins](http://jenkins-ci.org). 

#####Coverage

- Logic Testing via SenTestingKit (OCUnit)
- Application Testing via SenTestingKit (OCUnit)
- Integration (User Interface) Testing via UIAutomation

## Prerequisites

- [Jenkins](http://jenkins-ci.org)
- [Xcode 4.x](https://developer.apple.com/xcode/)
- [ios-sim](https://github.com/phonegap/ios-sim) 




## How To Get Started 
to be filled with content

===
#####Jenkins Build Script

######build.sh

Automatically calls unit_testing.sh and integration_testing.sh
You may modify some constants in this script:

* PROJECT_PREFIX
* APPNAME
* PLISTPATH
* XCODEPROJECTPATH
* INHOUSE_SCHEME
* ADHOC_SCHEME
* INHOUSE_IPA_NAME
* ADHOC_IPA_NAME
* UNITTESTNAME
* UIAUTOMATIONPREFIX
* UIAUTOMATIONTESTPATH
* SIMULATORSDK

===
#####Unit Testing Execution Script

######unit_testing.sh

Parameter:

* SDK name
* unit test target name

Example:

```
/bin/sh unit_testing.sh iphonesimulator MyAppTests
```
![ScreenShot](https://raw.github.com/i-saumitra/Voice-controlled-MP3-Player/master/screenshot.jpg)

===
#####Integration Testing Execution Script

######integration_testing.sh

Parameter:
 
* SDK name
* app name
* UIAutomation prefix
* UIAutomation test path

Example:

```
/bin/sh integration_testing.sh iphonesimulator MyApp foo bar
```
===
#####Integration Testing Transformer Stylesheet

######integration_test_result_transform.xsl


Parameter:

* Title
* ScreenshotPathPrefix
* SmileyPathPrefix

Example:

```
xsltproc --stringparam Title "FooBar" --stringparam ScreenshotPathPrefix "test/" --stringparam SmileyPathPrefix "foo/" -output out.html transform.xsl Automation\ Results.plist
```

===

## Contact


### Creators

[Sven Jansen](http://github.com/macsven)  
[Till Toenshoff](http://github.com/lobotomat)  
