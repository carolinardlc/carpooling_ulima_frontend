<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>App CarPooling — Documento Técnico</title>
  <meta name="description" content="Documento técnico y guía de desarrollo para la App de CarPooling (Flutter + Ruby + MySQL). Requerimientos, arquitectura, diagramas y mockups." />
  <style>
    :root{
      --accent:#0b74da;
      --muted:#6b7280;
      --bg:#f7f9fc;
      --card:#ffffff;
      --maxw:1000px;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    body{background:var(--bg);color:#111827;margin:0;line-height:1.5}
    .container{max-width:var(--maxw);margin:32px auto;padding:24px}
    header{display:flex;align-items:center;gap:16px;margin-bottom:18px}
    header h1{margin:0;font-size:1.6rem}
    header p{margin:0;color:var(--muted)}
    .card{background:var(--card);border-radius:12px;padding:18px;box-shadow:0 6px 18px rgba(15,23,42,0.06);margin-bottom:18px}
    h2{color:var(--accent);margin-top:8px}
    h3{margin-top:12px}
    table{width:100%;border-collapse:collapse;margin-top:12px}
    table th,table td{padding:8px;border:1px solid #e6edf3;text-align:left;font-size:0.95rem}
    table th{background:#f1f6fb;color:#0f172a}
    .two-col{display:grid;grid-template-columns:1fr 300px;gap:16px}
    .muted{color:var(--muted);font-size:0.95rem}
    .small{font-size:0.9rem;color:var(--muted)}
    ul{margin:8px 0 8px 20px}
    pre{background:#0f172a;color:#f8fafc;padding:12px;border-radius:8px;overflow:auto;font-size:0.9rem}
    .img-placeholder{width:100%;height:180px;border-radius:8px;background:linear-gradient(90deg,#eef6ff,#f7fbff);display:flex;align-items:center;justify-content:center;color:var(--muted);border:1px dashed #dbeafe}
    footer{font-size:0.9rem;color:var(--muted);margin-top:12px;text-align:center}
    @media (max-width:900px){.two-col{grid-template-columns:1fr} .container{padding:14px}}
  </style>
</head>
<body>
  <main class="container">
    <header>
      <div>
        <h1>App de CarPooling — Documento Técnico Mejorado</h1>
        <p class="small">Flutter (Android) • Backend Ruby • MySQL — Documento de requisitos, arquitectura y guías de instalación</p>
      </div>
    </header>

    <!-- Overview -->
    <section class="card" id="overview">
      <h2>Resumen del proyecto</h2>
      <p class="muted">
        <strong>CarPooling</strong> es una aplicación móvil desarrollada con <strong>Flutter</strong> para Android que conecta conductores y pasajeros con rutas similares
        para compartir viajes. La plataforma permite crear y reservar viajes, gestionar pagos electrónicos, enviar notificaciones en tiempo real y mantener comunicación entre usuarios.
        Integra mecanismos de confianza (calificaciones, reportes y verificación) para asegurar una experiencia segura, transparente y eficiente.
      </p>

      <h3>Objetivos principales</h3>
      <ul>
        <li>Reducir costos de transporte y congestión urbana.</li>
        <li>Ofrecer una alternativa sostenible y accesible para desplazamientos diarios.</li>
        <li>Brindar una plataforma confiable y escalable para conductores, pasajeros y administradores.</li>
      </ul>
    </section>

    <!-- Tech Stack -->
    <section class="card" id="tech-stack">
      <h2>Tecnologías principales</h2>
      <div class="two-col">
        <div>
          <h3>Frontend / Mobile</h3>
          <ul>
            <li>Flutter (Dart) — App Android (arquitectura recomendada: BLoC / Provider / Riverpod).</li>
            <li>Integración con FCM para notificaciones push.</li>
            <li>Mapas y geolocalización: Google Maps SDK / Mapbox (según preferencia).</li>
          </ul>

          <h3>Backend</h3>
          <ul>
            <li>Ruby (Ruby on Rails o Sinatra) — API REST JSON.</li>
            <li>MySQL — Base de datos relacional.</li>
            <li>Servicios externos: pasarela de pagos (Stripe, PayPal, MercadoPago), FCM, servicio de verificación SMS/Email.</li>
          </ul>

          <h3>Infraestructura recomendada</h3>
          <ul>
            <li>Contenedores Docker + Kubernetes (opcional) para escalabilidad.</li>
            <li>Balanceador de carga (NGINX / HAProxy), SSL/TLS, CDN para activos.</li>
            <li>Backups periódicos y monitorización (Prometheus / Grafana).</li>
          </ul>
        </div>

        <aside>
          <h3>Imágenes / Diagramas</h3>
          <div class="img-placeholder">Diagrama de despliegue (images/imagen11.png)</div>
          <p class="small" style="margin-top:8px">Añade las imágenes en la carpeta <code>images/</code> con los nombres ya referenciados en el documento.</p>
        </aside>
      </div>
    </section>

    <!-- Instalación -->
    <section class="card" id="setup">
      <h2>Configuración del ambiente de desarrollo</h2>

      <h3>1. Ruby (Backend)</h3>
      <p class="muted">Ruby se utiliza para implementar la API REST que gestionará autenticación, reservas, pagos, notificaciones y reportes.</p>
      <ol>
        <li>Descargar el instalador desde el sitio oficial: <a href="https://rubyinstaller.org/downloads/" target="_blank" rel="noopener">rubyinstaller.org</a>.</li>
        <li>Instalar y comprobar versión con <code>ruby -v</code> y <code>gem -v</code>.</li>
        <li>Recomendación: usar <code>rbenv</code> o <code>rvm</code> si se trabajará con varias versiones de Ruby.</li>
      </ol>

      <h3>2. Flutter SDK (Frontend)</h3>
      <p class="muted">Flutter permite compilar la aplicación para Android con una sola base de código.</p>
      <ol>
        <li>Descargar Flutter: <a href="https://docs.flutter.dev/get-started/install/windows/mobile" target="_blank" rel="noopener">docs.flutter.dev</a>.</li>
        <li>Añadir la carpeta <code>flutter/bin</code> al PATH del sistema.</li>
        <li>Verificar instalación: <code>flutter doctor</code> y aceptar licencias: <code>flutter doctor --android-licenses</code>.</li>
        <li>Si surge un problema con Git: <code>git config --global --add safe.directory '*'</code>.</li>
      </ol>

      <h3>3. Android Studio</h3>
      <ol>
        <li>Descargar desde: <a href="https://developer.android.com/studio#get-android-studio" target="_blank" rel="noopener">developer.android.com</a>.</li>
        <li>Instalar SDK, crear/emular dispositivo Android, configurar AVD.</li>
        <li>Conectar el proyecto Flutter a Android Studio para depuración y pruebas en emulador o dispositivo físico.</li>
      </ol>

      <div style="margin-top:10px" class="small">Imágenes de ayuda: <span class="muted">images/imagen1.png → images/imagen10.png</span></div>
    </section>

    <!-- Arquitectura -->
    <section class="card" id="architecture">
      <h2>Arquitectura y diagrama de despliegue</h2>
      <p class="muted">Arquitectura cliente-servidor: la app móvil actúa como cliente, la API en Ruby gestiona la lógica y MySQL almacena los datos. Las notificaciones se gestionan mediante FCM.</p>

      <h3>Flujo básico</h3>
      <ol>
        <li>Usuario inicia sesión → token JWT (o sesión) emitida por la API.</li>
        <li>Conductor publica un viaje (origen, destino, plazas, precio).</li>
        <li>Pasajero busca viajes → reserva asiento → genera pago.</li>
        <li>Backend confirma pago y notifica a conductor/pasajero vía FCM.</li>
        <li>Después del viaje, ambos usuarios pueden calificarse y dejar reseña.</li>
      </ol>

      <div class="img-placeholder">Diagrama Entidad-Relación (images/imagen13.png)</div>
    </section>

    <!-- Requerimientos -->
    <section class="card" id="requirements">
      <h2>Requerimientos</h2>

      <h3>Funcionales (resumen)</h3>
      <table>
        <thead>
          <tr><th>Nombre</th><th>Característica</th><th>Descripción</th><th>Prioridad</th></tr>
        </thead>
        <tbody>
          <tr><td>Registro de usuarios</td><td>Autenticación</td><td>Registro con datos básicos y verificación</td><td>Alta</td></tr>
          <tr><td>Inicio de sesión</td><td>Autenticación</td><td>Acceso con email/contraseña (y/o OAuth)</td><td>Alta</td></tr>
          <tr><td>Publicación de viajes</td><td>Viajes</td><td>Crear viajes con origen, destino, fecha y precio</td><td>Alta</td></tr>
          <tr><td>Reserva de asientos</td><td>Viajes</td><td>Reservar uno o varios asientos disponibles</td><td>Alta</td></tr>
          <tr><td>Pagos en línea</td><td>Pagos</td><td>Pasarela de pago segura</td><td>Alta</td></tr>
          <tr><td>Notificaciones</td><td>Comunicación</td><td>FCM para alertas en tiempo real</td><td>Alta</td></tr>
          <tr><td>Mensajería</td><td>Comunicación</td><td>Chat entre conductor y pasajero</td><td>Media</td></tr>
          <tr><td>Reseñas y reportes</td><td>Reputación & Seguridad</td><td>Calificaciones y reportes de incidencias</td><td>Alta</td></tr>
        </tbody>
      </table>

      <h3>No funcionales (resumen)</h3>
      <table>
        <thead><tr><th>Nombre</th><th>Característica</th><th>Descripción</th><th>Prioridad</th></tr></thead>
        <tbody>
          <tr><td>Escalabilidad</td><td>Rendimiento</td><td>Soportar crecimiento de usuarios</td><td>Alta</td></tr>
          <tr><td>Disponibilidad</td><td>Confiabilidad</td><td>99% uptime objetivo</td><td>Alta</td></tr>
          <tr><td>Seguridad de datos</td><td>Seguridad</td><td>Cifrado en reposo y en tránsito</td><td>Alta</td></tr>
          <tr><td>Tiempo de respuesta</td><td>Rendimiento</td><td>API responde en < 2s en condiciones normales</td><td>Alta</td></tr>
          <tr><td>Mantenibilidad</td><td>Soporte</td><td>Código modular y documentado</td><td>Media</td></tr>
        </tbody>
      </table>
    </section>

    <!-- Casos de uso -->
    <section class="card" id="use-cases">
      <h2>Casos de uso (principales)</h2>
      <table>
        <thead><tr><th>Código</th><th>Nombre</th><th>Actor</th><th>Descripción</th></tr></thead>
        <tbody>
          <tr><td>UC1</td><td>Registrarse / Iniciar sesión</td><td>Usuario</td><td>Crear cuenta o acceder con credenciales</td></tr>
          <tr><td>UC2</td><td>Solicitar / Reservar viaje</td><td>Pasajero</td><td>Reservar asiento en un viaje disponible</td></tr>
          <tr><td>UC6</td><td>Aceptar viaje</td><td>Conductor</td><td>Conductor acepta la solicitud de pasajero</td></tr>
          <tr><td>UC7</td><td>Finalizar viaje</td><td>Conductor</td><td>Marcar viaje como completado</td></tr>
          <tr><td>UC8</td><td>Calificar pasajero</td><td>Conductor</td><td>Dar feedback y calificación</td></tr>
          <tr><td>UC9</td><td>Gestionar usuarios</td><td>Administrador</td><td>Activar, suspender o eliminar cuentas</td></tr>
        </tbody>
      </table>
    </section>

    <!-- ER Diagram description -->
    <section class="card" id="er">
      <h2>Modelo de datos (alto nivel)</h2>
      <p class="muted">Entidades clave: <strong>Users, Vehicles, Trips, Bookings, Payments, Stops, Reviews, Messages, Reports, Notifications</strong>.</p>
      <ul>
        <li><strong>Users</strong>: datos personales, roles (pasajero/conductor/administrador), verificación y calificaciones.</li>
        <li><strong>Vehicles</strong>: vinculados a conductores; marca, modelo, placa, capacidad.</li>
        <li><strong>Trips</strong>: origen/destino, plazas, precio, horarios, paradas intermedias.</li>
        <li><strong>Bookings</strong>: referencia a trip + user, estado y monto.</li>
        <li><strong>Payments</strong>: transacciones asociadas a reservas.</li>
      </ul>
      <div class="img-placeholder">ER Diagram (images/imagen13.png)</div>
    </section>

    <!-- Mockups -->
    <section class="card" id="mockups">
      <h2>Mockups y pantallas clave</h2>
      <p class="muted">Lista de pantallas principales para el diseño UI/UX:</p>
      <ol>
        <li>Iniciar sesión</li>
        <li>Registrarse</li>
        <li>Fallo de inicio de sesión (error handling)</li>
        <li>Búsqueda de viajes / resultados</li>
        <li>Detalle de viaje y solicitud de reserva</li>
        <li>Chat entre conductor y pasajero</li>
        <li>Calificación y reseña post-viaje</li>
        <li>Perfil de usuario</li>
        <li>Configuración de perfil</li>
        <li>Historial de viajes</li>
        <li>Registro de vehículo</li>
        <li>Registro de método de pago</li>
        <li>Confirmación de transacción</li>
        <li>Notificaciones</li>
      </ol>
      <div class="img-placeholder">Mockups (images/PROG.MOVIL.svg)</div>
    </section>

    <!-- Mejoras propuestas -->
    <section class="card" id="improvements">
      <h2>Mejoras propuestas (priorizadas)</h2>
      <h3>Inmediatas (sprint 1)</h3>
      <ul>
        <li>Implementar autenticación JWT y verificación por email/SMS.</li>
        <li>Integrar pasarela de pagos y flujo de confirmación.</li>
        <li>Chat básico con mensajes asociados a una reserva (persistencia mínima).</li>
        <li>Test básico de integración: endpoints críticos / flujo de reserva y pago.</li>
      </ul>

      <h3>Mediano plazo (sprint 2-3)</h3>
      <ul>
        <li>Optimizar búsqueda de viajes (filtros por hora, precio y paradas).</li>
        <li>Mejorar UX con mapas interactivos y geocoding inverso para paradas.</li>
        <li>Panel de administración para gestión de usuarios y reportes.</li>
      </ul>

      <h3>Largo plazo</h3>
      <ul>
        <li>Escalado horizontal (autoscaling, base de datos replicada).</li>
        <li>Funcionalidades avanzadas: matching predictivo, rutas recurrentes, suscripciones.</li>
        <li>Internacionalización (i18n) y soporte multi-moneda.</li>
      </ul>
    </section>

    <!-- Seguridad y cumplimiento -->
    <section class="card" id="security">
      <h2>Seguridad y buenas prácticas</h2>
      <ul>
        <li>Uso de HTTPS/TLS en todas las comunicaciones.</li>
        <li>Almacenamiento seguro de contraseñas (bcrypt/argon2) y tokens con expiración.</li>
        <li>Validación y sanitización de inputs (prevención de SQL injection / XSS).</li>
        <li>Registro de auditoría para acciones críticas (pagos, reportes, cambios de estado).</li>
        <li>Política de privacidad y manejo de datos personales conforme a la legislación aplicable.</li>
      </ul>
    </section>

    <!-- Roadmap / Next steps -->
    <section class="card" id="roadmap">
      <h2>Roadmap y siguientes pasos recomendados</h2>
      <ol>
        <li>Definir MVP funcional mínimo (registro, publicación de viajes, reserva, pago, notificaciones, calificaciones).</li>
        <li>Implementar pruebas automatizadas (unitarias e integración) para flujo crítico.</li>
        <li>Desplegar en un entorno de staging (pruebas con datos reales controlados).</li>
        <li>Realizar pruebas de usabilidad con usuarios reales y ajustar UX.</li>
        <li>Plan de lanzamiento limitado (ciudad/área) y monitoreo de métricas clave (Tasa de ocupación, Tasa de cancelación, Tiempo promedio de respuesta).</li>
      </ol>
    </section>

    <!-- anexos / referencias -->
    <section class="card" id="appendix">
      <h2>Anexos y recursos</h2>
      <ul>
        <li>Enlaces: Flutter docs, Ruby, Android Studio (en los apartados anteriores).</li>
        <li>Imágenes y diagramas referenciados dentro del proyecto: carpeta <code>images/</code>.</li>
        <li>Sugerencia: mantener un repositorio Git con ramas <code>main</code>, <code>develop</code> y ramas por feature.</li>
      </ul>
    </section>

    <footer>
      Versión del documento: <strong>Mejorada</strong> • Exportado como HTML • Si quieres, lo transformo en un README.md, un PDF o una presentación.
    </footer>
  </main>
</body>
</html>
