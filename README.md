# Demo-Android-Ticket-Json

Can be tested through adb:
```shell
adb shell am start -a android.intent.action.VIEW -c android.intent.category.BROWSABLE -d "https://my.yavin.com/ticket/twTOukE3/"
```

# Associate the yavin link (Android 12)

Since Android 12 is required to explicitly associate the link and the application, otherwise the browser will be prioritize.<br>

In order to automatically verify the association, Android check a file hosted on yavin domain. In the file Yavin need to know:
- the package name of your application also known to be your application ID declared in the app's build.gradle file.
- The SHA256 fingerprints of your app’s signing certificate. 

You can use the following command to generate the fingerprint via the Java keytool: 
```shell
keytool -list -v -keystore <your_keystore_filename>
```

You can also ask the user to do it manually, there is an exemple implemented in this demo app:
https://github.com/YavinAPI/Demo-Android-Ticket-Json/blob/f986fc604a47a4adc7ea2c3cddfcb9aa4a74d25e/app/src/main/java/com/yavin/linker/MainActivity.kt#L48-L59
