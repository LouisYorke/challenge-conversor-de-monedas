# Currency Converter - Java API Client

Este proyecto es un cliente de consola desarrollado en **Java** para la conversión de divisas en tiempo real. Fue diseñado como parte del programa **Oracle Next Education (ONE)**, aplicando principios de Programación Orientada a Objetos (POO) e integración con servicios REST externos.

---

## Stack Tecnológico

* **Lenguaje:** Java 17+
* **Librerías:** [Google GSON](https://github.com/google/gson) para el procesamiento de archivos JSON.
* **API Externa:** [ExchangeRate-API](https://www.exchangerate-api.com/) (Tasas de cambio actualizadas).

---

## Funcionalidades

* **Conversión Dinámica:** Consulta de tasas de cambio en tiempo real para múltiples divisas.
* **Historial de Sesión:** Registro detallado de las operaciones realizadas durante la ejecución.
* **Gestión de Excepciones:** Robustez ante fallos de conexión, errores de API o entradas de usuario no válidas.
* **Seguridad:** Implementación de archivos de configuración externos para proteger credenciales.

---

## Estructura del Proyecto

```text
src/
├── main/
│   ├── java/
│   │   ├── ConversorApp.java       # Clase principal (Entry point)
│   │   ├── models/                 # Records y clases de datos
│   │   ├── services/               # Lógica de consumo de API y cálculos
│   │   └── util/                   # Gestión de configuración y utilidades
│   └── resources/
│       └── config.properties       # Archivo de configuración (Ignorado en Git)

```

---

## Instalación y Configuración

1. Clonar el repositorio
Bash
git clone [https://github.com/aquilescb/conversor_de_monedas](https://github.com/aquilescb/conversor_de_monedas)
cd conversor_de_monedas
2. Obtener API Key
Regístrate en ExchangeRate-API para obtener una clave gratuita.

En la carpeta src, crea un archivo llamado config.properties.

Agrega tu clave privada:

Properties
API_KEY=tu_clave_aqui
3. Configurar Dependencias (GSON)
Si utilizas IntelliJ IDEA sin un gestor de dependencias (Maven/Gradle):

Descarga el archivo .jar desde el Repositorio Central de MVN.

Ve a File > Project Structure > Modules > Dependencies.

Haz clic en el botón + > JARs or Directories y selecciona el archivo .jar descargado.

Aplica los cambios.

---

## Ejecución
Desde tu IDE (como IntelliJ IDEA o Eclipse):

Asegúrate de que el archivo config.properties esté accesible en el classpath.

Ejecuta la clase ConversorApp.java.

Si prefieres la línea de comandos:

Bash
javac -cp "lib/gson-2.10.1.jar" src/ConversorApp.java
java -cp "src:lib/gson-2.10.1.jar" ConversorApp
