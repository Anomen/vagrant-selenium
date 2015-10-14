# vagrant-selenium
Vagrant configuration base on ubuntu/trusty64, ready to be used with Selenium.

## Introduction

Selenium allows you to automate tests in Web Browsers. To do so, you need to have selenium webdriver installed for all the browsers that you want to run your test into.

## Installation

1. Install [Vagrant](https://www.vagrantup.com)
2. Clone this git repository
3. run `git submodule init` from within your checkout directory
4. run `git submodule update` from within your checkout directory
5. Run the command `vagrant up`

This vagrant works for *Virtualbox*, on a 64 bits machine.

## Browser support

- Firefox (latest version)
- Google Chrome (latest version)

The script also installs the latest version of selenium server, and google chrome webdriver.

## Why a VM for Selenium?

Installing selenium server and the webdrivers are easy on a machine. However, everytime that you want to run your tests, it opens the browser on top of the other windows, preventing you from doing something else. Unless you use phantomjs, it is not possible to run Chrome or Firefox hidden, without disturbing you on your work.

Thanks to this VM, you only need to start the VM, and all your tests will be run into the VM. You can continue developping in the meanwhile!

## How does it work?

When the VM starts, it automatically runs selenium server, along with the google-chrome webdriver. **You need to wait a few minutes** before running your tests.

On your host machine, you can send the tests on this address: **localhost:4444**, just as if you installed selenium on your host machine.

## How to access the host from the guest machine?

An alias already exists for your convenience: *http://host/* will target your host machine.
