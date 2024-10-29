LIBS 28-10-2024
+++
```bash

# Define versions of various dependencies for the project, making it easier to update and manage them.
[versions]
activityComposeVersion = "1.9.3"      # Version for androidx.activity:activity-compose (Compose integration with activities).
agp = "8.7.1"                         # Android Gradle Plugin (AGP) version, essential for Android project builds.
androidxJunit = "1.7.4"               # Version for androidx.test.ext:junit, a library for Android unit testing.
appcompat = "1.7.0"                   # Version for androidx.appcompat, providing backward compatibility support.
coilCompose = "2.7.0"                 # Version for io.coil-kt:coil-compose, an image loading library for Jetpack Compose.
converterGson = "2.11.0"              # Version for converter-gson, used for JSON serialization with Retrofit.
core = "1.13.1"                       # Version for androidx.core, a set of basic libraries for Android development.
espressoCoreVersion = "3.6.1"         # Version for androidx.test.espresso:espresso-core, used for UI testing in Android.
hiltAndroid = "2.52"                  # Version for Hilt (Dagger Hilt), a dependency injection library for Android.
hiltAndroidGradlePlugin = "2.52"      # Version for Hilt's Gradle Plugin, required to use Hilt.
hiltNavigationCompose = "1.2.0"       # Version for Hilt integration with Jetpack Compose navigation.
junitVersion = "1.2.1"                # Version for androidx.test.ext:junit (JUnit library for Android).
kotlin = "2.0.10"                     # Kotlin version for the project, the main language for Android development.
coreKtx = "1.13.1"                    # Version for androidx.core:core-ktx, providing Kotlin extensions for core libraries.
junit = "4.13.2"                      # Version for junit:junit, a basic unit testing library.
espressoCore = "3.6.1"                # Version for androidx.test.espresso, another reference to Espresso for UI testing.
lifecycleRuntimeKtx = "2.8.6"         # Version for lifecycle-runtime-ktx, managing lifecycle-aware components.
activityCompose = "1.9.3"             # Version for activity-compose, specific to activity integration with Jetpack Compose.
composeBom = "2024.10.00"             # Version for BOM (Bill of Materials) of Jetpack Compose, managing Compose versions.
material = "1.12.0"                   # Version for material design library, which provides Material Design components.
materialIconsExtended = "1.7.4"       # Version for material icons in Compose.
composeMaterial3 = "1.3.0"            # Version for material3, supporting Material You components.
materialVersion = "1.7.4"             # Version for core Material Design library.
orchestrator = "1.5.1"                # Version for orchestrator, a tool for running Android tests.
retrofit = "2.11.0"                   # Version for retrofit, a type-safe HTTP client for Android.
runner = "1.6.2"                      # Version for test runner, essential for Android testing.
truth = "1.6.0"                       # Version for Truth, a library for assertion statements in testing.
ui = "1.7.4"                          # Version for Compose UI, the main UI toolkit for Compose.
uiTestManifest = "1.7.4"              # Version for UI testing manifest in Compose.
uiTooling = "1.7.4"                   # Version for Compose UI tooling, provides tools for preview and inspection.
uiToolingPreview = "1.7.4"            # Version for previewing Compose UI components.

# Define libraries to be used in the project, referencing the version numbers defined above.
[libraries]
#noinspection SimilarGradleDependency
androidx-activity-compose-v170 = { module = "androidx.activity:activity-compose", version.ref = "activityComposeVersion" } # Jetpack Compose integration for activities.
androidx-appcompat = { module = "androidx.appcompat:appcompat", version.ref = "appcompat" } # AppCompat library for backward compatibility.
androidx-core = { module = "androidx.core:core", version.ref = "core" } # Android core library.
androidx-core-ktx = { group = "androidx.core", name = "core-ktx", version.ref = "coreKtx" } # Kotlin extensions for Android core.
androidx-espresso-core-v351 = { module = "androidx.test.espresso:espresso-core", version.ref = "espressoCoreVersion" } # Espresso for UI testing.
androidx-hilt-navigation-compose = { module = "androidx.hilt:hilt-navigation-compose", version.ref = "hiltNavigationCompose" } # Hilt integration with Compose navigation.
androidx-junit = { module = "androidx.test.ext:junit", version.ref = "androidxJunit" } # JUnit library for unit tests in Android.
androidx-junit-v115 = { module = "androidx.test.ext:junit", version.ref = "junitVersion" } # JUnit testing, another version reference.
androidx-lifecycle-runtime-ktx-v260 = { module = "androidx.lifecycle:lifecycle-runtime-ktx", version.ref = "lifecycleRuntimeKtxVersion" } # Lifecycle library for lifecycle-aware components.
androidx-material = { module = "androidx.compose.material:material", version.ref = "materialVersion" } # Material Design components for Jetpack Compose.
androidx-material-icons-extended = { module = "androidx.compose.material:material-icons-extended", version.ref = "materialIconsExtended" } # Extended Material Icons for Compose.
androidx-orchestrator = { module = "androidx.test:orchestrator", version.ref = "orchestrator" } # Test orchestrator for managing Android tests.
androidx-runner = { module = "androidx.test:runner", version.ref = "runner" } # Runner for executing tests on Android.
androidx-truth = { module = "com.google.truth:truth", version.ref = "truth" } # Truth library for assertions in testing.
coil-compose = { module = "io.coil-kt:coil-compose", version.ref = "coilCompose" } # Image loading library for Compose.
converter-gson = { module = "com.squareup.retrofit2:converter-gson", version.ref = "converterGson" } # Gson converter for Retrofit.
hilt-android = { module = "com.google.dagger:hilt-android", version.ref = "hiltAndroid" } # Hilt for dependency injection.
hilt-android-compiler = { module = "com.google.dagger:hilt-android-compiler", version.ref = "hiltAndroid" } # Hilt compiler.
junit = { group = "junit", name = "junit", version.ref = "junit" } # JUnit library for unit tests.
androidx-espresso-core = { group = "androidx.test.espresso", name = "espresso-core", version.ref = "espressoCore" } # Another reference for Espresso.
material = { module = "com.google.android.material:material", version.ref = "material" } # Core Material Design library.
retrofit-core = { module = "com.squareup.retrofit2:retrofit", version.ref = "retrofit" } # Retrofit HTTP client.
dagger-hilt-compiler = { module = "com.google.dagger:hilt-compiler", version.ref = "hiltAndroid" } # Dagger Hilt compiler for dependency injection.

# Libraries for lifecycle management and Jetpack Compose UI.
androidx-lifecycle-runtime-ktx = { group = "androidx.lifecycle", name = "lifecycle-runtime-ktx", version.ref = "lifecycleRuntimeKtx" } # Lifecycle-aware components for Android.
androidx-activity-compose = { group = "androidx.activity", name = "activity-compose", version.ref = "activityCompose" } # Activity integration with Compose.
androidx-compose-bom = { group = "androidx.compose", name = "compose-bom", version.ref = "composeBom" } # BOM for managing Compose versions.
androidx-ui = { group = "androidx.compose.ui", name = "ui" } # Core UI library for Jetpack Compose.
androidx-ui-graphics = { group = "androidx.compose.ui", name = "ui-graphics" } # Compose graphics library.
androidx-ui-tooling = { group = "androidx.compose.ui", name = "ui-tooling" } # Tooling for Compose UI previews and inspection.
androidx-ui-tooling-preview = { group = "androidx.compose.ui", name = "ui-tooling-preview" } # Preview support for Compose UI.
androidx-ui-test-manifest = { group = "androidx.compose.ui", name = "ui-test-manifest" } # Manifest support for testing Compose UI.
androidx-ui-test-junit4 = { group = "androidx.compose.ui", name = "ui-test-junit4", version.ref = "androidxJunit" } # JUnit support for Compose UI testing.
androidx-material3 = { group = "androidx.compose.material3", name = "material3", version.ref = "composeMaterial3" } # Material You components for Jetpack Compose.

# Plugins for Hilt and Kotlin.
[plugins]
android-application = { id = "com.android.application", version.ref = "agp" } # Plugin for Android application projects.
kotlin-android = { id = "org.jetbrains.kotlin.android", version.ref = "kotlin" } # Plugin for Kotlin on Android.
kotlin-kapt = { id = "org.jetbrains.kotlin.kapt", version.ref = "kotlin" } # Plugin for annotation processing in Kotlin.
hilt = { id = "com.google.dagger.hilt.android", version.ref = "hiltAndroidGradlePlugin" } # Plugin for Hilt dependency injection.


```

