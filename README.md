## 📖 Descripción General

Device Insight es una aplicación Android desarrollada en Kotlin, con el fin de aprender los primeros pasos de la programacion móvil; que permite monitorear en tiempo real los sensores del dispositivo y el estado de conectividad. Diseñada con buenas prácticas de desarrollo, incluye gestión moderna de permisos y una interfaz de usuario intuitiva.

## 🎯 Características Principales

### 🔍 Panel de Sensores
- **Monitoreo en tiempo real** de acelerómetro y sensor de luz ambiental
- **Control de muestreo** con tasas configurables (Rápido, Normal, Lento)
- **Filtrado de datos** con promedios móviles para lecturas suavizadas
- **Pausar/Reanudar** monitoreo según necesidad
- **Historial** de las últimas 20 lecturas con timestamps

### 🌐 Panel de Conectividad  
- **Estado de conexión** (Conectado/Desconectado)
- **Tipo de conexión** (Wi-Fi, Datos Móviles, Ethernet)
- **Información detallada** de red Wi-Fi (SSID, intensidad de señal)
- **Datos del operador** móvil y tipo de red (2G, 3G, 4G, 5G)
- **Gestión inteligente** de permisos con explicaciones contextuales

### 🔐 Privacidad y Permisos
- **Explicaciones claras** del propósito de cada permiso
- **Solicitud contextual** de permisos en tiempo de ejecución
- **Manejo elegante** de denegaciones con opciones de recuperación
- **Transparencia total** en el uso de datos del usuario

## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Kotlin 100%
- **Arquitectura:** MVC (Preparada para migración a MVVM)
- **SDK Mínimo:** API 26 (Android 8.0)
- **SDK Objetivo:** API 34 (Android 14)
- **Bibliotecas Principales:**
  - Material Design Components
  - AndroidX (AppCompat, ConstraintLayout)
  - Lifecycle (ViewModel, LiveData)
  - Coroutines (Para operaciones asíncronas)

## 📱 Sensores Utilizados

| Sensor | Tipo | Propósito | Disponibilidad |
|--------|------|-----------|----------------|
| **Acelerómetro** | `TYPE_ACCELEROMETER` | Medir movimiento y orientación | ✅ Disponible en todos los dispositivos |
| **Sensor de Luz** | `TYPE_LIGHT` | Medir intensidad lumínica ambiental | ⚠️ Disponible en la mayoría de dispositivos |
| **Preparado para:** Giroscopio, Proximidad, Magnetómetro | - | - | Expandible |

## 🔐 Permisos Requeridos

| Permiso | Propósito | Nivel de Riesgo |
|---------|-----------|-----------------|
| `ACCESS_FINE_LOCATION` | Detectar redes Wi-Fi cercanas y señal | Alto |
| `ACCESS_COARSE_LOCATION` | Ubicación aproximada para redes | Alto |
| `READ_PHONE_STATE` | Información del operador móvil | Alto |
| `ACCESS_WIFI_STATE` | Estado y información de conexión Wi-Fi | Normal |
| `ACCESS_NETWORK_STATE` | Verificar conectividad general | Normal |

**Nota:** Todos los permisos incluyen explicaciones detalladas y se solicitan solo cuando son necesarios.

## 🏗️ Arquitectura Implementada
app/
├── data/
│ └── models/                         # Modelos de datos (SensorData, ConnectivityInfo)
├── ui/
│ └── activities/                     # Activities (Main, Sensores, Connectivity, Privacy)
├── utils/                               # Utilidades (PermissionManager, Constants)
└── resources/                     # Layouts, strings, themes


##🚀 Instalación y Uso

1. Clonar el proyecto:
   ```bash
   git clone https://github.com/tuusuario/device-insight.git
2.	Abrir en Android Studio:
o	Abrir Android Studio
o	Seleccionar "Open an existing project"
o	Navegar a la carpeta del proyecto
3.	Ejecutar en dispositivo:
o	Conectar dispositivo Android vía USB
o	Habilitar depuración USB
o	Ejecutar app configuration
📋 Requisitos del Sistema
•	Android 8.0+ (API 26+)
•	Permisos de ubicación para información completa de Wi-Fi
•	Sensores físicos para funcionalidad completa de monitoreo (los del dispositivo)
📄 Licencia
Este proyecto está a disposición de cualquiera que lo utilice con fines educativos
👨‍💻 Autor
•	Diego Alonso González Gándara
________________________________________
