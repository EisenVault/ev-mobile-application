# ev-mobile-application
Project containing mobile app

Steps for publishing the app after doing changes - You can check the same in Shared Google Drive : Dev and Setup Guide --> Development --> AndroidAppDocument.docx

Android App Document

Software Requirements:

1.ZipAlign

2.SignApk

3.apktool SDK

4. ZipSigner ( Mobile Application    )

Steps to decompile/Recompile apk using apktool

1. Execute apktool.exe from cmd and follow the above commands for decompile and recompile

Decompile:

for windows

apktool d test.apk 

for linux

java -jar apktool.jar d eisen_app.apk

Recompile:

for windows

apktool b <folder_name> 

for Linux

java -jar apktool.jar b eisen_app.apk //check this as it is not working

2. ZipSigner (Mobile App) Not working in my mobile, need to have some other android phone to 

use this app

Save Recompiled  apk into Mobile and launch ZipSigner 

a. Select input as input.apk and output path for signed apk

b. select Certificate  and generate the key

c. sign the file

3. Signing apk with SignApk 

command

java -jar signapk.jar certificate.pem key.pk8 infile.apk outfile.apk

copy the certificate and key from already generated certificate and key and change their 

name. This is not working as the certificate has expired. To generate new certificate using  

android studio and then perform these steps.

here infile.apk is the file created by zipsigner

here outfile.apk is the file created after signing

 

4. Using Zipaligner

zipalign  4 infile.apk outfile.apk

here infile.apk is the file created  by SignApk

here outfile.apk is the file created after aligning

The outfile.apk is the file that will be published on play store

Publish app on google playstore

Playstore Link

https://play.google.com/apps/publish/?dev_acc=10573564872885444575

Apk Segments

Store Listing:

Contains information regarding Product Details, graphics assets etc

Content Rating:

General rating for your App
