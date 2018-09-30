# CIS362atMSU
This is a collection of apps for CIS362, Mobile App Development at Missouri State University

## Getting started

Each of the apps built in this repository were created in Android Studio for the Missouri State University (MSU) Mobile App Development class during the fall of 2018.

Android Studio for these began with version 3.1, and ended with version 3.2 (so far! note - finalize at project end)

There is just zero guarantee these will work with anything else at all. Honestly, there are no guarantees here anything will work at all!

## Developing

You are welcome to do whatever you would like with this collection of code. The great majority of it was taken directly from the textbook and modified to run with the (then) latest version of Android Studio.

```shell
<TextView
        android:layout_width="wrap_content"
        android:text="Hello World!"
         />
```

This repository uses productFlavors to differentiate the apps into versions, all within the same code project.

```shell
    flavorDimensions "version"
    productFlavors {
        hellogoodbye {
            dimension "version"
            applicationId "com.tobyziegler.android.hellogoodbye"
            versionNameSuffix "-hellogoodbye"
        }
```

The app/build.gradle file is modified with added flavorDimensions and a productFlavor for each app.

```shell
    buildTypes {
        debug {
            productFlavors.hellogoodbye.buildConfigField "String", "flavor", "\"hellogoodbye\""
            ...etc.
            }
```
Each flavor gets a debug buildType,

```shell
        release {
            productFlavors.hellogoodbye.buildConfigField "String", "flavor", "\"hellogoodbye\""
            ...etc.
            }
```
and a release buildType.

Viola!

## Android Studio Apps

The app flavors in this repository include:
* HelloGoodbye
* BurgerCalorieCounter
* Calculator
* Paintings
* ActivityLifeCycle
* AutomotiveCalculator

More will be added until the conclusion of the semester.

## Contributing

I truly do not expect any contributions to this repository. The whole thing is only here to store and track my progress in a single class at school.

If this helps anyone else, that's just a massive bonus. Meanwhile, browse or branch or download to your heart's content.

## Links

These are the basic links to source material for the course:
- Android Developer Site: http://developer.android.com/
- Repository: http://github.com/MacZiegler/CIS362atMSU
- MSU Home: http://www.missouristate.edu/
  - All reasonable efforts have been taken to comply with the Missouri State University Academic Integrity Policy: http://www.missouristate.edu/policy/Op3_01_AcademicIntegrityStudents.htm
  
  I used [Jesse Luoto's](https://github.com/jehna) awesome readme [best practices project](https://github.com/jehna/readme-best-practices) as the basis/template for this readme, so thanks [Jesse](https://github.com/jehna)!
- Readme file inspired by: https://github.com/jehna/readme-best-practices/blob/master/README-default.md

I ended up using productFlavors to separate the apps but keep them all in the same repository. I found the idea in basically two places:
-from codeAddiction: https://codeaddiction.net/articles/58/multiple-apps-in-one-android-studio-project
-and from Stepstone Tech: https://medium.com/stepstone-tech/how-to-build-17-apps-with-a-single-android-project-and-not-go-crazy-91d025adf0f0

It turns out their instructions were a tad outdated and caused a flavorDimensions error. Fixed with the advice from:
-Android Developers Configure Build Variants: https://developer.android.com/studio/build/build-variants?utm_source=android-studio#product-flavors

## Licensing

Does this need licensing? I would like to list it as something like:

"The code in this project is licensed under MIT license."

...but I am just not sure whether I should or whether it is necessary or even whether it has some sort of prohibition.
