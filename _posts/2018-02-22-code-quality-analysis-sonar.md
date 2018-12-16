---
layout: post
title: Code Quality analysis with Sonar
date: 2018-02-22 19:16:58.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
meta:
  _edit_last: '1'
  _thumbnail_id: '179'
  _wp_page_template: default
  post_grid_post_settings: a:10:{s:9:"post_skin";s:4:"flat";s:19:"custom_thumb_source";s:92:"https://abyte.stream/wp-content/plugins/post-grid/assets/frontend/css/images/placeholder.png";s:17:"font_awesome_icon";s:0:"";s:23:"font_awesome_icon_color";s:7:"#737272";s:22:"font_awesome_icon_size";s:4:"50px";s:17:"custom_youtube_id";s:0:"";s:15:"custom_vimeo_id";s:0:"";s:21:"custom_dailymotion_id";s:0:"";s:14:"custom_mp3_url";s:0:"";s:20:"custom_soundcloud_id";s:0:"";}
  _the_champ_meta: a:5:{s:7:"sharing";i:0;s:16:"vertical_sharing";i:0;s:7:"counter";i:0;s:16:"vertical_counter";i:0;s:11:"fb_comments";i:0;}
  _yoast_wpseo_content_score: '60'
  _yoast_wpseo_primary_category: ''
  ampforwp_custom_content_editor: ''
  ampforwp_custom_content_editor_checkbox: ''
  ampforwp-amp-on-off: default
  _yoast_wpseo_focuskw_text_input: Code Quality analysis with Sonar - Sanjay Patel
    blogs
  _yoast_wpseo_focuskw: Code Quality analysis with Sonar - Sanjay Patel blogs
  _yoast_wpseo_linkdex: '62'
  _yoast_wpseo_metakeywords: sonar, Code quality, code,, quality, sonar scanner, sonar-scanner,
    sonar qube, sonarqube
  _yoast_wpseo_metadesc: This article describes step by step to setup sonarqube in
    your local environment and run the reports. Project with or without maven/gradle
    can be configure for code quality analysis with sonarqube and sonar scanner.
author:
  login: sanjaypatel2525
  email: sanjaypatel2525@gmail.com
  display_name: sanjaypatel2525
  first_name: ''
  last_name: ''
---
Every software starts with a good documentation and good code. Whenever a team starts a project are there different minds working on the same thing and sometimes this leads to differences in coding standards. To overcome this problem there are many standalone tools, which can go through your code and depending on configured rules in that tool. It gives lines of code which under coding rules violation.

There are many code quality tools in java such as,

* CheckStyle
* Firebugs
* PMD

Actually, sonar is the combination of all these, That's the reason I prefer Sonar over the individual tool. Moreover, it has code coverage plugin as well Cobertura which is quite decent.
<h1>Steps to install Sonar and Sonar-Scanner.</h1>


### Install required version of JRE.
https://docs.sonarqube.org/display/SONAR/Requirements

### Download latest Sonar form following link.
https://www.sonarqube.org/downloads/

### Read licensing and stuff (Completely optional, The current version is licensed under LGPL v3 )
https://softwareengineering.stackexchange.com/questions/47323/can-i-use-an-lgpl-licenced-library-in-my-commercial-app

### Install Sonar Scanner (It's a replacement for Sonar runner). If you are using maven and  gradle then it's not required.
https://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner

### Extract both the zips on one location as shown below.
<img class="alignnone size-full wp-image-176" src="{{ site.baseurl }}/assets/img_5a8efabed2852.png" alt="" />


### Let Sonar-scanner know  Sonarqube URL (Optional, If you haven't updated the port or URL).
sonar-scanner\conf\sonar-scanner.properties --&gt; Update the sonar.host.url
Add Sonar-scanner\bin path to your system and verify by running sonar-scanner.bat -h in the console.

### Spin up the Sonarqube server by running StartSonar.bat from Sonarqube bin directory and verify if it has come properly or not by going to the browser.
localhost:9000
click tutorial and make a note of the generated key.

### Create sonar-project.properties in the root of the project which you want to scan.
<b>sonar-project.properties</b>
{% highlight properties %}
# must be unique in a given SonarQube instance
sonar.projectKey=my:project
# this is the name and version displayed in the SonarQube UI. Was mandatory prior to SonarQube 6.1.
sonar.projectName=My project
sonar.projectVersion=1.0
# Path is relative to the sonar-project.properties file. Replace "\" by "/" on Windows.
# This property is optional if sonar.modules is set. 
sonar.sources=.
# Encoding of the source code. Default is default system encoding
#sonar.sourceEncoding=UTF-8
{% endhighlight %}


### Run solar-scanner command from the root of your project.


### In case you are not using maven or gradle you might face the following issue.
<img class="alignnone size-full wp-image-177" src="{{ site.baseurl }}/assets/img_5a8f039d217de.png" alt="" />
Just add a follwoing line in sonar-project.properties.

sonar.java.binaries=&lt;replace with your binaries path. bin\**\*.class&gt; #path of your class files.

### Once you get 'Execution Success'. Revisit your localhost:9000.
<img class="alignnone size-full wp-image-181 " src="{{ site.baseurl }}/assets/img_5a8f182662166.png" alt="" />


That's setup is complete, You can browse through the site and find out the easy.
