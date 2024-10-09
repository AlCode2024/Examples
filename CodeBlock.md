# Probado bloques de codigo con boton para copiar

#### Función para filtrar usuarios mediante una edad minima, se considera mayor o igual.
```kotlin
fun mostrarUsuariosPorEdad(minEdad: Int) {
    val usuariosFiltrados = usuarios.filter { it.edad >= minEdad }.sortedBy { it.edad }
    if (usuariosFiltrados.isNotEmpty()) {
        println("----- Usuarios con edad igual o mayor a $minEdad años -----")
        for (usuario in usuariosFiltrados) {
            usuario.mostrarDatos()
        }
    } else {
        println("No hay usuarios con edad igual o mayor a $minEdad años.")
    }
}
```
___

```kotlin
fun mostrarUsuariosPorEdad(minEdad: Int) {
    val usuariosFiltrados = usuarios.filter { it.edad >= minEdad }.sortedBy { it.edad }
    if (usuariosFiltrados.isNotEmpty()) {
        println("----- Usuarios con edad igual o mayor a $minEdad años -----")
        for (usuario in usuariosFiltrados) {
            usuario.mostrarDatos()
        }
    } else {
        println("No hay usuarios con edad igual o mayor a $minEdad años.")
    }
}
```
#Crear un boton usando JetPack Compose.

```kotlin
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.material3.*
import androidx.compose.runtime.Composable
import androidx.compose.ui.Modifier
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.platform.LocalContext
import androidx.compose.ui.text.font.FontWeight
import androidx.compose.ui.unit.sp
import androidx.compose.ui.graphics.Color

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            MyApp {
                MyButton()
            }
        }
    }
}

@Composable
fun MyApp(content: @Composable () -> Unit) {
    MaterialTheme {
        Surface(
            modifier = Modifier.fillMaxSize(),
            color = MaterialTheme.colorScheme.background
        ) {
            content()
        }
    }
}

@Composable
fun MyButton() {
    Button(onClick = {
        println("¡Botón presionado!")
    }) {
        Text("Presionar", fontSize = 18.sp, fontWeight = FontWeight.Bold, color = Color.White)
    }
}

@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
    MyApp {
        MyButton()
    }
}
```


Probando, todo esto es parte de un resumen para genererar apps de forma mas dinamica.

```Kotlin
@Composable
fun MyButton() {
    Button(onClick = {
        println("¡Botón presionado!")
    }) {
        Text("Presionar", fontSize = 18.sp, fontWeight = FontWeight.Bold, color = Color.White)
    }
}
```
