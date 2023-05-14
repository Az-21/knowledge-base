# Configuration
Stuff which doesn't get checked into `git`.


## App Signature

### Key
```ps
./android/app/key.jks
```

### Key Properties
```ps
./android/key.properties
```
```r
keyAlias=key
storeFile=key.jks
keyPassword=hunter2
storePassword=hunter2
```

### Gradle Config
```ps
./android/app/build.gradle
```
```groovy
android{
  // ...
  
  signingConfigs {
    release {
      keyAlias keystoreProperties['keyAlias']
      keyPassword keystoreProperties['keyPassword']
      storeFile keystoreProperties['storeFile'] ? file(keystoreProperties['storeFile']) : null
      storePassword keystoreProperties['storePassword']
    }
  }
  
  buildTypes {
    release { 
      signingConfig signingConfigs.release
    }
  }
  
  // ...
}
```



## SDK Level
```ps
./android/local.properties
```
```r
flutter.minSdkVersion=24
flutter.targetSdkVersion=33
```
