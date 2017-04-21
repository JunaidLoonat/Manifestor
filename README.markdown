# 1. Name
Manifestor - Android Manifest.xml tool

# 2. Author
Saurabh Harit < saurabh(at)sensepost(dot)com >

# 3. License, version & release date
License : GPLv3  
Version : v0.1  
Release Date : 2011/11/01

# 4. Description
Android applications may share the data of a content provider with other applications installed on your device. For example, if you receive an image attachment in an email, your mail client will have to share it with an image viewer. One way of sharing a content provider's data with other applications is by using "grant-uri-permission" tag in AndroidManifest.xml. Using this tag, a content provider can specify a path, path pattern or path prefix. However, if this path is mistakenly set to "/", any other installed application would be able to access data of that content provider.
< grant-uri-permission android:pathPrefix="/"  />
Manifestor.py extracts AndroidManifest.xml from an Android application package (.apk), decodes it and scans it for such permission flaws. As an output, it will display you the set path and whether or not it could be vulnerable.

# 5. Usage
Options:

    -h, --help            show this help message and exit

    -o OUTPUTDIR, --output-dir=OUTPUTDIR
          Output directory to use. This path will be used to
          download the apk files to your machine

    -a APKS, --apk=APKS   Path (on Android device) of APK(s) to scan. Example:
          /system/app/Gmail.apk. If the value of this switch is
          set to scan_all, the script will automatically scan
          all apks in /system/app and /system/sd/app folder

    -l LOCALFILES, --local=LOCALFILES
          Path (on the local machine) to APK(s).

    -A APKPATHS, --apkpath=APKPATHS
          Path (on Android device) to search for APK(s) to scan.
          Example: /system/app

As input, it accepts an apk file path or a folder name on your phone. If you have apk files on your local machine, you can use "-l" switch. "-o" switch lets you specify the folder where the apk files will be downloaded and saved from you android device. If this switch is not specified, the files are saved in the current folder.

# 6. Requirements
Python

# 7. Additional Resources
Slides, Outsmarting Smartphones - http://www.slideshare.net/sensepost/outsmarting-smartphones
