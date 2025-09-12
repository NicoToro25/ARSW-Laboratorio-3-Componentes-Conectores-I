# Arquitecturas de Software (ARSW) - Laboratorio #3

## Componentes y conectores - Parte I.

#### Nicolás Toro

[![Java](https://img.shields.io/badge/Java-17%2B-blue.svg)](https://www.oracle.com/java/)
[![Maven](https://img.shields.io/badge/Maven-Build-brightgreen.svg)](https://maven.apache.org/)

---

En este laboratorio se mostró cómo, en una arquitectura de software, los componentes encapsulan responsabilidades y los 
conectores permiten que interactúen de manera desacoplada, flexible y extensible.

El objetivo principal es entender y experimentar como funciona una arquitectura donde se implementan componentes y conectores.

[Laboratorio 3](https://github.com/ARSW-ECI-archive/SpringBoot_REST_API_Blueprints)

## Estructura del laboratorio

```bash
.
.
├── ejercicio-previo/                          # Ejercicio introductorio con Spring
│   ├── img/                                   # Evidencias gráficas
│   ├── src/
│   │   └── main/
│   │       ├── java/
│   │       │   └── edu/eci/arsw/springdemo/ui/  # Ejemplo de inyección de dependencias con Spring
│   │       └── resources/                     # Archivos de configuración
│   └── target/                                # Archivos compilados y generados por Maven
│       ├── classes/edu/eci/arsw/springdemo/ui/
│       └── generated-sources/annotations/
│
└── laboratorio/                               # Proyecto principal: Blueprints con componentes y conectores
    ├── .mvn/wrapper/                          # Configuración de wrapper de Maven
    ├── img/media/                             # Capturas del laboratorio
    ├── src/
    │   ├── main/java/edu/eci/arsw/blueprints/
    │   │   ├── filter/impl/                   # Implementaciones de filtros
    │   │   ├── model/                         # Clases de dominio (Blueprint, Point)
    │   │   ├── persistence/impl/              # Persistencia en memoria
    │   │   └── services/                      # Lógica de negocio y orquestación
    │   └── test/java/edu/eci/arsw/blueprints/test/persistence/impl/
    │                                          # Pruebas unitarias de persistencia
    └── target/                                # Archivos compilados y generados por Maven
        ├── classes/edu/eci/arsw/blueprints/   # Clases compiladas
        │   ├── filter/impl/
        │   ├── model/
        │   ├── persistence/impl/
        │   └── services/
        ├── generated-sources/annotations/
        ├── generated-test-sources/test-annotations/
        ├── maven-archiver/
        ├── maven-status/                      # Estado de compilación
        ├── surefire-reports/                  # Reportes de ejecución de pruebas
        └── test-classes/edu/eci/arsw/blueprints/test/persistence/impl/

```
---

### Ejecutar el Proyecto

Este laboratorio está compuesto por dos proyectos Maven independientes: **ejercicio-previo** y **laboratorio**. 
Dentro de cada proyecto se encuentra su respectivo README, donde cada se puede ver el contenido y la finalidad de cada 
proyecto.

Cada uno debe compilarse y ejecutarse por separado. A continuación, se describen los pasos para ejecutar ambos proyectos en cualquier sistema operativo compatible con Java y Maven.

#### 1. Requisitos previos

- **Java 17** o superior instalado y configurado en el `PATH`.
- **Apache Maven** instalado y configurado en el `PATH`.
- (Opcional) Un IDE como IntelliJ IDEA, Eclipse o VS Code para facilitar la edición y ejecución.

Verifica las versiones instaladas ejecutando en la terminal:

```bash
java -version
mvn -version
```

#### 2. Clonar el repositorio

Si aún no tiene el repositorio localmente, clónelo con:

```bash
git clone https://github.com/NicoToro25/ARSW-Laboratorio-3-Componentes-Conectores-I.git
cd laboratorio-3
```

#### 3. Compilar los proyectos

Cada parte es un proyecto Maven independiente. Debes compilar cada uno por separado:

- **ejercicio-previo**

```bash
cd ejercicio-previo
mvn clean package
```

- **laboratorio**

```bash
cd ../laboratorio
mvn clean package
```

#### 4. Ejecutar los proyectos

Para ejecutar cada parte se debe estar en la carpeta específica de cada proyecto `/ejercicio-previo` o `/laboratorio`

- **ejercicio-previo**

En el directorio `ejercicio-previo` ejecute:

```bash
mvn exec:java@ejercicio-previo
```

- **laboratorio**

En el directorio `/laboratorio` ejecute:

```bash
mvn exec:java@laboratorio
```

> **Nota:** Si su IDE lo permite, también puede ejecutar directamente las clases principales desde la interfaz gráfica del IDE.

Si se tiene algún inconveniente con la ejecución, asegúrarse de que las variables de entorno de Java y Maven estén correctamente configuradas y de estar ubicado en la carpeta correspondiente antes de ejecutar los comandos.


---