build.gradle

```bash
plugins {
    id("com.android.application")              // Plugin for Android application projects.
    id("kotlin-android")                       // Plugin for using Kotlin in Android projects.
    id("kotlin-kapt")                          // Enables Kotlin annotation processing, useful for libraries like Hilt.
    id("com.google.dagger.hilt.android")       // Plugin for Hilt dependency injection in Android.
    id("org.jetbrains.kotlin.plugin.parcelize")// Plugin for using Parcelable in Kotlin, making object serialization easier.
    id("org.jetbrains.kotlin.plugin.compose")  // Plugin for Jetpack Compose, Kotlins UI toolkit.}

android {
    namespace = "com.example.probandoapi"      // Sets the base package namespace for the project.
    compileSdk = 34                            // Specifies the SDK level used to compile the app.

    defaultConfig {
        applicationId = "com.example.probandoapi" // Unique identifier for the application.
        minSdk = 26                                // Minimum SDK level supported by the app.
        targetSdk = 34                             // Target SDK level for which the app is optimized.
        versionCode = 1                            // Internal version code for the app.
        versionName = "1.0"                        // Version name for display purposes.

        // Configuración para Hilt
        javaCompileOptions {
            annotationProcessorOptions {
                // Disables Android superclass validation in Hilt, which can be useful for some edge cases.
                arguments.put("dagger.hilt.android.internal.disableAndroidSuperclassValidation", "true")
            }
        }
    }

    buildTypes {
        release {
            isMinifyEnabled = false                // Disables code shrinking in the release build.
            // Sets ProGuard rules for the release build.
            proguardFiles(getDefaultProguardFile("proguard-android-optimize.txt"), "proguard-rules.pro")
        }
    }

    compileOptions {
        sourceCompatibility = JavaVersion.VERSION_17   // Sets Java source compatibility to version 17.
        targetCompatibility = JavaVersion.VERSION_17   // Sets Java target compatibility to version 17.
    }

    kotlinOptions {
        jvmTarget = "17"                            // Sets JVM target to version 17 for Kotlin compilation.
    }

    buildFeatures {
        compose = true                              // Enables Jetpack Compose for building UIs.
    }

    composeOptions {
        kotlinCompilerExtensionVersion = "1.5.2"    // Specifies the version of the Kotlin Compose compiler.
    }
}

dependencies {
    implementation(libs.androidx.core.ktx)           // Core KTX library for Android extensions.
    implementation(libs.androidx.appcompat)          // AppCompat library for backward compatibility.
    implementation(libs.material)                    // Material Design components library.
    implementation(libs.ui)                          // Core UI toolkit for Jetpack Compose.
    implementation(libs.androidx.material3)          // Material 3 components for Jetpack Compose.
    implementation(libs.ui.tooling.preview)          // Preview tools for Compose UI.
    debugImplementation(libs.ui.tooling)             // Tooling library for debugging in Compose.
    debugImplementation(libs.ui.test.manifest)       // Manifest tool for UI testing in Compose.
    implementation(libs.androidx.lifecycle.runtime.ktx.v260) // Lifecycle-aware components.
    implementation(libs.androidx.activity.compose.v170) // Activity integration with Compose.

    // Hilt para inyección de dependencias
    implementation(libs.hilt.android)                // Hilt library for dependency injection.
    kapt(libs.hilt.android.compiler)                 // Compiler for Hilt annotation processing.
    implementation(libs.androidx.hilt.navigation.compose) // Hilt navigation integration for Compose.

    // Dependencias de prueba (opcional)
    testImplementation(libs.junit)                   // JUnit library for unit testing.
    androidTestImplementation(libs.androidx.junit.v115)  // AndroidX JUnit extension for Android testing.
    androidTestImplementation(libs.androidx.espresso.core.v351) // Espresso library for UI testing.
    androidTestImplementation(libs.androidx.ui.test.junit4) // JUnit testing library for Compose UI.

    // Retrofit y Gson (asegúrate de que estas referencias están definidas en libs.versions.toml)
    implementation(libs.retrofit.core)               // Retrofit library for HTTP networking.
    implementation(libs.converter.gson)              // Gson converter for Retrofit, for JSON serialization.

    // Coil
    implementation(libs.coil.compose)                // Coil library for image loading in Jetpack Compose.

    // Hilt Compiler desde el catálogo
    kapt(libs.hilt.compiler)                         // Hilt compiler from version catalog.
}

kapt {
    correctErrorTypes = true                         // Allows kapt to ignore certain error types.
}



```


build.gradle
```bash

// build.gradle.kts de nivel de proyecto
buildscript {
    dependencies {
        // Agrega el plugin de Hilt para la inyección de dependencias.
        classpath("com.google.dagger:hilt-android-gradle-plugin:2.52")
    }
}

// Archivo de configuración de nivel superior donde puedes añadir opciones de configuración
// comunes a todos los subproyectos/módulos.
plugins {
    // Plugin para aplicaciones de Android, con una versión específica, pero no se aplica aquí directamente.
    id("com.android.application") version "8.7.1" apply false
    
    // Plugin para utilizar Kotlin en proyectos de Android.
    id("org.jetbrains.kotlin.android") version "2.0.0" apply false
    
    // Plugin de Hilt para la inyección de dependencias en Android.
    id("com.google.dagger.hilt.android") version "2.52" apply false
    
    // Plugin para habilitar Jetpack Compose, el kit de herramientas de UI declarativo de Kotlin.
    id("org.jetbrains.compose") version "1.6.11" apply false // Cambia la versión si es necesario
    
    // Plugin adicional para Jetpack Compose, para soportar nuevas funcionalidades de Compose en Kotlin.
    id("org.jetbrains.kotlin.plugin.compose") version "2.0.0" apply false
}



```
