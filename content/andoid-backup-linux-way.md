Title: Andoid backup linux way
Date: 2015-07-15 01:31
Category: android

adb backup will write an Android-specific archive:
```
adb backup  -f myAndroidBackup.ab  com.corp.appName
```

Phone will ask you about password to encrypt backup data.

This archive can be converted to tar format using:
```
dd if=myAndroidBackup.ab  bs=1 skip=24|openssl zlib -d > myAndroidBackup.tar
```
