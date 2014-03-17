Recents Settings (recents.io)
================

This is the default settings file for recents the Mac status bar application, if you would like to add a type of project to this please submit a pull request and we will package it with future releases.

Keep in mind, a user can edit their own file and so this file is only added on install or if they delete their current settings.

### Currently supported project types

- Mixture
- Node
- Grunt
- Wordpress
- Statamic
- Laravel
- Grails
- Android
- Brightscript
- Autotools

__This list should be updated as new projects are added to the default json__

### Explanation of settings for adding new project types:


__projectType__
Lower case name of the project type - must be unique

__nameRegex__
The regex that will pull the project name out of the settings file - if this fails then enclosing folder name will be used. Should be in Objective C Regex format.

__settingsFile__
The filename (or path) to the settings file from the root of the project

__image__
The project image file (see other images in this repo for sizing and file format)

__keyFile__
The name of the key file to search for to find this project - doesn't have to be unique but is required ensure the project will be indexed

__projectRootRelativeToKeyFile__
null if the keyFile is in the project root or as many ../ as needed to move up to the root of the project

__filesExistInRoot__
A whitelist of files that must ALL exist in the root for the project to be shown.  Do not use an extension if you want to find with or without extension

__ignoreIfFilesInRoot__
A blacklist of files - if ANY are found then the project will not be shown for this project type

__ignoreIfPathContains__
If this string appears in the filepath it will not be shown for this project type

__button etc__
null will not show the button.  Auto layout is not yet perfected so buttons don't yet resize properly - this will be added soon.  You can add an array of apps that Recents should try and open - if it's not on the system then it will move to the next one and finally try the default

