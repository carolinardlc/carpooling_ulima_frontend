# 🚗 CarPooling App

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Ruby](https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)](https://www.ruby-lang.org)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com)
[![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com)

> **Optimiza tu movilidad urbana compartiendo viajes de forma segura, eficiente y sostenible**

---

## 📋 Tabla de Contenidos

- [Descripción](#-descripción)
- [Características Principales](#-características-principales)
- [Tecnologías Utilizadas](#️-tecnologías-utilizadas)
- [Configuración del Ambiente de Desarrollo](#-configuración-del-ambiente-de-desarrollo)
  - [Ruby](#1-ruby)
  - [Flutter SDK](#2-flutter-sdk)
  - [Android Studio](#3-android-studio)
- [Arquitectura del Sistema](#️-arquitectura-del-sistema)
- [Requerimientos](#-requerimientos)
  - [Funcionales](#requerimientos-funcionales)
  - [No Funcionales](#requerimientos-no-funcionales)
- [Casos de Uso](#-casos-de-uso)
- [Modelo de Datos](#️-modelo-de-datos)
- [Mockups](#-mockups)
- [Contribuir](#-contribuir)
- [Licencia](#-licencia)

---

## 📖 Descripción

**CarPooling App** es una aplicación móvil innovadora desarrollada en Flutter para Android que revoluciona la movilidad urbana al conectar conductores y pasajeros que comparten rutas similares. Nuestra plataforma facilita viajes compartidos de manera inteligente, reduciendo costos, minimizando el tráfico vehicular y contribuyendo significativamente a la sostenibilidad ambiental.

### 🎯 Objetivo

Crear un ecosistema de transporte colaborativo que permita a los usuarios:
- **Crear y reservar viajes** de manera intuitiva
- **Gestionar pagos seguros** con múltiples métodos de pago
- **Recibir notificaciones en tiempo real** sobre el estado de sus viajes
- **Mantener comunicación directa** a través de mensajería integrada
- **Construir confianza** mediante un sistema robusto de calificaciones y verificación

---

## ✨ Características Principales

### Para Pasajeros 👥
- ✅ Búsqueda y reserva de viajes disponibles
- 💳 Pagos seguros y verificados
- ⭐ Sistema de calificación y reseñas
- 💬 Chat en tiempo real con conductores
- 📍 Seguimiento de viaje en curso
- 📜 Historial completo de viajes

### Para Conductores 🚘
- 📝 Publicación de viajes con rutas personalizadas
- 🚦 Gestión de paradas intermedias
- 💰 Recepción de pagos automatizada
- ⭐ Perfil con calificaciones y reputación
- 🔔 Notificaciones de nuevas reservas
- 📊 Dashboard de viajes realizados

### Seguridad y Confianza 🛡️
- ✔️ Verificación de usuarios (correo y teléfono)
- 🚨 Sistema de reportes de incidencias
- 🔒 Encriptación de datos sensibles
- ⚖️ Políticas de cancelación claras
- 📱 Soporte y asistencia integrada

---

## 🛠️ Tecnologías Utilizadas

### Frontend
- **Flutter** - Framework multiplataforma para desarrollo móvil
- **Dart** - Lenguaje de programación orientado a objetos

### Backend
- **Ruby** - Lenguaje para la lógica de negocio
- **Ruby API REST** - Arquitectura de servicios web
- **MySQL** - Sistema de gestión de base de datos relacional

### Servicios Externos
- **Firebase Cloud Messaging (FCM)** - Sistema de notificaciones push
- **Google Maps API** - Integración de mapas y geolocalización

### Herramientas de Desarrollo
- **Android Studio** - IDE oficial para desarrollo Android
- **Git** - Control de versiones
- **Postman** - Pruebas de API

---

## 🚀 Configuración del Ambiente de Desarrollo

### Requisitos Previos
- Windows 10 o superior
- Al menos 8GB de RAM
- 10GB de espacio en disco disponible
- Conexión a Internet estable

---

### 1. Ruby

Ruby es el lenguaje de programación que impulsa nuestro backend, gestionando toda la lógica de negocio desde la autenticación hasta el procesamiento de pagos.

#### 1.1 Descarga
Visita el [sitio oficial de Ruby Installer](https://rubyinstaller.org/downloads/) y descarga la versión recomendada para Windows.

<img width="950" height="670" alt="image" src="https://github.com/user-attachments/assets/91b7151e-e48a-412d-a866-d8c365d104cb" />


#### 1.2 Instalación
Ejecuta el instalador y sigue las instrucciones en pantalla. Asegúrate de marcar la opción **"Add Ruby to PATH"**.

<img width="858" height="305" alt="image" src="https://github.com/user-attachments/assets/58b68e0c-d874-4277-b39b-bd660e074fe0" />


#### 1.3 Verificación
Abre una terminal y ejecuta:
```bash
ruby --version
```

Deberías ver la versión instalada de Ruby.

<img width="864" height="246" alt="image" src="https://github.com/user-attachments/assets/fdf94783-4d49-4a02-a9ac-2eef35c73cf6" />


---

### 2. Flutter SDK

Flutter es el framework de Google que permite crear aplicaciones nativas multiplataforma con un solo código base, utilizando el lenguaje Dart.

#### 2.1 Descarga
Descarga Flutter SDK desde la [documentación oficial](https://docs.flutter.dev/get-started/install/windows/mobile).

<img width="1237" height="594" alt="image" src="https://github.com/user-attachments/assets/7603f8ac-b2d4-4864-a724-7ef71cc797a6" />


#### 2.2 Configuración de Variables de Entorno
1. Extrae el archivo descargado en una ubicación permanente (ej: `C:\flutter`)
2. Abre el **Panel de Control** → **Sistema y Seguridad** → **Sistema**
3. Selecciona **Configuración avanzada del sistema**
4. Haz clic en **Variables de entorno**
5. En **Variables del sistema**, edita la variable `PATH`
6. Añade la ruta completa a la carpeta `bin` de Flutter (ej: `C:\flutter\bin`)

<img width="865" height="657" alt="image" src="https://github.com/user-attachments/assets/5e722bdb-6383-4af8-a238-0ace370b8d7e" />


#### 2.3 Instalación
Abre una terminal y ejecuta:
```bash
flutter doctor
```

Este comando verificará todas las dependencias necesarias.

<img width="1244" height="621" alt="image" src="https://github.com/user-attachments/assets/3f63c325-281e-469a-a39f-1be229b87665" />


#### 2.4 Aceptar Licencias de Android
Ejecuta el siguiente comando para aceptar las licencias del SDK de Android:
```bash
flutter doctor --android-licenses
```

**Nota:** Si encuentras errores de permisos Git, ejecuta:
```bash
git config --global --add safe.directory '*'
```

<img width="1260" height="647" alt="image" src="https://github.com/user-attachments/assets/5545fe3e-f545-42f4-918c-34dd001dd1c4" />


---

### 3. Android Studio

Android Studio es el entorno de desarrollo integrado (IDE) oficial para aplicaciones Android, proporcionando todas las herramientas necesarias para compilar, depurar y probar la aplicación.

#### 3.1 Descarga
Descarga Android Studio desde el [sitio oficial](https://developer.android.com/studio#get-android-studio).

<img width="1244" height="506" alt="image" src="https://github.com/user-attachments/assets/416758b7-f468-4f21-a1e6-95dd81b1a98d" />


#### 3.2 Instalación
Ejecuta el instalador y sigue el asistente de configuración. Asegúrate de instalar:
- Android SDK
- Android SDK Platform-Tools
- Android Emulator

<img width="707" height="571" alt="image" src="https://github.com/user-attachments/assets/3ccba9fe-9a5e-43c6-a367-3c87e3a5f4e6" />


#### 3.3 Verificación
Abre Android Studio y verifica que el SDK esté correctamente configurado en **Settings → Appearance & Behavior → System Settings → Android SDK**.

<img width="970" height="771" alt="image" src="https://github.com/user-attachments/assets/df020cf9-de98-4137-9e88-284687dd67df" />


---

## 🏗️ Arquitectura del Sistema

### Diagrama de Despliegue

Nuestra aplicación utiliza una **arquitectura cliente-servidor moderna** con los siguientes componentes:

<img width="547" height="589" alt="image" src="https://github.com/user-attachments/assets/8c22c443-b7d0-4738-a9ad-decdd1ed172f" />


#### Componentes Principales

1. **Capa de Presentación**
   - 📱 **App Móvil (Flutter)**: Interfaz para usuarios finales
   - 💻 **Dashboard Web**: Panel administrativo y de mantenimiento

2. **Capa de Comunicación**
   - 🔐 **Protocolo HTTPS**: Comunicación segura y encriptada
   - 🔄 **API REST**: Endpoints para operaciones CRUD

3. **Capa de Lógica de Negocio**
   - ⚙️ **Backend Ruby**: Procesamiento de solicitudes
   - 🔍 **Validación de datos**: Seguridad y consistencia
   - 📧 **Gestión de notificaciones**: Integración con FCM

4. **Capa de Datos**
   - 🗄️ **MySQL Database**: Almacenamiento persistente
   - 🔒 **Backup automático**: Respaldo periódico de datos

5. **Servicios Externos**
   - 🔔 **Firebase Cloud Messaging**: Notificaciones push en tiempo real

---

## 📊 Requerimientos

### Requerimientos Funcionales

| ID | Requerimiento | Categoría | Descripción | Prioridad |
|----|---------------|-----------|-------------|-----------|
| **RF01** | Registro de usuarios | Autenticación | Permitir el registro de nuevos usuarios con validación de datos básicos (nombre, email, teléfono, contraseña) | 🔴 Alta |
| **RF02** | Inicio de sesión | Autenticación | Autenticar usuarios mediante email y contraseña con opción de recuperación | 🔴 Alta |
| **RF03** | Gestión de perfil | Usuario | Editar información personal, foto de perfil y preferencias de viaje | 🟡 Media |
| **RF04** | Verificación de usuario | Seguridad | Validar correo electrónico y número telefónico para incrementar la confianza | 🔴 Alta |
| **RF05** | Registro de vehículos | Vehículos | Permitir a conductores registrar vehículos con datos completos (marca, modelo, placa, capacidad, fotos) | 🔴 Alta |
| **RF06** | Publicación de viajes | Viajes | Crear viajes indicando origen, destino, fecha, hora, precio por asiento y asientos disponibles | 🔴 Alta |
| **RF07** | Reserva de asientos | Viajes | Reservar uno o más asientos disponibles en un viaje publicado | 🔴 Alta |
| **RF08** | Pagos en línea | Pagos | Procesar pagos seguros mediante pasarelas de pago electrónicas | 🔴 Alta |
| **RF09** | Gestión de reservas | Reservas | Modificar o cancelar reservas según políticas establecidas | 🟡 Media |
| **RF10** | Notificaciones push | Comunicación | Enviar alertas sobre viajes, pagos, cancelaciones y cambios importantes | 🔴 Alta |
| **RF11** | Mensajería interna | Comunicación | Chat en tiempo real entre conductor y pasajero para coordinar detalles del viaje | 🟡 Media |
| **RF12** | Sistema de calificaciones | Reputación | Permitir a usuarios calificar y dejar reseñas tras completar un viaje | 🟡 Media |
| **RF13** | Reporte de incidencias | Seguridad | Denunciar comportamientos inapropiados, problemas o incidentes durante el viaje | 🔴 Alta |
| **RF14** | Paradas intermedias | Viajes | Gestionar puntos de recojo y paradas opcionales dentro de una ruta | 🟢 Baja |
| **RF15** | Historial de viajes | Usuario | Consultar registro completo de viajes realizados con detalles y comprobantes | 🟡 Media |

---

### Requerimientos No Funcionales

| ID | Requerimiento | Categoría | Descripción | Prioridad |
|----|---------------|-----------|-------------|-----------|
| **RNF01** | Escalabilidad | Rendimiento | El sistema debe soportar un crecimiento progresivo de usuarios sin degradación del rendimiento | 🔴 Alta |
| **RNF02** | Alta disponibilidad | Confiabilidad | El servicio debe mantener una disponibilidad mínima del 99% anual (downtime < 3.65 días/año) | 🔴 Alta |
| **RNF03** | Seguridad de datos | Seguridad | Implementar cifrado AES-256 para datos sensibles en reposo y TLS 1.3 para datos en tránsito | 🔴 Alta |
| **RNF04** | Usabilidad | UX/UI | Interfaz intuitiva con máximo 3 clics para funciones principales, siguiendo principios de Material Design | 🔴 Alta |
| **RNF05** | Compatibilidad | Portabilidad | Soporte para Android 8.0 (API 26) o superior, optimizado para pantallas de 5" a 7" | 🟡 Media |
| **RNF06** | Tiempo de respuesta | Rendimiento | Las peticiones al backend deben completarse en menos de 2 segundos en el 95% de los casos | 🔴 Alta |
| **RNF07** | Mantenibilidad | Desarrollo | Código modular con documentación completa, siguiendo principios SOLID y patrones de diseño | 🟡 Media |
| **RNF08** | Respaldo de datos | Confiabilidad | Backup automático diario de la base de datos con retención de 30 días | 🟡 Media |
| **RNF09** | Internacionalización | Usabilidad | Estructura preparada para soportar múltiples idiomas (i18n) en versiones futuras | 🟢 Baja |
| **RNF10** | Optimización móvil | Rendimiento | Consumo eficiente de batería (<5%/hora de uso activo) y datos (<10MB/hora sin caché de mapas) | 🔴 Alta |

---

## 👥 Casos de Uso

### Diagrama General

<img width="424" height="1219" alt="image" src="https://github.com/user-attachments/assets/dd621409-64fe-4be2-a69d-e01c2108ea65" />


### Descripción Detallada

| Código | Caso de Uso | Actor | Descripción | Flujo Principal |
|--------|-------------|-------|-------------|-----------------|
| **UC01** | Registrarse / Iniciar Sesión | Pasajero / Conductor | Gestión de autenticación y acceso a la plataforma | 1. Usuario ingresa credenciales<br>2. Sistema valida datos<br>3. Se concede acceso |
| **UC02** | Solicitar Viaje | Pasajero | Búsqueda y reserva de viaje disponible | 1. Pasajero busca destino<br>2. Selecciona viaje<br>3. Confirma reserva |
| **UC03** | Cancelar Viaje | Pasajero | Cancelación de viaje previamente reservado | 1. Pasajero accede a reserva<br>2. Solicita cancelación<br>3. Sistema procesa reembolso según políticas |
| **UC04** | Calificar Conductor | Pasajero | Evaluación post-viaje del servicio del conductor | 1. Viaje finalizado<br>2. Pasajero asigna calificación<br>3. Deja comentario opcional |
| **UC05** | Realizar Pago | Pasajero | Procesamiento de pago del viaje reservado | 1. Selecciona método de pago<br>2. Confirma transacción<br>3. Recibe comprobante |
| **UC06** | Aceptar Viaje | Conductor | Confirmación de solicitud de viaje recibida | 1. Conductor recibe notificación<br>2. Revisa detalles<br>3. Acepta o rechaza |
| **UC07** | Finalizar Viaje | Conductor | Marcado de viaje como completado | 1. Conductor indica llegada<br>2. Sistema actualiza estado<br>3. Activa proceso de calificación |
| **UC08** | Calificar Pasajero | Conductor | Evaluación post-viaje del comportamiento del pasajero | 1. Viaje finalizado<br>2. Conductor asigna calificación<br>3. Deja comentario opcional |
| **UC09** | Gestionar Usuarios | Administrador | Control sobre cuentas de usuarios del sistema | 1. Visualiza lista de usuarios<br>2. Revisa actividad<br>3. Suspende/activa cuentas según necesidad |
| **UC10** | Gestionar Conductores | Administrador | Validación y supervisión de conductores registrados | 1. Revisa documentación<br>2. Valida información del vehículo<br>3. Aprueba o rechaza |
| **UC11** | Monitorear Viajes | Administrador | Supervisión en tiempo real de viajes activos | 1. Accede a dashboard<br>2. Visualiza mapa en tiempo real<br>3. Detecta anomalías |
| **UC12** | Ver Historial | Pasajero / Conductor | Consulta de viajes anteriores realizados | 1. Accede a historial<br>2. Filtra por fecha/estado<br>3. Visualiza detalles |
| **UC13** | Ver Perfil Conductor | Pasajero | Consulta de información y reputación del conductor | 1. Selecciona conductor<br>2. Ve calificaciones<br>3. Lee comentarios |
| **UC14** | Configurar Disponibilidad | Conductor | Gestión de horarios disponibles para ofrecer viajes | 1. Accede a configuración<br>2. Define horarios<br>3. Establece días disponibles |
| **UC15** | Ver Perfil Pasajero | Conductor | Consulta de información del pasajero antes de aceptar | 1. Revisa perfil<br>2. Consulta calificaciones<br>3. Toma decisión |
| **UC16** | Generar Reportes | Administrador | Obtención de métricas y estadísticas del sistema | 1. Selecciona tipo de reporte<br>2. Define rango de fechas<br>3. Exporta datos |

---

## 🗄️ Modelo de Datos

### Diagrama Entidad-Relación

<img width="944" height="1076" alt="image" src="https://github.com/user-attachments/assets/386646ae-f32b-4ad8-8262-fa014e456080" />


### Descripción de Entidades

#### 👤 **Users** (Usuarios)
Representa tanto a pasajeros como conductores en el sistema.

**Atributos principales:**
- `user_id` (PK): Identificador único
- `name`, `email`, `phone`: Datos de contacto
- `password_hash`: Contraseña encriptada
- `user_type`: Tipo de usuario (Pasajero/Conductor)
- `rating`: Calificación promedio
- `is_verified`: Estado de verificación
- `profile_photo_url`: Foto de perfil

---

#### 🚗 **Vehicles** (Vehículos)
Vehículos registrados por los conductores.

**Atributos principales:**
- `vehicle_id` (PK): Identificador único
- `user_id` (FK): Conductor propietario
- `brand`, `model`, `year`: Información del vehículo
- `license_plate`: Placa de circulación
- `capacity`: Número de asientos disponibles
- `color`: Color del vehículo

---

#### 🛣️ **Trips** (Viajes)
Viajes ofrecidos por los conductores.

**Atributos principales:**
- `trip_id` (PK): Identificador único
- `driver_id` (FK): Conductor del viaje
- `vehicle_id` (FK): Vehículo asignado
- `origin`, `destination`: Puntos de inicio y fin
- `departure_time`: Hora de salida
- `price_per_seat`: Precio por asiento
- `available_seats`: Asientos disponibles
- `status`: Estado del viaje (Pendiente/En curso/Completado/Cancelado)

---

#### 📝 **Bookings** (Reservas)
Reservas realizadas por los pasajeros.

**Atributos principales:**
- `booking_id` (PK): Identificador único
- `trip_id` (FK): Viaje reservado
- `passenger_id` (FK): Pasajero que reserva
- `seats_reserved`: Cantidad de asientos
- `pickup_location`: Punto de recojo
- `total_amount`: Monto total
- `status`: Estado de la reserva

---

#### 💳 **Payments** (Pagos)
Transacciones de pago realizadas.

**Atributos principales:**
- `payment_id` (PK): Identificador único
- `booking_id` (FK): Reserva asociada
- `amount`: Monto pagado
- `payment_method`: Método utilizado
- `status`: Estado del pago
- `transaction_date`: Fecha de transacción

---

#### 📍 **Stops** (Paradas)
Puntos de parada dentro de un viaje.

**Atributos principales:**
- `stop_id` (PK): Identificador único
- `trip_id` (FK): Viaje asociado
- `address`: Dirección de la parada
- `latitude`, `longitude`: Coordenadas GPS
- `estimated_time`: Hora estimada de llegada
- `stop_order`: Orden en la ruta

---

#### ⭐ **Reviews** (Reseñas)
Calificaciones y opiniones entre usuarios.

**Atributos principales:**
- `review_id` (PK): Identificador único
- `trip_id` (FK): Viaje evaluado
- `reviewer_id` (FK): Usuario que califica
- `reviewed_id` (FK): Usuario calificado
- `rating`: Puntuación (1-5)
- `comment`: Comentario opcional

---

#### 💬 **Messages** (Mensajes)
Sistema de mensajería interna.

**Atributos principales:**
- `message_id` (PK): Identificador único
- `trip_id` (FK): Viaje relacionado
- `sender_id` (FK): Remitente
- `receiver_id` (FK): Destinatario
- `message_content`: Contenido del mensaje
- `sent_at`: Fecha y hora de envío

---

#### 🚨 **Reports** (Reportes)
Denuncias e incidencias reportadas.

**Atributos principales:**
- `report_id` (PK): Identificador único
- `reporter_id` (FK): Usuario que reporta
- `reported_id` (FK): Usuario reportado
- `trip_id` (FK): Viaje relacionado
- `reason`: Motivo del reporte
- `description`: Descripción detallada
- `status`: Estado del reporte

---

#### 🔔 **Notifications** (Notificaciones)
Alertas enviadas a los usuarios.

**Atributos principales:**
- `notification_id` (PK): Identificador único
- `user_id` (FK): Destinatario
- `type`: Tipo de notificación
- `title`: Título de la notificación
- `message`: Contenido del mensaje
- `is_read`: Estado de lectura
- `created_at`: Fecha de creación

---

## 🎨 Mockups

Diseño visual de las principales pantallas de la aplicación:

![Mockups](images/PROG.MOVIL.svg)

### Pantallas Incluidas

1. **Inicio de Sesión** - Autenticación de usuario
2. **Registro** - Creación de nueva cuenta
3. **Error de Inicio** - Manejo de errores de autenticación
4. **Búsqueda de Viaje** - Menú principal de búsqueda
5. **Solicitud de Viaje** - Confirmación de reserva
6. **Chat de Viaje** - Comunicación entre usuarios
7. **Calificación** - Sistema de evaluación post-viaje
8. **Perfil** - Vista de perfil de usuario
9. **Configuración** - Ajustes de perfil
10. **Historial** - Registro de viajes pasados
11. **Registro de Vehículo** - Alta de vehículos
12. **Método de Pago** - Gestión de pagos
13. **Confirmación de Transacción** - Verificación de pago
14. **Notificaciones** - Centro de alertas

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Si deseas colaborar con el proyecto:

1. 🍴 Haz un Fork del repositorio
2. 🌿 Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. 💾 Commit tus cambios (`git commit -m 'Add: nueva funcionalidad'`)
4. 📤 Push a la rama (`git push origin feature/AmazingFeature`)
5. 🔀 Abre un Pull Request

### Directrices de Contribución
- Sigue las convenciones de código establecidas
- Documenta nuevas funcionalidades
- Incluye pruebas para nuevas características
- Actualiza el README si es necesario



<div>

</div>
