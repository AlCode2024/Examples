```com
 └── tuapp
      ├── assets
      │    └── sample_data.json              # JSON de datos de prueba o simulación
      ├── res
      │    ├── drawable                      # Imágenes estáticas y vectoriales
      │    │    ├── logo.png
      │    │    ├── background.jpg
      │    │    └── icon.xml                 # Imagen vectorial
      │    └── raw                           # JSON de configuración u otros datos estáticos
      │         └── config_data.json
      ├── data                               # Capa de datos
      │    ├── models                        # Modelos de datos
      │    │    └── User.kt
      │    └── repository                    # Lógica de obtención de datos
      │         └── UserRepository.kt
      ├── ui                                 # Interfaz de usuario
      │    ├── components                    # Componentes reutilizables
      │    │    └── CustomButton.kt
      │    ├── screens                       # Pantallas principales
      │    │    ├── HomeScreen.kt
      │    │    ├── DetailScreen.kt
      │    │    └── LoginScreen.kt
      │    ├── theme                         # Tema de la app (colores, tipografías, formas)
      │    │    ├── Color.kt
      │    │    ├── Shape.kt
      │    │    └── Typography.kt
      ├── viewmodel                          # Manejo del estado con ViewModel
      │    └── UserViewModel.kt
      ├── navigation                         # Navegación entre pantallas
      │    └── AppNavigation.kt
      └── utils                              # Funciones auxiliares y constantes
           └── Constants.kt```
