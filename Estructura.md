```app
 ├── manifests
 │    └── AndroidManifest.xml
 ├── java
 │    └── com.example.tuapp
 │         ├── MainActivity.kt
 │         ├── data                        # Capa de datos
 │         │    ├── models                 # Modelos de datos
 │         │    │    └── User.kt
 │         │    └── repository             # Lógica de obtención de datos
 │         │         └── UserRepository.kt
 │         ├── ui                          # Interfaz de usuario
 │         │    ├── components             # Componentes reutilizables
 │         │    │    └── CustomButton.kt
 │         │    ├── screens                # Pantallas principales
 │         │    │    ├── HomeScreen.kt
 │         │    │    ├── DetailScreen.kt
 │         │    │    └── LoginScreen.kt
 │         │    └── theme                  # Tema de la app
 │         │         ├── Color.kt
 │         │         ├── Shape.kt
 │         │         └── Typography.kt
 │         ├── viewmodel                   # Manejo del estado con ViewModel
 │         │    └── UserViewModel.kt
 │         ├── navigation                  # Navegación entre pantallas
 │         │    └── AppNavigation.kt
 │         └── utils                       # Funciones auxiliares y constantes
 │              └── Constants.kt
 ├── res
 │    ├── drawable                         # Imágenes estáticas y vectoriales
 │    │    └── logo.png
 │    ├── mipmap                           # Íconos de la aplicación
 │    ├── values
 │    │    ├── colors.xml                  # Archivo de colores
 │    │    ├── strings.xml                 # Archivo de cadenas de texto
 │    │    └── themes.xml                  # Archivo de temas
 │    ├── xml                              # Archivos XML adicionales
 │    └── raw                              # Archivos JSON o multimedia crudos
 ├── build.gradle                          # Archivo de configuración de Gradle
```
