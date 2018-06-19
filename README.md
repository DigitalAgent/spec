# DigitalAgent Project Specification

![revision](https://img.shields.io/badge/revision-0.1-lightgrey.svg)
![license](https://img.shields.io/badge/license-MIT-green.svg)


This document serves as the current specification of DigitalAgent, a suite of applications and services for auditing and securing one's devices, accounts, and other aspects of digital identity.


### Standard Client Features

* Filesystem - Scan / clean junk files (temp, logs, installers, etc.)
* Browsers - Clear browser data (cache, history, etc.)
* Services - Manage running processes and service states (auto, manual, disabled)
* Networks - Monitor and audit local network connections (WLAN, WWAN, Bluetooth)
* Scan Engine - definitions updated regularly (e.g. weekly) via GZIP compressed download
* App Info - Display information about currently installed applications such as publisher, data usage, potential vulnerabilities or battery-draining performance issues, rating info, etc (via realtime API)
* Scheduler - Enable or disable network interfaces and other services or devices on a set schedule
* Custom Profiles - Energy saving, high performance, ultra-secure for public networks, etc.


### Additional Mobile Features

	
* Advanced Security Profiles - disable device features (GPS, Radio) based on filters such as location, time, and more
* Kill Switch - Disable GPS, Radio etc. using gestures and/or easy-access control panel


### API Overview / Server Application Features

    
* One-way hash of phone # for authentication, can be revoked at any time. Utilizes SMS service to verify phone number and establish an authenticated state
* The account created in the manner above, along with any stored profiles, settings, or other data, can be wiped instantly at any time, and can be set to auto-delete upon X failed attempts to authenticate, with the default being 10
* Fully anonymized client reporting of metrics such as clean logs, application and system behavior, and other highly useful information (All data MUST be reported in explicit structures and formats and care MUST be taken to ensure that no personally identifiable information is ever stored or mishandled)
* Social Profile Auditing - Review social media content on the most popular social networks (top 2 or 3 to start) and perform admin operations such as batch downloading photos, deleting unwanted content, unfollowing groups, and identifying potential phishing scams, fake content, and other potential threats
* Saved Profiles - Security profiles can be stored via API and are keyed from the ID associated with the one-way-hash


### Target Platforms

* Windows
* Mac OSX
* Linux RPM/DEB
* Android
* iOS
* ???


### Technology Overview
    
* Production API - .NET Core / C# 6 / Mono
* Production DB - PostgreSQL / SQLite3
* Production AI - C++14 / Python / TensorFlow
* Utility APIs - Node JS / .NET Core / Other
* Client Engines, Services, IPC, etc - C++11 / Boost
* Mobile UX API Adapters - Java / Obj-C / Swift
* Core UX - React Native (all targets)

#### Client-Side Stack

![Client-Side Architecture](https://raw.githubusercontent.com/DigitalAgent/spec/master/client-architecture.xml "Logo Title Text 1")
