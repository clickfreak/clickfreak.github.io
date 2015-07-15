Title: Andoid backup linux way
Date: 2015-07-15 01:31
Category: android

adb backup will write an Android-specific archive:
```
adb backup  -f myAndroidBackup.ab  com.corp.appName
```
Phone will ask you about password to encrypt backup data. Do not set password! When push right button on the phone to start backup process.

.ab archive can be converted to tar format using:
```
dd if=myAndroidBackup.ab bs=24 skip=1 | python -c "import zlib,sys;print zlib.decompress(sys.stdin.read())" > myAndroidBackup.tar
```
