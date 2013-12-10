# About
"Prototype" is an easy to use HTML5 Mobile App generator that will (hopefully) make my life easier. Craft and share clickable prototypes in no time with others accross various platforms (iOS, Android, Windows Phone 8)

## Why
* Building a clickable prototype accross multiple platforms, takes time
* It often requires programming skills
* Sharing such a prototype can be complicated
* ...accross multiple platforms even more!
* Imho there is not such a thing already existing for your mobile phone / tablet.

## Technology
* Native Distribution using Cordova Phonegap
* Sencha Touch 2 Framework

# Project Setup

## Prerequisites

* Install Sencha Touch 2 SDK
* Install Sencha CMD
* Install GIT
* Setup local Webserver
* Cordova CMD

## Project Setup

### Git Project
```bash
mkdir Prototype
cd Prototype
git init
touch README.md
git add .
```

_GIT REPO Erstellen_

```bash
git commit -m "first commit"
git remote add origin git@github.com:chrigu-ebert/app-prototype.git
git push -u origin master
```

### Phonegap Setup
```bash
cd ..
cordova create Prototype be.chrigu.prototype "App Prototype Generator"
cd Prototype
cordova platform add ios
```

### Sencha Touch 2 Setup
```bash
rm -rf www/*
cd www
sencha upgrade
curl http://cdn.sencha.com/touch/sencha-touch-2.3.1-gpl.zip -o st2.zip
unzip st2.zip
sencha -sdk ./touch-2.3.1 generate app Prototype .
rm -rf st2.zip touch-2.3.1
```
