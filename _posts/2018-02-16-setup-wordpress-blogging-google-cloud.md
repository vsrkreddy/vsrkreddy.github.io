---
layout: post
title: How to Setup Your WordPress Blogging on Google Cloud
date: 2018-02-16 23:01:04.000000000 -05:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
redirect_from:
  - /2018/02/16/setup-wordpress-blogging-google-cloud/
  - /2018/02/16/setup-wordpress-blogging-google-cloud/amp/
cardImage: Untitled4.jpg
meta:
  _edit_last: '1'
  _wp_page_template: default
  post_grid_post_settings: a:10:{s:9:"post_skin";s:4:"flat";s:19:"custom_thumb_source";s:91:"http://abyte.stream/wp-content/plugins/post-grid/assets/frontend/css/images/placeholder.png";s:17:"font_awesome_icon";s:0:"";s:23:"font_awesome_icon_color";s:7:"#737272";s:22:"font_awesome_icon_size";s:4:"50px";s:17:"custom_youtube_id";s:0:"";s:15:"custom_vimeo_id";s:0:"";s:21:"custom_dailymotion_id";s:0:"";s:14:"custom_mp3_url";s:0:"";s:20:"custom_soundcloud_id";s:0:"";}
  _the_champ_meta: a:5:{s:7:"sharing";i:0;s:16:"vertical_sharing";i:0;s:7:"counter";i:0;s:16:"vertical_counter";i:0;s:11:"fb_comments";i:0;}
  _yoast_wpseo_content_score: '60'
  _yoast_wpseo_primary_category: ''
  ampforwp_custom_content_editor: ''
  ampforwp_custom_content_editor_checkbox: ''
  ampforwp-amp-on-off: default
  _thumbnail_id: '133'
author:
  login: sanjaypatel2525
  email: sanjaypatel2525@gmail.com
  display_name: sanjaypatel2525
  first_name: ''
  last_name: ''
---
Setting up a website for your self is always exciting but just a thought of dealing with tech can be a mood off. We always want something simple and cost-effective.

Blogging can be a passion or can be a way of making some extra bucks. In this blog, I am going to talk about how easily you can setup your lightning fast blogging site up running within no time. Also, I will discuss on performance and cost of the site( It's free).

Normally, to create a WordPress website , You will have to find out a web hosting service and have to pay some amount on monthly or yearly basis to keep your services running, buy a domain name configure it with your hosting, setup PHP, MYSQL, Apache stack, install WordPress than you can start writing blog. <strong>That's it?</strong>

Luckily with growing technologies, we don't have to do all of that.
# Here is the highlight of the blog.

Few clicks setup WordPress on Google cloud
* Setup Domain name
* Setup caching and SEO - optional but highly recommended.
* Setup Cloudflare security and caching- optional but recommended.

# Setup WordPress on Google Cloud
Most of us might have a Gmail account. If you have then you already have google cloud account, Only remaining thing is setting up your billing (As per Google you will not be charged at all it is only for personal identification).
### 1. Setup billing details with Google for personal identification.
a. Open up the URL (https://console.cloud.google.com/home/dashboard). Accept the terms and conditions.
<img class="alignnone size-full wp-image-99" src="{{ site.baseurl }}/assets/img_5a8737303c219.png" alt="" />
b. Sign up for a free trial from the top right corner.
<img class="alignnone size-full wp-image-100" src="{{ site.baseurl }}/assets/img_5a8737ca9dc80.png" alt="" />
c. Fill up the billing details and card info and you are all set.

### 2. Spin up your own cloud virtual machine.
a. Hover over Compute Engine and click on VM Instance.
<img class="alignnone size-full wp-image-108" src="{{ site.baseurl }}/assets/img_5a8746463d9f1.png" alt="" />
b. Click on Create Instance from the top menu.
<img class="alignnone size-full wp-image-112" src="{{ site.baseurl }}/assets/img_5a875e003da23.png" alt="" />
Make sure you select the micro instance to keep it free and allow HTTP traffic.

Definitely, we have selected smallest configuration possible and WordPress website will be bit slow but you will see how performant and efficient it can be.  To make it optimized for this small cloud instance, please check on my another blog Optimizing WordPress for Google F1 instance.
c. Click create.

### 3. Start up Wordpress Docker containers.
a. Go to VM instances and Click on SSH next you VM.  Make sure you allow popup.
<img class="alignnone size-full wp-image-109" src="{{ site.baseurl }}/assets/img_5a8746716e390.png" alt="" />
b. Add attached files to your server via FTP software like (WinSCP, Filezilla etc.)
<a href="http://abyte.stream/wp-content/uploads/2018/02/stack.zip">default.conf, Dockerfile-nginx, stack.yml</a>
c. Run the following command on in SSH console.
docker-compose -f stack.yml up
&nbsp;
That's it your WordPress is up and running on google cloud for free. After few minutes and then you can open up your WordPress website with google external IP mentioned screen above.

### 4.Setup WordPress language and admin password.
a. Open up the external IP on browser, select default language and continue.
<img class="alignnone size-full wp-image-113" src="{{ site.baseurl }}/assets/img_5a875f28cea16.png" alt="" />
b. Enter required information.
<img class="alignnone size-full wp-image-114" src="{{ site.baseurl }}/assets/img_5a875f9fe8689.png" alt="" />
&nbsp;
This is it you are all set to create your first blog.
# What's Next
&nbsp;
Setup Domain name for no cost or almost no cost. Read my next blog on setting up domain and comparison.
