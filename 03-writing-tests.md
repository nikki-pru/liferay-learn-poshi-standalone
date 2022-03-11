# Writing tests

Let's get started with writing your first Poshi test!

## Prerequisites

1. Java JDK 8

1. [Git](https://docs.github.com/en/get-started/quickstart/create-a-repo)

1. [Gradle](https://gradle.org/install/) or [Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html#sec:adding_wrapper) 6.6.1 or higher.

## Setup

1. Create a new directory. For this tutorial we will name it `poshi-standalone`.

1. Setup Gradle wrapper (6.6.1 +) in the newly created directory.
  ```
  $ gradle wrapper
  ```

  Your directory should now contain the following:
  ```
  poshi-standalone
  ├── .gradle
  ├── gradle   
  ├── └── wrapper
  |       ├──  gradle-wrapper.jar
  |       └──  gradle-wrapper.properties
  ├── gradlew
  └── gradlew.bat
  ```

1. Setup version control (git) in the directory.

1. To create the necessary files to use Poshi Standalone, run the following command from the desired directory in a terminal/command line window:

  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/liferay/liferay-portal/master/modules/test/poshi/poshi-standalone/setup.sh)"
  ```

  Your directory should now contain the following

  ```
  poshi-standalone
  ├── .gradle
  ├── gradle   
  ├── gradle   
  ├── └── wrapper
  |       ├──  gradle-wrapper.jar
  |       └──  gradle-wrapper.properties
  ├── build.gradle
  ├── gradlew
  ├── gradlew.bat
  ├── poshi.properties
  ├── poshi-ext.properties
  └── settings.gradle
  ```

## Planning your test

Let's setup a test case that we would like to automate. Say we would like to assert that searching for blue vanilla cupcakes on Google yields results that show recipes for blue vanilla cupcakes. The steps we would take would be:

1. Navigate to http://google.com.

1. Enter  `blue vanilla cupcakes` into the search bar.

1. Assert that the results display the header **Recipes**.


## Defining page objects

Now, let's locate and name the elements we need to interact with.


### Create the *.path file
1. On a browser, navigate to http://google.com.

1. Open the Web Developer Tools for your browser (F12).