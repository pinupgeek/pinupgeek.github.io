---
layout: post
title:  "Brightbox Now Offering Ruby 2.1 Ubuntu Packages"
date:   2014-01-16 12:00:00
---

<img src="/assets/ubuntu-ruby-2-1.png" alt="Ubuntu + Ruby 2.1" class="img-responsive center-block" />

As [mentioned previously](http://www.pinupgeek.com/ruby-2-1-0-released/ "Ruby 2.1.0 Released") on pinupgeek.com, Ruby 2.1 was released on Christmas Day last year (2013). Less than a month from that event, cloud hosting provider <a href="http://brightbox.com/" target="_blank">Brightbox</a> has made available Ubuntu packages for this new release.

<!--more-->

The packages are currently available for Precise, Quantal, Raring and Saucy, and Lucid is reportedly <a href="http://brightbox.com/blog/2014/01/09/ruby-2-1-ubuntu-packages/" target="_blank">on the way</a>. These packages should bring increased performance, thanks to improvements to Ruby 2.1 in general, but also due to a Brightbox-specific patch to a  <a href="https://github.com/rubygems/rubygems/issues/766" target="_blank">bug</a> in rubygems 2.2.0.

###How to `apt-get` Those Packages

If you want to grab these Ruby 2.1 packages for your own Ubuntu machine, just add Brightbox's launchpad package repository and install the `ruby2.1` package:

> `sudo apt-get install python-software-properties` <br>
> `sudo apt-add-repository ppa:brightbox/ruby-ng` <br>
> `sudo apt-get update` <br>
> `sudo apt-get install ruby2.1` <br>
> <br>
> `ruby2.1 -v` <br>
> `ruby 2.1.0p0 (2013-12-25 revision 44422) [x86_64-linux-gnu]`