---
layout: post
title: Setup And Write Selenium Scripts.
date: 2018-02-28 15:42:18.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
redirect_from:
  - /2018/02/28/setup-write-selenium-scripts/
  - /2018/02/28/setup-write-selenium-scripts/amp/
cardImage: img_5a95bf47bbe8c.png
meta:
  _edit_last: '1'
  _oembed_20dd7606376650949e781dc71441d972: "{{unknown}}"
  _wp_page_template: default
  post_grid_post_settings: a:10:{s:9:"post_skin";s:4:"flat";s:19:"custom_thumb_source";s:91:"http://abyte.stream/wp-content/plugins/post-grid/assets/frontend/css/images/placeholder.png";s:17:"font_awesome_icon";s:0:"";s:23:"font_awesome_icon_color";s:7:"#737272";s:22:"font_awesome_icon_size";s:4:"50px";s:17:"custom_youtube_id";s:0:"";s:15:"custom_vimeo_id";s:0:"";s:21:"custom_dailymotion_id";s:0:"";s:14:"custom_mp3_url";s:0:"";s:20:"custom_soundcloud_id";s:0:"";}
  _the_champ_meta: a:5:{s:7:"sharing";i:0;s:16:"vertical_sharing";i:0;s:7:"counter";i:0;s:16:"vertical_counter";i:0;s:11:"fb_comments";i:0;}
  _yoast_wpseo_content_score: '90'
  _oembed_818ed07ad8f5703de8bbbfb90d335778: "{{unknown}}"
  _yoast_wpseo_primary_category: ''
  ampforwp_custom_content_editor: ''
  ampforwp_custom_content_editor_checkbox: ''
  ampforwp-amp-on-off: default
  _oembed_c4829536d79ffef4c9a8a07070b87b19: "{{unknown}}"
  _oembed_da9518fbbfb4c9dd5c3b80600e3e84a3: "{{unknown}}"
  _oembed_1911ca92bab7121351c5c1df671da8b1: "{{unknown}}"
  _yoast_wpseo_focuskw_text_input: Setup And Write Selenium Scripts.
  _yoast_wpseo_focuskw: Setup And Write Selenium Scripts.
  _yoast_wpseo_metadesc: Selenium is one of the most popular open source testing automation
    tool. The best thing about any tool can a big community support, Selenium has
    very vast community and it has multiple tools to ease your work. In this blog,
    I am going to discuss about 'Setup And Write Selenium Scripts' . Here is the agenda.
  _yoast_wpseo_linkdex: '63'
  _yoast_wpseo_metakeywords: selenium ide, selenium, ide, browser, test, selenium
    test script, selenium script, selenium test, selenium client, client
  _oembed_5bdbf92b424025e5e56acbf824a88ac8: "{{unknown}}"
author:
  login: sanjaypatel2525
  email: sanjaypatel2525@gmail.com
  display_name: sanjaypatel2525
  first_name: ''
  last_name: ''
---
Selenium is one of the most popular open source testing automation tool. The best thing about any tool can a big community support, Selenium has very vast community and it has multiple tools to ease your work.  In this blog, I am going to discuss about 'Setup And Write Selenium Scripts' . Here is the agenda.

* Why should you use Selenium?
* What are tools involved in Selenium and which tool is right for you?
* How to use Selenium IDE to generate the selenium scripts?
* Finally, writing code to cover test cases (Not really required if you selenium IDE).

## Why should you use selenium?
<img class="alignnone size-full wp-image-216" src="{{ site.baseurl }}/assets/img_5a95bf47bbe8c.png" alt="" />
## Tools involved in Selenium
 <img class="alignnone wp-image-223 size-full" src="{{ site.baseurl }}/assets/untitle-1.jpeg" alt="" width="799" height="295" />
There are multiple tools provided by selenium to create and run the tests.


### Selenium Webdriver
Selenium Webdriver is the interface which accepts commands from Selenium clients and executes on the respective browser. In simple term, we can selenium web driver opens up a browser and run the commands on that browser.  Every browser will have there own web drivers. Here is the link you can use to download the web drivers.

