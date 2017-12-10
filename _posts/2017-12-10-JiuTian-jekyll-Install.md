---
layout:     post
title:      Jekyll Install
subtitle:   Using jekyll to make a blog
date:       2017-12-10
author:     BY syuukawa
header-img: img/post-bg-hacker.jpg
catalog: true
tags:
    - Jekyll
---


## Foreword
	 Some software or plug-in should be install 
	 
	 ruby version >= 2.0
	 
	 bundler
	 
	 jekyll

## Main
*******************Reference***************************************
https://www.cnblogs.com/huochaihe/p/7575012.html
https://segmentfault.com/a/1190000007243257
http://blog.csdn.net/daxiangqqcom/article/details/78329496?locationNum=8&fps=1
*******************Reference***************************************

*******************1:::Ruby Install***************************************
**********************************************************************
Install Dependencies
**********************************************************************

yum -y groupinstall "Development Tools"

yum -y install gdbm-devel libdb4-devel libffi-devel libyaml libyaml-devel ncurses-devel openssl-devel readline-devel tcl-devel

**********************************************************************
Download and Build Ruby from Source
**********************************************************************
mkdir -p rpmbuild/{BUILD,BUILDROOT,RPMS,SOURCES,SPECS,SRPMS}

wget http://cache.ruby-lang.org/pub/ruby/2.2/ruby-2.2.3.tar.gz -P rpmbuild/SOURCES

wget https://raw.githubusercontent.com/tjinjin/automate-ruby-rpm/master/ruby22x.spec -P rpmbuild/SPECS

rpmbuild -bb rpmbuild/SPECS/ruby22x.spec

yum -y localinstall rpmbuild/RPMS/x86_64/ruby-2.2.3-1.el7.centos.x86_64.rpm

********************************************************************
Test the Install
********************************************************************
ruby -v
gem -v

Error11111
 centos7 redis requires Ruby version >= 2.2.2	 	

*******************2:::Ruby Change Version***************************************
centos7 redis requires Ruby version >= 2.2.2
http://blog.csdn.net/daxiangqqcom/article/details/78329496?locationNum=8&fps=1	
*******************2:::Ruby Change Version***************************************

*******************3:::Ruby Change Version***************************************

Error22222
[root@192 myblog]# jekyll serve
/usr/local/rvm/rubies/ruby-2.3.4/lib/ruby/site_ruby/2.3.0/rubygems/core_ext/kernel_require.rb:55:in `require': cannot load such file -- bundler (LoadError)
	from /usr/local/rvm/rubies/ruby-2.3.4/lib/ruby/site_ruby/2.3.0/rubygems/core_ext/kernel_require.rb:55:in `require'
	from /usr/local/rvm/gems/ruby-2.3.4/gems/jekyll-3.6.2/lib/jekyll/plugin_manager.rb:48:in `require_from_bundler'
	from /usr/local/rvm/gems/ruby-2.3.4/gems/jekyll-3.6.2/exe/jekyll:11:in `<top (required)>'
	from /usr/local/rvm/gems/ruby-2.3.4/bin/jekyll:23:in `load'
	from /usr/local/rvm/gems/ruby-2.3.4/bin/jekyll:23:in `<main>'
	from /usr/local/rvm/gems/ruby-2.3.4/bin/ruby_executable_hooks:15:in `eval'
	from /usr/local/rvm/gems/ruby-2.3.4/bin/ruby_executable_hooks:15:in `<main>'

**********************3:::install bundler********************************************** 
https://segmentfault.com/a/1190000007243257
Jekyll搭建个人博客
**********************3:::install bundler**********************************************

Success
[root@192 myblog]# jekyll serve
Configuration file: /root/myblog/_config.yml
            Source: /root/myblog
       Destination: /root/myblog/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.499 seconds.
 Auto-regeneration: enabled for '/root/myblog'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
  
  
## Epilogue

   Be not afraid of life . Believe that life is worth living . and your belief will help create the fact.
                                                              ------William James , Is Life Worth Living 


