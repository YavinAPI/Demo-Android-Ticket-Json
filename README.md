# Demo-Android-Ticket-Json

Can be tested through adb:
```shell
adb shell am start -a android.intent.action.VIEW -c android.intent.category.BROWSABLE -d "https://my.yavin.com/ticket/twTOukE3/"
```

# Associate the yavin link

Since Android 12 is required to explicitly associate the link and the application, otherwise the browser will be prioritize.<br>
For now you need to do it manually:<br>
https://developer.android.com/training/app-links/verify-site-associations#make-request

There is an exemple implemented in this demo app:
https://github.com/YavinAPI/Demo-Android-Ticket-Json/blob/f986fc604a47a4adc7ea2c3cddfcb9aa4a74d25e/app/src/main/java/com/yavin/linker/MainActivity.kt#L48-L59