<a href="https://www.seleniumhq.org/download/" rel="nofollow">https://www.seleniumhq.org/download/</a>
<img class="alignnone size-full wp-image-225" src="{{ site.baseurl }}/assets/img_5a95c8cd481a4.png" alt="" />


### Selenium Clients  (Web drivers client).
Selenium clients are nothing but the interface which is used by our code or program to deal with selenium servers.  Let take an example of simple HTTP service, any site which is available on browser acts as server and browser acts as a client. Same way even our codes requires a selenium client to deal with selenium server.

In order to write selenium script, you will need a selenium client as well.  There is list of clients available in selenium sites, depending on what coding language you use, you can pick respective clients.
<img class="alignnone size-full wp-image-226" src="{{ site.baseurl }}/assets/img_5a95c8e884a09.png" alt="" />


### Selenium IDE.
Selenium IDE is a tool provided by selenium to records the actions which you can use to create selenium script. This is really a timesaver for you. Rather going through the complete documentation on selenium before starting on writing selenium code, you can directly go in your browser and start recording your action and selenium IDE will give you the option to export your recording as test scripts.

## Use Selenium IDE to generate the selenium scripts.
<img class="alignnone size-full wp-image-224" src="{{ site.baseurl }}/assets/img_5a95c4f1000f7.png" alt="" />
### Steps to setup and record selenium IDE.
Selenium IDE is only supported for Firefox, this does not mean you can not run your script from another browser. Script generation needs Firefox, but the script can be run for any browser.


### Firefox and Selenium versions
Due to going demand of browsing speed and being robust against security threats, the browser has kept itself updated and with this even Selenium has to be updated. To get rid of this problem you can plan to have a fixed version of the browser and fixed version of selenium.  For example, I use selenium and firefox inside a VM and have disabled all the browser updates. This keeps my test cases running.  I am using Firefox version 54 and selenium IDE 2.9.1

### To install firefox go below links and install.
https://ftp.mozilla.org/pub/firefox/releases/54.0.1/win64/en-US/

### To install Selenium IDE go to firefox addons URL.
https://addons.mozilla.org/en-US/firefox/addon/selenium-ide/
In case you do not find any supported version, check the plugins supported version and download that specific firefox version.
https://ftp.mozilla.org/pub/firefox/releases/

### Go to tools (press ALT) in Firefox and click on Selenium IDE.
<img class="alignnone size-full wp-image-230" src="{{ site.baseurl }}/assets/img_5a95d43ac87e4.png" alt="" />

Click on the record button.
<img class="alignnone size-full wp-image-231" src="{{ site.baseurl }}/assets/img_5a95d4ebf175b.png" alt="" />


### Stop recording once you have manually run the test.
Now go back to Firefox and start running the test steps manually. Once it is done click on that red button again in Selenium IDE to stop recording the script. Now you will there is lot lines generated in Selenium IDE.  These are the commands which can be run again to repeat the steps. These commands can be exported as a test script in any language you want.
One thing to note here you sometimes these scripts are not accurate and you have to manually edit scripts.

### Export the test script to your favorite language.
Go to File -> Export Test Cases -> Select web driver with your preferred language.
It will create respective script files.  This file you can directly use to run the selenium test case.
<img class="alignnone size-full wp-image-232" src="{{ site.baseurl }}/assets/img_5a96c382f2aeb.png" alt="" />
## Writing code to cover your test cases.
The last step to this is, Once the code is exported you can import it in your favorite IDE (eclipse, Netbeans, Visual studio code etc) or you can directly run it using command line commands supported by the language.  For example java.
java -cp .:/usr/share/java/junit.jar org.junit.runner.JUnitCore [test class name]

Here is an example how it looks in Eclipse.  Also,  notice I have geckodriver.exe as well in my libraries, which is nothing but a firefox Webdriver. You can download it from selenium site for another browser as well.
<img class="alignnone size-full wp-image-234" src="{{ site.baseurl }}/assets/img_5a96c7cd0484a.png" alt="" />


## What's next....
Once you finished creating all your test scenarios you can configure it to run automatically either by scheduled cron jobs or use Jenkins for continuous integration.
Jenkins is an open-source continuous integration tool, You can automate a lot of dev ops stuff like build, deployments, testing, monitoring etc. For this please read my another blog on configuring selenium with Jenkins.
