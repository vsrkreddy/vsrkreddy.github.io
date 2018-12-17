---
layout: post
title: E2E Browser Testing with Protractor
date: 2018-03-02 03:36:41.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
cardImage: untitle2.jpeg
meta:
  _edit_last: '1'
  _thumbnail_id: '253'
  _wp_page_template: default
  post_grid_post_settings: a:10:{s:9:"post_skin";s:4:"flat";s:19:"custom_thumb_source";s:91:"http://abyte.stream/wp-content/plugins/post-grid/assets/frontend/css/images/placeholder.png";s:17:"font_awesome_icon";s:0:"";s:23:"font_awesome_icon_color";s:7:"#737272";s:22:"font_awesome_icon_size";s:4:"50px";s:17:"custom_youtube_id";s:0:"";s:15:"custom_vimeo_id";s:0:"";s:21:"custom_dailymotion_id";s:0:"";s:14:"custom_mp3_url";s:0:"";s:20:"custom_soundcloud_id";s:0:"";}
  _the_champ_meta: a:5:{s:7:"sharing";i:0;s:16:"vertical_sharing";i:0;s:7:"counter";i:0;s:16:"vertical_counter";i:0;s:11:"fb_comments";i:0;}
  _yoast_wpseo_content_score: '90'
  _yoast_wpseo_primary_category: ''
  ampforwp_custom_content_editor: ''
  ampforwp_custom_content_editor_checkbox: ''
  ampforwp-amp-on-off: default
  _yoast_wpseo_focuskw_text_input: End to End (E2E) Browser Testing with Protractor
    - Angular and Non Angular
  _yoast_wpseo_focuskw: End to End (E2E) Browser Testing with Protractor - Angular
    and Non Angular
  _yoast_wpseo_metadesc: There are many ways to test our application but having a
    testing with end user feel is the always the important one. The protractor is
    JS framework built up Selenium JS web driver. It provides ease of End to End (E2E)
    browser testing with protractor It provides a JS wrapper around Selenium commands.
    The framework..
  _yoast_wpseo_linkdex: '56'
  _yoast_wpseo_metakeywords: browser, testing, protractor, headless, angular, non,
    driver
author:
  login: sanjaypatel2525
  email: sanjaypatel2525@gmail.com
  display_name: sanjaypatel2525
  first_name: ''
  last_name: ''
---
There are many ways to test our application but having a testing with end user feel is the always the important one. The protractor is JS framework built up Selenium JS web driver.  It provides ease of End to End (E2E) browser testing with protractor angular and non angular applications. It provides a JS wrapper around Selenium commands. The framework contains many intuitive functions which really speed up writing test cases.

** Protractor doesn't require your site to be on the Angular framework, You can use it all kind of sites.
## In this blog, we are going to cover following points.

What is Protractor and why you need it?
Setting up and running Protractor project.
Running protractor headless in non-UI Linux kind of environment.
Perks- Taking the screenshot.

<img class="alignnone size-full wp-image-252" src="{{ site.baseurl }}/assets/img_5a9774aa865b3.png" alt="" />
## What is Protractor and why you need it?
The protractor is an end to end browser test automation tool.  It emulates user like actions on browsers and is supported by many browsers (chrome, IE, firefox etc). It is a wrapper around selenium web driver commands and much more. Provides automatic wait capabilities for the resource to load and render. Here some points which make Protractor a great framework.

* It is an open source project and has big community support.
* It is well documented.
* Easy to setup and configure.
* Work with almost all the browser.
* Anytime you can take screenshots of the browser.

## Setting up and running Protractor project.
Let's jump into technicals. We are going to install and run one sample Protractor test case.

### Download and install Node JS and npm from the following URL.
<a href="https://nodejs.org/en/download/" rel="nofollow">https://nodejs.org/en/download/</a>

### Install Protractor using npm, Open shall/command prompt.
npm install -g protractor

### With above command, you must have web driver-manger command available to your console, Update web driver-managerwebdriver-manager 
update


### Start web driver-manager in the separate console.
webdriver-manager start
This required when you run you test case.
Create a file conf.js for Protractor configurations.
{% highlight java %}exports.config = {
	seleniumAddress: 'http://localhost:4444/wd/hub',
	specs: ['First-test.js'],
	allScriptsTimeout: 30000,

	// Options to be passed to Jasmine-node.
	jasmineNodeOpts: {
		showColors: true,
		defaultTimeoutInterval: 100000,
		isVerbose: true
	},
	capabilities: {
		'browserName': 'chrome',
		'chromeOptions': {
			args: [ "--headless", "--disable-gpu", "--window-size=1920x1080" ] 
		}
	}// remove headless if you want to see the action
};
{% endhighlight %}


### Create First-test.js in the same location.
This is your actual test steps. For now, you can copy paste below code. This script will open google.com and search for 'abyte.stream'
{% highlight java %}describe('First automated tests', function() {

  beforeEach(function() {
      return browser.ignoreSynchronization = true; // Important for non angular applications
    });

  it('First test', function() {
	//debugger;	 enable if you want to debug the code in chrome
	browser.driver.get('https://www.google.com');
	browser.driver.manage().window().maximize();
	browser.driver.findElement(by.id('lst-ib')).sendKeys('abyte.stream');
	browser.driver.findElement(by.name('btnK')).click();
        //expect(completedAmount.count()).toEqual(2);*/ Test any condition here which expect in the output.
  });
});{% endhighlight %}


### Run the protractor using the following command and see the protractor driving browser magic.
protractor conf.js




## Running protractor headless in non UI Linux kind of environment.
<img class="alignnone size-full wp-image-260" src="{{ site.baseurl }}/assets/img_5a98c56230888.png" alt="" />
Till this point, we have successfully achieved running test on the real browser. There are places when we do not have GUI, we just have a black screen server, In this situation, we need to go headless.

Headless browser doesn't require a graphics driver at all, They just get commands and execute them directly in memory. To achieve this you need to specify headless in cong.js under capabilities.
{% highlight json %} capabilities: { 'browserName': 'chrome', 'chromeOptions': { args: [ "--headless", "--disable-gpu", "--window-size=1920x1080" ] } }{% endhighlight %}
## Taking screenshot
{% highlight html %}<code class="lang-javascript">
browser.takeScreenshot().then(function(png) {
  var stream = fs.createWriteStream("/tmp/screenshot.png");
  stream.write(new Buffer(png, 'base64'));
  stream.end();
});
{% endhighlight %}
