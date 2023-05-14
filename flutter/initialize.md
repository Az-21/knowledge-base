# Initialize

## Project
```ps
flutter create --platforms=android,windows --org az21 appname
```

**Note** Don't use uppercase char in orgnization name or app name.

## App Name
```ps
./android/app/src/main/AndroidManifest.xml
```
```r
android:label="appname"
```


## Icon
```ps
# Place icon here
./assets/icon/icon.png
```

```yaml
# pubspec.yaml
dev_dependencies:
  flutter_launcher_icons: <latest>

flutter_launcher_icons:
  android: "launcher_icon"
  image_path: "assets/icon/icon.png"
```

```ps
# Run command in root
dart run flutter_launcher_icons
```
