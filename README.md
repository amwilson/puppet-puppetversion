####Table of Contents

1. [Overview](#overview)
2. [Module Description - What is the puppetversion module?](#module-description)
3. [Setup - The basics of getting started with puppetversion](#setup)
    * [What puppetversion affects](#what-puppetversion-affects)
    * [Setup requirements](#setup-requirements)
    * [Beginning with puppetversion](#beginning-with-puppetversion)
4. [Usage - Configuration options and additional functionality](#usage)
5. [Reference - An under-the-hood peek at what the module is doing and how](#reference)
5. [Limitations - OS compatibility, etc.](#limitations)
6. [Development - Guide for contributing to the module](#development)

##Overview

$$$$$$$$$$$$$$

[![Build
Status](https://secure.travis-ci.org/opentable/puppet-puppetversion.png)](https://secure.travis-ci.org/opentable/puppet-puppetversion.png)

##Module Description

$$$$$$$$$$$$$$

##Setup

###What puppetversion affects

*


###Beginning with homes

To create a new local user:

```puppet
   puppetversion { 'version 3.4.3':
     version => '3.4.3'
   }
```

##Usage

###Classes and Defined Types

####Class: `puppetversion`
The puppetversion module guides the upgrade of puppet.

**Parameters within `puppetversion`:**
#####`version`
The version that you want to upgrade to


##Reference

$$$$$$$$$$$$$$$

##Limitations

This module is tested on the following platforms:

* CentOS 5
* CentOS 6
* Ubuntu 10.04.4
* Ubuntu 12.04.2
* Ubuntu 13.10

It is tested with the OSS version of Puppet only.

##Development

###Contributing

Please read CONTRIBUTING.md for full details on contributing to this project.

###Running tests

This project contains tests for both [rspec-puppet](http://rspec-puppet.com/) and [beaker](https://github.com/puppetlabs/beaker) to verify functionality. For in-depth information please see their respective documentation.

Quickstart:

    gem install bundler
    bundle install
    bundle exec rake spec
	BEAKER_DEBUG=yes bundle exec rspec spec/acceptance

