# Sustentación Android

## Pasos para Actualizar el Proyecto o Solucionar Bugs

Para mantener el proyecto actualizado y resolver problemas, sigue los siguientes pasos:

### Actualizar Versiones en Android Studio

Asegúrate de seguir las recomendaciones de Android Studio para mantener las versiones actualizadas.

### Cambios Realizados en build.gradle a Nivel de Módulo

1. Cambio de Compatibilidad de Java

   En la primera versión del proyecto, se utilizaba `JavaVersion.VERSION_1_8` como la compatibilidad de origen y destino de Java. En la segunda versión, se ha actualizado a `JavaVersion.VERSION_11`. Esto significa que el proyecto ahora es compatible con Java 11 en lugar de Java 8.

   ```gradle
   compileOptions {
       sourceCompatibility JavaVersion.VERSION_1_8
       targetCompatibility JavaVersion.VERSION_1_8
   }
   kotlinOptions {
       jvmTarget = '1.8'
   }gradle
    Copy code
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_11
        targetCompatibility JavaVersion.VERSION_11
    }
    kotlinOptions {
        jvmTarget = '11'
    }

2. Versión de Kotlin

En ambas versiones del proyecto, se utiliza Kotlin como lenguaje principal. La versión de Kotlin se mantuvo igual en ambas versiones, es decir, '1.5.21'.

    gradle
    Copy code
    kotlinOptions {
        kotlinCompilerExtensionVersion compose_version
        kotlinCompilerVersion '1.5.21'
    }

3. Valor de jvmTarget

Se actualizó el valor de jvmTarget de '1.8' a '11' en la configuración de Kotlin.

     kotlinOptions {
     jvmTarget = '11'
     }

No se realizaron cambios en el archivo build.gradle a nivel de proyecto.
