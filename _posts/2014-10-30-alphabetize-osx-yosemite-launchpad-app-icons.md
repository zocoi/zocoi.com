---
title: Alphabetize OSX Yosemite launchpad app icons
layout: post
date: '2014-10-30 09:57:26 -0700'
type: post
parent_id: 0
published: true
status: publish
categories:
- Misc
meta:
  publicize_twitter_url: http://t.co/oe6Y4PE7sx
  _wpas_done_6901007: 1
  publicize_linkedin_url: ''
  _wpas_done_6901009: 1
  geo_latitude: 37.7550619
  geo_longitude: -122.3983993
  geo_address: Potrero Hill, San Francisco, CA, USA
  geo_public: ''
  publicize_twitter_user: zocoi
  _publicize_done_external: a:1:{s:8:"facebook";a:1:{i:560224923;b:1;}}
  _wpas_done_1907398: 1
  _rest_api_client_id: -1
  _wpas_skip_google_plus: 1
  _wpas_skip_tumblr: 1
  _wpas_skip_path: 1
  _rest_api_published: 1
  _publicize_pending: 1
  publicize_facebook_url: https://facebook.com/10152914267544924
author:
  login: mephis1987
  email: mephis1987@gmail.com
  display_name: Hung Dao
  first_name: ''
  last_name: ''
---

I don't use Launchpad as often since the new Spotlight search is fast and convenient. But I would love to have an organized launchpad. Here is the easiest way to reset it to default settings.

Run this in Terminal:

```
defaults write com.apple.dock ResetLaunchPad -bool true; killall Dock
```
