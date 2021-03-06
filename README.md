# Assesment Model - Kotlin Native
This repo contains Sage Bionetwork's exploritory work to build a cross-platform assesment model using Kotlin Native.
The MPP code can be found inside the [assessmentModel/](assessmentModel/) directory while
sample app implementations can be found inside the [androidApp/](androidApp/) resp. [iosApp/](iosApp/) dir.

More information on Kotlin native can be found in [multiplatform documentation](http://kotlinlang.org/docs/reference/building-mpp-with-gradle.html).

## iOS

To compile the project from Xcode just open `iosApp/iosApp.xcodeproj` and run the application.
The [swift tests](iosApp/iosAppTests/iosAppTests.swift) also can be executed from Xcode.

To compile a framework for ios simulator from the command line execute:

```
  > ./gradlew :assessmentModel:build
```

To compile the framework for a device use the `device` project property:

```
  > ./gradlew :assessmentModel:build -Pdevice=true
```

To run kotlin tests (including the [common ones](greeting/src/commonTest/kotlin/CalculatorTest.kt))
on an iOS simulator execute:

```
  > ./gradlew :assessmentModel:iosTest
```

By default the `iPhone 8` simulator is used. One can change this setting using the `iosDevice` project property:

```
  > ./gradlew :assessmentModel:iosTest -PiosDevice='iPhone 7'
```


## Android

The application can be built and executed on a device or emulator using Android Studio 3.2 or higher.
One can also compile the application and run tests from the command line:

```
   > ./gradlew :androidApp:build
```
