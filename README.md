# mapBoxAndroidReactNative


git clone project

cd ./project


npm install


for Run:

change file
./android/app/build.gradle

dependencies{
  - compile project(':mapbox-react-native-mapbox-gl')
  + compile (project(':mapbox-react-native-mapbox-gl')) {
  +      compile ('com.squareup.okhttp3:okhttp:3.6.0') {
  +          force = true
  +      }
  + }
}

change file
./android/build.gradle
ext {
        ...
        - buildToolsVersion = "27.0.3"
        - compileSdkVersion = 27
        + buildToolsVersion = "26.0.3"
        + compileSdkVersion = 26
        ...
    }



the first run:
react-native run-android

then:
change file
./android/build.gradle
ext {
        ...
        - buildToolsVersion = "26.0.3"
        - compileSdkVersion = 26
        + buildToolsVersion = "27.0.3"
        + compileSdkVersion = 27 
        ...
    }
    

The second run:
react-native run-android
