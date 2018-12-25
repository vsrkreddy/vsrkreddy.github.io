---
layout: post
title: Spring Boot - Quick Overview
date: 2018-10-11 02:52:39.000000000 -04:00
type: post
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
meta:
  _edit_last: '1'
  _wp_page_template: default
  post_grid_post_settings: a:10:{s:9:"post_skin";s:4:"flat";s:19:"custom_thumb_source";s:91:"http://35.229.62.76/wp-content/plugins/post-grid/assets/frontend/css/images/placeholder.png";s:17:"font_awesome_icon";s:0:"";s:23:"font_awesome_icon_color";s:7:"#737272";s:22:"font_awesome_icon_size";s:4:"50px";s:17:"custom_youtube_id";s:0:"";s:15:"custom_vimeo_id";s:0:"";s:21:"custom_dailymotion_id";s:0:"";s:14:"custom_mp3_url";s:0:"";s:20:"custom_soundcloud_id";s:0:"";}
  _wp_old_slug: hello-world
author:
  login: velma
  email: shivaram.velma777@gmail.com
  display_name: velma
  first_name: ''
  last_name: ''
---
## Goals  
 
1. Enable building production ready applications quickly. 
1.  Provide common non - functionality features like embedded servers (tomcat, jetty), metrics, health checks, external configurations 
 
## Features: 

1.  Quickly create spring applications with auto configurations. Quick Starters like web logging etc.. 
1.  Embedded Server  - package tomcat in application jar and deploy the application. 
1.  Monitoring - spring boot actuator - how many time services is called, failed etc. 
 
 Before spring boot we have to decide all the dependencies and the versions as well problem is there might be a comparability issues. There would be lot of configurations like dispatcher servlet , view resolver etc with out spring boot. 
## Steps to create quick the spring boot project ( Opinionated)  
 go to start.spring.io - <a href="https://start.spring.io/" target="_blank" rel="noopener">Click Here..</a> 
 Group name - package name, Artifact - Project name, add dependencies necessary ( web, actuator, thyme leaf, security so on..) 
 Download the zip, unzip it and import to IDE( eclipse, spring ts). Click on Spring Application and run it. Quick and simple indeed! 
 Spring boot looks at frameworks available on CLASS PATH, existing configurations for application, based on this Spring boot provides basic configuration needed to configure the application with these frameworks. 
## What is Spring boot Auto Configurations  
 
1.  @SpringBootApplication - indicates that this is## spring context  file.## enables auto configuration, enables component scan  (scan this package and sub packages) 
1.   SpringApplication.run(Main.class, args) Method- takes in spring context , returns application context, Application Context will have all the beans configured.   
 
