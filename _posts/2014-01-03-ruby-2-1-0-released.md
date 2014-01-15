---
layout: post
title:  "Ruby 2.1.0 is released"
date:   2014-01-03 10:34:09
---

As per tradition, the newest MRI Ruby release (<a href="https://www.ruby-lang.org/en/news/2013/12/25/ruby-2-1-0-is-released/" target="_blank">2.1.0</a>) came out on Christmas Day. The new release has been met with praise of its performance increases thanks to the new <a href="http://www.infoq.com/news/2013/12/ruby21" target="_blank">RGenGC</a> generational <a href="http://www.i-programmer.info/news/98-languages/6807-ruby-21-with-better-garbage-collection.html" target="_blank">garbage collector</a> and improved method caching.

Other notable changes include

<!--more-->

<ul>
	<li>refinements <a href="https://bugs.ruby-lang.org/issues/8481" target="_blank">#8481</a> <a href="https://bugs.ruby-lang.org/issues/8571" target="_blank">#8571</a></li>
	<li>syntax changes
<ul>
	<li>Rational/Complex Literal <a href="https://bugs.ruby-lang.org/issues/8430" target="_blank">#8430</a></li>
	<li>def’s return value <a href="https://bugs.ruby-lang.org/issues/3753" target="_blank">#3753</a></li>
</ul>
</li>
	<li>Bignum
<ul>
	<li>use GMP <a href="https://bugs.ruby-lang.org/issues/8796" target="_blank">#8796</a></li>
</ul>
</li>
	<li>String#scrub <a href="https://bugs.ruby-lang.org/issues/8414" target="_blank">#8414</a></li>
	<li>Socket.getifaddrs <a href="https://bugs.ruby-lang.org/issues/8368" target="_blank">#8368</a></li>
	<li>RDoc 4.1.0 and RubyGems 2.2.0</li>
	<li>“literal”.freeze is now optimized <a href="https://bugs.ruby-lang.org/issues/9042" target="_blank">#9042</a></li>
	<li>add Exception#cause <a href="https://bugs.ruby-lang.org/issues/8257" target="_blank">#8257</a></li>
	<li>update libraries like BigDecimal, JSON, NKF, Rake, RubyGems, and RDoc</li>
	<li>remove curses <a href="https://bugs.ruby-lang.org/issues/8584" target="_blank">#8584</a></li>
</ul>
For more info <a href="http://www.ruby-lang.org/en/news/2013/12/25/ruby-2-1-0-is-released/" target="_blank">click here to check out the official announcement.</a>