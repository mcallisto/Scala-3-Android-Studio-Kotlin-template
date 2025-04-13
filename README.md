# Android Studio project with a Scala 3 module

A template project for the latest **Android Studio** with an added **Scala 3** module.

## Aim

Helping the adoption of Scala in Android Studio.

This is the project you get if:

1. in **Android Studio** Android Studio _Meerkat | 2024.3.1 Patch 1_ you choose from menu:

    `New` > `New Project…` > `Empty Activity` (template for Phone and Tablet)

2. you then add a minimal Scala 3.7.0-RC2 module named `core` and call it from the `app` module

3. you use [STTP](https://github.com/softwaremill/sttp) to query [ScalaDex](https://index.scala-lang.org/)
and display the results. Credits and big thanks for this to [@keynmol](https://github.com/keynmol)

## Notes

### Why Scala 3.7.0?

Because is the first Scala version shipping https://github.com/scala/scala3/pull/22632.
The emitted Scala code is more compatible with Android ART.

Since currently all Scala libraries are not yet published to Maven Central with this version,
the workaround is to let Android R8 minify the code,
so `minifyEnabled true` must be set even for `debug` builds.

### What about a Java-only template?

Android Studio is currently quite opinionated towards Kotlin,
so a Java module is not an option you get straight from the `New` > `New Project…` menu.

If you want the same project starting from the Java-only template,
please check https://github.com/mcallisto/Scala-3-Android-Studio-Java-template.
