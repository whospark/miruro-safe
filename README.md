# Miruro Safe (Android WebView wrapper)

A minimal Android Studio project for loading `https://www.miruro.cx/` in a WebView.

## Security choices
- HTTPS-only (cleartext disabled; mixed content blocked)
- Main-frame navigation limited to `miruro.cx` and its subdomains
- WebView Safe Browsing enabled; unsafe hits are sent back to safety
- No camera, microphone, location, contacts, SMS, storage, or notification permissions declared
- WebView file/content access disabled
- Third-party cookies disabled
- Pop-up windows blocked
- WebView debugging disabled
- Downloads are not automatically handled

## Build
1. Install Android Studio and open this folder (`MiruroSafe`).
2. Allow Gradle sync; install Android SDK 35 if prompted.
3. Use **Build > Build APK(s)**.
4. Install the generated debug APK on your own Android device.


## Limitations / important
This wrapper does not make the site trustworthy or remove the site's own ads/scripts. Embedded media providers may not work because main-frame navigation is restricted to Miruro domains. Do not loosen the allowlist unless you have independently verified the destination. The project is source code; it has not been built or security-audited here.

