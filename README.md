# ViewBindingSample


```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)

    binding = ActivityMainBinding.inflate(layoutInflater)   // 바인딩 클래스의 객체 생성
    val view = binding.root                  // 바인딩 객체의 root 뷰 참조
    setContentView(view)                                    // 생성한 뷰 설정
}
```

```groovy
android {
    namespace 'com.example.viewbindingsample'
    compileSdk 33

    defaultConfig {
        applicationId "com.example.viewbindingsample"
        minSdk 26
        targetSdk 33
        versionCode 1
        versionName "1.0"

        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
    kotlinOptions {
        jvmTarget = '1.8'
    }

    buildFeatures {
        viewBinding true
    }
}
```
