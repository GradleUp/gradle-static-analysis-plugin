Change Log
==========

Version 1.3
-----------

- First release under new group name. The plugin is now available under 
`com.gradleup.static-analysis` plugin id and published in jCenter and Gradle Plugin Portal.
- Package names are changed according to the new repository
- Findbugs support is completely removed in order to support Gradle 6

### Migration

For more modern plugins approach

```groovy
plugins {

    // Replace 
    id 'com.novoda.static-analysis' version '1.2'
    
    // With
    id 'com.gradleup.static-analysis' version '1.3'
}
```

For classpath dependency approach:

```groovy
// Replace
buildscript {
    // ...
    dependencies {
        classpath 'com.novoda:gradle-static-analysis-plugin:1.2'
    }
}

apply plugin: 'com.novoda.static-analysis'

// With:
buildscript {
    // ...
    dependencies {
        classpath("com.gradleup:static-analysis-plugin:1.3")
    }
}

apply plugin: 'com.gradleup.static-analysis'
```

Older Versions
-------------

Please refer to Novoda's repository for versions older than 1.2: https://github.com/novoda/gradle-static-analysis-plugin/blob/master/CHANGELOG.md
