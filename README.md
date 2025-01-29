# ObjectDetectionLiveFeedKotlinComplete
 kotlin practice app

```
app/
├── build.gradle                 # App level build configuration
├── src/
│   ├── main/
│   │   ├── AndroidManifest.xml # App permissions and components declaration
│   │   ├── assets/
│   │   │   ├── labelmap.txt    # Labels for object detection classes
│   │   │   └── mobilenet.tflite # TensorFlow Lite model file
│   │   ├── java/
│   │   │   └── com.example.objectdetectionlivefeed/
│   │   │       ├── MainActivity.kt   # Entry point of the app
│   │   │       ├── ML/
│   │   │       │   └── Classifier.kt # Model interface and inference
│   │   │       ├── Drawing/
│   │   │       │   ├── BorderedText.kt      # Text rendering for labels
│   │   │       │   ├── MultiBoxTracker.kt   # Tracking detection boxes
│   │   │       │   └── OverlayView.kt       # Drawing detection overlay
│   │   │       └── LiveFeed/
│   │   │           ├── AutoFitTextureView.kt          # Camera preview scaling
│   │   │           ├── CameraConnectionFragment.kt     # Camera handling
│   │   │           └── ImageUtils.kt                   # Image processing utilities
│   │   └── res/
│   │       ├── drawable/
│   │       │   ├── ic_launcher_background.xml
│   │       │   └── ic_launcher_foreground.xml
│   │       ├── layout/
│   │       │   ├── activity_main.xml        # Main activity layout
│   │       │   └── camera_fragment.xml      # Camera preview layout
│   │       ├── values/
│   │       │   ├── colors.xml
│   │       │   └── strings.xml
│   │       └── mipmap/                      # App icons
│   └── test/                                # Unit tests
│       └── java/
│           └── com.example.objectdetectionlivefeed/
│               └── ExampleUnitTest.kt
└── proguard-rules.pro                       # ProGuard configuration

# Key Dependencies in build.gradle
dependencies {
    // TensorFlow Lite
    implementation 'org.tensorflow:tensorflow-lite:2.x.x'
    implementation 'org.tensorflow:tensorflow-lite-support:0.x.x'
    
    // CameraX (Optional - for modern camera implementation)
    implementation 'androidx.camera:camera-core:1.x.x'
    implementation 'androidx.camera:camera-camera2:1.x.x'
    implementation 'androidx.camera:camera-lifecycle:1.x.x'
    
    // Other standard Android dependencies
    implementation 'androidx.core:core-ktx:1.x.x'
    implementation 'androidx.appcompat:appcompat:1.x.x'
    implementation 'com.google.android.material:material:1.x.x'
}

# Required Permissions in AndroidManifest.xml
<uses-permission android:name="android.permission.CAMERA" />
<uses-feature android:name="android.hardware.camera" />
<uses-feature android:name="android.hardware.camera.autofocus" />
```