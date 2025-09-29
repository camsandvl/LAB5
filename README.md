# LAB 5 - Pokédex con Retrofit y Jetpack Compose

## Descripción
Este proyecto es una aplicación de Android que consume el API pública de [PokeAPI](https://pokeapi.co/) utilizando **Retrofit**.  
El objetivo es practicar permisos, acceso a internet y repaso de conceptos previos como **UI con Jetpack Compose** y **Navegación**.

La aplicación muestra:

1. Una **lista de los primeros 100 Pokémon**, obtenidos desde el endpoint de la API.  
2. Una segunda pantalla con **4 imágenes diferentes del Pokémon seleccionado** (frente, espalda, frente shiny y espalda shiny).

La interfaz es muy simple y sigue el ejemplo mostrado en el laboratorio.

---

## Tecnologías usadas
- **Kotlin**
- **Jetpack Compose** para la interfaz
- **Navigation Compose** para navegación entre pantallas
- **Retrofit2 + Gson** para consumir el API
- **Coil** para mostrar imágenes
- **ViewModel + LiveData/State** para manejo del estado

---

## Estructura del proyecto
- `MainActivity.kt`: Punto de entrada de la app y configuración de la navegación.
- `ListScreen.kt`: Pantalla que muestra el listado de los 100 Pokémon.
- `DetailScreen.kt`: Pantalla que muestra las 4 imágenes del Pokémon seleccionado.
- `PokeApi.kt`: Definición de la interfaz de Retrofit para acceder a la PokeAPI.
- `MainViewModel.kt` y `DetailViewModel.kt`: Lógica para obtener y manejar datos desde la API.
- `ui/theme/`: Archivos básicos de tema y colores generados por Android Studio.

---

## Cómo ejecutar
1. Clonar este repositorio en Android Studio.
2. Asegurarse de tener configurado **Java 17** en el proyecto.
3. Conectarse a internet (la app necesita acceder a la API).
4. Ejecutar la aplicación en un emulador o dispositivo físico con Android 7.0 (API 24) o superior.

---

## Funcionamiento
- Al abrir la aplicación, se carga automáticamente la lista de los primeros 100 Pokémon desde `https://pokeapi.co/api/v2/pokemon?limit=100`.
- Al tocar un Pokémon de la lista, se navega a la pantalla de detalle.
- La pantalla de detalle muestra 4 imágenes del mismo Pokémon:  
  - Frente normal  
  - Espalda normal  
  - Frente shiny  
  - Espalda shiny  

---
