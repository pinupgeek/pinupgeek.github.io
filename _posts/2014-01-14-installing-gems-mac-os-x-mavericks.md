---
layout: post
title:  "Installing Gems in Mac OS X Mavericks"
date:   2014-01-14 19:34:09
---

<img class="pull-right img-responsive" alt="Installing Gems in Mac OS X Mavericks" src="/assets/jekyll.png" />I decided to do some work with a <a title="GitHub Pages" href="http://pages.github.com/" target="_blank">GitHub Pages</a> page today. What's more, I chose to do some work with <a title="Jekyll" href="http://jekyllrb.com/" target="_blank">Jekyll</a>, since it's supported by Pages. I was having a terrible getting Jekyll installed on my MacBook Pro, so I decided I'd publish this quick post to help out anyone else who might be having the same problem.

Every time I ran the command to install Jekyll (<code>sudo gem install jekyll</code>), I kept getting this response:

`Building native extensions. This could take a while...`<br>
`ERROR: Error installing jekyll:`<br>
`ERROR: Failed to build gem native extension.`<br>
`/usr/local/rvm/rubies/ruby-1.9.3-p392/bin/ruby extconf.rb`<br>
`creating Makefile`<br>
`make`<br>
`compiling porter.c`<br>
`make: gcc-4.2: No such file or directory`<br>
`make: *** [porter.o] Error 1`<br>
`Gem files will remain installed in /usr/local/rvm/gems/ruby-1.9.3-p392/gems/fast-stemmer-1.0.2 for inspection.`<br>
`Results logged to /usr/local/rvm/gems/ruby-1.9.3-p392/gems/fast-stemmer-1.0.2/ext/gem_make.out`<br>
<h3>What's Going On?!?</h3>
Like any competent coder, I turned to Google to find out what was going on. I came across a lot of posts that said I needed to install Xcode (available through the App Store) and the command line tools (available through the Xcode preferences window). But that wasn't very helpful because I had already done those things.

The problem I was having was much more elusive.
<h3>The Hidden GCC</h3>
The real problem was right there in front of me:

<code>make: gcc-4.2: No such file or directory</code>

When I tried to install the Jekyll gem, my MacBook Pro couldn't complete my command because it couldn't find GCC.

To get this straightened out, I typed <code>which gcc</code> and found that it was installed at <code>/usr/bin/gcc</code>.

Then I just made a <strong>symlink</strong> to help out the gem installer:

<strong><code>ln -s /usr/bin/gcc /usr/bin/gcc-4.2</code></strong>

Then installing Jekyll worked just like it was supposed to.

If you're running into the same problem installing gems in Mac OS X Mavericks, this might be the issue.