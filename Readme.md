App de Carpooling
Descripción General

Nuestra aplicación móvil de carpooling, desarrollada en Flutter para Android, tiene como objetivo optimizar la movilidad urbana conectando a conductores y pasajeros que comparten rutas similares. La app permite crear y gestionar viajes, realizar reservas, efectuar pagos seguros, enviar y recibir notificaciones en tiempo real y mantener comunicación directa mediante mensajería interna.

Además, incorpora funcionalidades de seguridad como verificación de usuarios, calificaciones, reportes de incidencias y control de identidad, lo que garantiza un servicio confiable, transparente y eficiente tanto para pasajeros como para conductores.

El backend, implementado en Ruby y respaldado por una base de datos MySQL, gestiona toda la lógica del negocio: autenticación, administración de usuarios y vehículos, publicación y reserva de viajes, control de pagos, sistema de notificaciones y manejo de reportes. Este modelo contribuye a reducir costos de transporte, disminuir el tráfico urbano y fomentar la sostenibilidad ambiental, generando a la vez valor para los usuarios mediante un servicio accesible y seguro.

Configuración del Ambiente de Desarrollo
1. Ruby

Ruby es un lenguaje de programación interpretado y orientado a objetos, reconocido por su sintaxis clara y su productividad. En el backend permite gestionar la lógica del negocio: autenticación, manejo de viajes, pagos, notificaciones y más.

1.1 Descargar Ruby Installer

Desde el sitio oficial: <a href="https://rubyinstaller.org/downloads/">Ruby Installer</a>


1.2 Instalar Ruby en Windows

1.3 Verificar instalación

2. Flutter SDK

Flutter es un framework multiplataforma de Google que utiliza el lenguaje Dart y permite desarrollar interfaces rápidas, modernas y eficientes. Con Flutter garantizamos que la app funcione de manera fluida en Android.

2.1 Descargar Flutter SDK

Desde el sitio oficial:
<a href="https://docs.flutter.dev/get-started/install/windows/mobile">Flutter SDK</a>


2.2 Configurar la ruta

Agregar la ruta del SDK a la variable de entorno PATH.

2.3 Instalación del SDK

2.4 Verificar instalación

Ejecutar:

flutter doctor
flutter doctor --android-licenses
git config --global --add safe.directory '*'

3. Android Studio

Android Studio es el IDE oficial para el desarrollo de aplicaciones Android. Permite compilar, depurar y ejecutar la app en dispositivos reales o emuladores.

3.1 Descargar Android Studio

<a href="https://developer.android.com/studio#get-android-studio">Sitio oficial</a>

3.2 Instalación


3.3 Verificación

Diagrama de Despliegue

La arquitectura utilizada es cliente-servidor.
Los clientes incluyen:

Aplicación móvil para usuarios finales.

Dashboard web para administradores y desarrolladores.

El flujo de comunicación funciona así:

La app móvil envía solicitudes vía HTTPS al backend Ruby mediante una API REST.

El backend realiza operaciones CRUD y consultas a la base de datos MySQL.

Cuando es necesario, el backend se comunica con Firebase Cloud Messaging (FCM) para el envío de notificaciones push.

El dashboard web permite supervisar métricas, administrar usuarios y gestionar la operación técnica y comercial de la plataforma.

Requerimientos Funcionales y No Funcionales
Requerimientos Funcionales

| Requerimiento             | Categoría     | Descripción                                             | Prioridad |
| ------------------------- | ------------- | ------------------------------------------------------- | --------- |
| Registro de usuarios      | Autenticación | Permite registrar nuevos usuarios con datos básicos.    | Alta      |
| Inicio de sesión          | Autenticación | Acceso mediante correo y contraseña.                    | Alta      |
| Gestión de perfil         | Usuario       | Editar datos personales, fotos y preferencias.          | Media     |
| Verificación de usuario   | Seguridad     | Validación de correo y teléfono.                        | Alta      |
| Registro de vehículos     | Vehículos     | Conductores registran datos y fotos de su auto.         | Alta      |
| Publicación de viajes     | Viajes        | Creación de viajes con origen, destino, fecha y precio. | Alta      |
| Reserva de asientos       | Viajes        | Pasajeros reservan asientos disponibles.                | Alta      |
| Pagos en línea            | Pagos         | Procesamiento seguro de pagos electrónicos.             | Alta      |
| Gestión de reservas       | Reservas      | Editar o cancelar reservas bajo políticas definidas.    | Media     |
| Sistema de notificaciones | Comunicación  | Envío de alertas de viajes, pagos y actualizaciones.    | Alta      |
| Mensajería interna        | Comunicación  | Chat entre conductor y pasajero.                        | Media     |
| Reseñas y calificaciones  | Reputación    | Evaluaciones entre usuarios tras el viaje.              | Media     |
| Reporte de incidencias    | Seguridad     | Denuncia de comportamientos inapropiados.               | Alta      |
| Paradas intermedias       | Viajes        | Añadir paradas opcionales en un viaje.                  | Baja      |
