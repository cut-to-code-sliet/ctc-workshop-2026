# CTC App Development Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: App Dev Basics & Kotlin Fundamentals (22 Sep 2026)](#session-1-app-dev-basics--kotlin-fundamentals-22-sep-2026)

---

## Session 1: App Dev Basics & Kotlin Fundamentals (22 Sep 2026)

### Topics Covered

#### 1. What is App Development? (10 min)
- **What is an Android app?** A program built to run on Android devices, with a UI the user interacts with directly on their phone/tablet (as opposed to a website loaded in a browser).
- **Native vs cross-platform:**
  - **Native**: built specifically for one platform using its own language/toolkit (e.g. Kotlin for Android, Swift for iOS). Best performance and full access to platform features.
  - **Cross-platform**: one codebase targeting multiple platforms (e.g. Flutter, React Native). Faster to build for both Android and iOS, but sometimes trades off performance or native feel.
- **Why Kotlin + Android Studio + Jetpack Compose:** Kotlin is Google's recommended language for Android — concise and modern. Android Studio is the official IDE. Jetpack Compose is the modern, declarative way to build Android UIs (as opposed to the older XML-based layout system).

**Classes and Objects (brief)**
- A **class** is a blueprint (e.g. `Car`) describing properties and behavior.
- An **object** is a specific instance created from that blueprint (e.g. `myHondaCity`).

**OOPs vs POOP**
- **OOP (Object-Oriented Programming)**: organizing code around classes and objects (encapsulation, inheritance, polymorphism, abstraction).
- **POP (Procedural-Oriented Programming)**: organizing code as a sequence of steps/functions acting on data, without bundling data and behavior together into objects.

#### 2. Kotlin Basics Needed for Android
- **`val` vs `var`**
  - `val` → read-only, cannot be reassigned once set (like `final` in Java).
  - `var` → mutable, can be reassigned.
```kotlin
  val name = "Aryan"   // cannot change later
  var score = 10       // can change later
  score = 20            // OK
```
- **Data types**: `Int`, `Double`, `Float`, `Boolean`, `String`, `Char`, etc. Kotlin infers types automatically, but they can also be declared explicitly.
```kotlin
  val age: Int = 20
  val price: Double = 99.99
  val isActive: Boolean = true
```
- **Functions**: declared with `fun`, can take parameters and return values.
```kotlin
  fun greet(name: String): String {
      return "Hello, $name!"
  }
```

---

### Homework
Read the following official Kotlin docs:
1. [Hello World (Kotlin Tour)](https://kotlinlang.org/docs/kotlin-tour-hello-world.html)
2. [Basic Types (Kotlin Tour)](https://kotlinlang.org/docs/kotlin-tour-basic-types.html)
3. [Control Flow (Kotlin Tour)](https://kotlinlang.org/docs/kotlin-tour-control-flow.html)
4. [Collections (Kotlin Tour)](https://kotlinlang.org/docs/kotlin-tour-collections.html)