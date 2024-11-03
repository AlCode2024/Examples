Resumen de API

```Bash

Resumen de la Arquitectura:

UI: Compuesta con Jetpack Compose, donde los datos provienen
 del ViewModel y se actualizan automáticamente cuando cambian.

ViewModel: Administra los datos y su estado para la UI, 
obteniéndolos del repositorio y asegurando que sobrevivan a cambios de configuración.

Repositorio: Proporciona la lógica de acceso a los datos. 
Llama a la API a través de Retrofit y devuelve los resultados al ViewModel.

Retrofit y API Service: Define cómo se estructuran y envían las solicitudes HTTP. 
Realiza las solicitudes de manera eficiente y convierte las respuestas JSON en objetos de Kotlin.

Hilt: Simplifica la creación y provisión de dependencias como Retrofit, 
el repositorio y el ViewModel.

Paging: Mejora el rendimiento al dividir los datos en partes manejables, 
cargándolos solo cuando el usuario los necesita.


```
```Bash

# Arquitectura de Aplicación con API usando Retrofit

| **Capa**              | **Implementaciones necesarias**                                                                                          | **Ejemplo de Código o Explicación**                                                                                 |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **UI**                | - **Jetpack Compose**: Construir la interfaz de usuario de forma declarativa.                                             | ```kotlin\n@Composable\nfun GameListScreen(viewModel: GameViewModel) {\n    val games = viewModel.games.collectAsState()\n    LazyColumn {\n        items(games.value) { game ->\n            Text(game.name)\n        }\n    }\n}\n```  |
|                       | - **Coil (o Glide)**: Cargar y mostrar imágenes desde URLs de la API en la UI.                                            | ```kotlin\nImage(\npainter = rememberImagePainter(data = game.imageUrl),\ncontentDescription = null\n)\n```  |
|                       | - **LiveData/StateFlow**: Observar los datos proporcionados por el `ViewModel`.                                           | ```kotlin\nval games by viewModel.games.observeAsState()\n```                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **ViewModel**         | - **ViewModel (de Jetpack)**: Gestionar la lógica de la interfaz de usuario y los datos en la UI.                         | ```kotlin\nclass GameViewModel @Inject constructor(private val repository: GameRepository) : ViewModel() {\n    val games = repository.getGames()\n}\n```  |
|                       | - **LiveData/StateFlow**: Exponer los datos al `UI` de forma reactiva.                                                    | ```kotlin\nval games = MutableLiveData<List<Game>>()\n```                                                           |
|                       | - **Hilt**: Para la inyección de dependencias, facilitando la inyección del `Repository`.                                 | ```kotlin\n@HiltViewModel\nclass GameViewModel @Inject constructor(...) : ViewModel() {}\n```                       |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Repository**        | - **Retrofit**: Realizar las solicitudes HTTP a la API y manejar las respuestas.                                         | ```kotlin\nclass GameRepository @Inject constructor(private val api: ApiService) {\n    suspend fun getGames() = api.getGames()\n}\n```  |
|                       | - **Coroutines (Kotlin)**: Realizar operaciones de red de forma asincrónica y evitar bloquear el hilo de la UI.           | ```kotlin\nsuspend fun getGames() = withContext(Dispatchers.IO) { api.getGames() }\n```                             |
|                       | - **Room (opcional)**: Almacenar datos localmente, si se requiere caché de datos.                                        | ```kotlin\n@Dao\ninterface GameDao {\n    @Query("SELECT * FROM games")\n    fun getAllGames(): List<Game>\n}\n```  |
|                       | - **DAO (Data Access Object, en caso de usar Room)**: Interactuar con la base de datos local.                             | ```kotlin\n@Insert\nfun insertGame(game: Game)\n```                                                                 |
|                       | - **Hilt**: Inyectar dependencias como Retrofit o DAO, si se utiliza Room.                                               | ```kotlin\nclass GameRepository @Inject constructor(private val api: ApiService, private val dao: GameDao) {}\n```  |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Retrofit Interface**| - **Retrofit Annotations**: `@GET`, `@POST`, `@Query`, `@Path`, para definir los endpoints de la API.                    | ```kotlin\ninterface ApiService {\n    @GET("games")\n    suspend fun getGames(): Response<List<Game>>\n}\n```       |
|                       | - **Data Models**: Clases de datos que representan las respuestas de la API.                                             | ```kotlin\ndata class Game(val id: Int, val name: String)\n```                                                      |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **API Server**        | - **API Backend**: El servidor debe estar configurado para recibir y responder a las solicitudes.                        | Servidor debe tener endpoints como `/games`, `/game/{id}`, etc., configurados para devolver datos en JSON.           |
|                       | - **Endpoints**: Definidos en el servidor para los recursos específicos (por ejemplo, `/games`, `/game/{id}`).           | **Ejemplo de Endpoint**: `https://api.example.com/games?key=API_KEY`                                                |


```
