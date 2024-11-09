Estos archivos funcionan entre si

LIBS
```bash
# Define versions of various dependencies for the project, making it easier to update and manage them.
[versions]
activityCompose = "1.9.3"
agp = "8.6.1"
androidxJunit = "1.2.1"
appcompat = "1.7.0"
coilCompose = "2.7.0"
converterGson = "2.11.0"
core = "1.15.0"
espressoCore = "3.6.1"
hiltAndroid = "2.52"
hiltAndroidGradlePlugin = "2.52"
hiltNavigationCompose = "1.2.0"
junit = "4.13.2"
kotlin = "2.0.21"
lifecycleRuntimeKtx = "2.8.7"
composeBom = "2024.10.01"
material = "1.12.0"
materialIconsExtended = "1.7.5"
composeMaterial3 = "1.3.1"
orchestrator = "1.5.1"
retrofit = "2.11.0"
runner = "1.6.2"
truth = "1.6.0"
ui = "1.7.5"

# Define libraries to be used in the project, referencing the version numbers defined above.
[libraries]
androidx-activity-compose-v170 = { module = "androidx.activity:activity-compose", version.ref = "activityCompose" }
androidx-appcompat = { module = "androidx.appcompat:appcompat", version.ref = "appcompat" }
androidcorelibrary = { module = "androidx.core:core", version.ref = "core" }
corektx = { group = "androidx.core", name = "core-ktx", version.ref = "core" }
androidx-espresso-core-v351 = { module = "androidx.test.espresso:espresso-core", version.ref = "espressoCore" }
androidx-hilt-navigation-compose = { module = "androidx.hilt:hilt-navigation-compose", version.ref = "hiltNavigationCompose" }
androidx-junit = { module = "androidx.test.ext:junit", version.ref = "androidxJunit" }
testjunit4 = { module = "androidx.test.ext:junit", version.ref = "androidxJunit" }
androidx-lifecycle-runtime-ktx-v260 = { module = "androidx.lifecycle:lifecycle-runtime-ktx", version.ref = "lifecycleRuntimeKtx" }
androidx-material = { module = "androidx.compose.material:material", version.ref = "material" }
androidx-material-icons-extended = { module = "androidx.compose.material:material-icons-extended", version.ref = "materialIconsExtended" }
androidx-orchestrator = { module = "androidx.test:orchestrator", version.ref = "orchestrator" }
androidx-runner = { module = "androidx.test:runner", version.ref = "runner" }
androidx-truth = { module = "com.google.truth:truth", version.ref = "truth" }
coil-compose = { module = "io.coil-kt:coil-compose", version.ref = "coilCompose" }
converter-gson = { module = "com.squareup.retrofit2:converter-gson", version.ref = "converterGson" }
hilt-android = { module = "com.google.dagger:hilt-android", version.ref = "hiltAndroid" }
hilt-android-compiler = { module = "com.google.dagger:hilt-compiler", version.ref = "hiltAndroid" }
junit = { group = "junit", name = "junit", version.ref = "junit" }
material = { module = "com.google.android.material:material", version.ref = "material" }
retrofit-core = { module = "com.squareup.retrofit2:retrofit", version.ref = "retrofit" }

# Libraries for lifecycle management and Jetpack Compose UI.
androidx-compose-bom = { group = "androidx.compose", name = "compose-bom", version.ref = "composeBom" }
previewtfc = { module = "androidx.compose.ui:ui-tooling-preview", version.ref = "ui" } # Preview tools for Compose UI.
androidx-ui-tooling = { module = "androidx.compose.ui:ui-tooling", version.ref = "ui" } # Tooling for debugging in Compose.
androidx-ui-test-manifest = { module = "androidx.compose.ui:ui-test-manifest", version.ref = "ui" } # Manifest tool for UI testing in Compose.
androidx-ui = { group = "androidx.compose.ui", name = "ui" }
androidx-ui-graphics = { group = "androidx.compose.ui", name = "ui-graphics" }
androidx-ui-test-junit4 = { group = "androidx.compose.ui", name = "ui-test-junit4", version.ref = "androidxJunit" }
androidx-material3 = { group = "androidx.compose.material3", name = "material3", version.ref = "composeMaterial3" }

# Plugins for Hilt and Kotlin.
[plugins]
android-application = { id = "com.android.application", version.ref = "agp" }
kotlin-android = { id = "org.jetbrains.kotlin.android", version.ref = "kotlin" }
kotlin-kapt = { id = "org.jetbrains.kotlin.kapt", version.ref = "kotlin" }
hilt = { id = "com.google.dagger.hilt.android", version.ref = "hiltAndroidGradlePlugin" }





```
