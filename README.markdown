<p align="center">
 <img src="https://github.com/iamtheblackunicorn/Ignotus/raw/main/android/app/src/main/res/mipmap-xxxhdpi/ic_launcher.png" width=350/>
</p>

# IGNOTUS :shushing_face:

*a simple guessing game written in Dart for Android and Mac OSX*

## ABOUT :books:

Having heard about the "awesomeness" of Dart and Flutter I decided to try my hand at some development and write a small game in Dart using Flutter. A guessing game!
Ignotus is the result of this experiment.

## BUILDING :hammer:

### Preparation

Please install the following tools:

- Android Studio
- Xcode (for a Mac OSX build)
- Java JDK
- Make
- Git
- Flutter

After having done this, run `flutter doctor` to see that everything is available for making a build.
Next, clone this repository! You could open up a terminal and run `make build_android`, however, you need to tell Flutter which certificates to use to sign the app.
To tell Flutter which certificates to use, we need to generate some first!

To do this, run this command on Mac OSX and Linux:

```bash
$ keytool -genkey -v -keystore key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
```
or if you are on Windows, run this instead:

```bash
keytool -genkey -v -keystore key.jks -storetype JKS -keyalg RSA -keysize 2048 -validity 10000 -alias key
```
If that was successful, fill out the fields for the keystore password in `android/app/key.properties` with the password you just used and place the file `key.jks`
into `android/app/`. Now, you can safely build a release APK!

### Final steps for Android

- Run `flutter pub get`.
- Run `make build_android`.

### Final steps for Mac OSX

- Run `make build_macosx`.

## DOWNLOAD :inbox_tray:

- GitHub releases: [DOWNLOAD](https://github.com/iamtheblackunicorn/Ignotus/releases) :joystick:

## NOTE :scroll:

- Ignotus by Alexander Abraham a.k.a *The Black Unicorn*
- licensed under the MIT license
