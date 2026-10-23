🎉 ¡Bienvenido a Clezapp PRO 3.7.14! 🚀
¡Gracias por confiar en Clezapp! Estás utilizando la versión PRO de nuestra plataforma de atención omnicanal, diseñada para ofrecer la máxima velocidad, estabilidad y productividad para tu equipo. 🎯

✨ VENTAJAS Y VIRTUDES DE CLEZAPP PRO

💎 Rendimiento Ultra-Fluido (60 FPS & 0ms Reactivity)
* **Envío Inmediato (Optimistic UI):** Los mensajes se despachan en 0ms; el operador redacta continuamente sin pausas ni esperas de servidor.
* **Alternancia Instantánea de Chats (0ms Ticket Switch):** Memoria en caliente que abre conversaciones previas en cero milisegundos, sin parpadeos ni pantallas en blanco.
* **Elevación de Ticket en Tiempo Real (0ms Lift):** El chat salta automáticamente al primer lugar de la bandeja apenas llega o se envía un mensaje.
* **Arquitectura Asíncrona (Code-Splitting):** Carga modular bajo demanda que reduce el peso inicial en más del 36%, optimizando el arranque en móviles y escritorio.

🛡️ Estabilidad 24/7 y Blindaje Anti-Caídas
* **Blindaje de Conexiones WhatsApp (Baileys & Evolution API):** Keep-Alive proactivo cada 20-25s, purga total de memoria ante sesiones cerradas y monitorización pasiva (watchdog) de 30s que libera hasta un 90% de CPU en el servidor.
* **Reconexión Progresiva Inteligente:** Auto-recuperación con retroceso exponencial ante microcortes de red, sin bucles de error ni fugas de memoria.
* **Protección Anti-Saturación de Grupos:** Descarte inmediato en paso 0 de mensajes de grupos masivos con caché en memoria, evitando sobrecargar RAM y CPU.

📦 Gestión Multimedia Inteligente y Ultraligera
* **Miniaturas Dinámicas (~12 KB):** Reducción de ancho de banda del 99.4% en fotos, videos y stickers en burbujas de chat; el original HD se descarga únicamente al abrir el visor.
* **Visor Cinemático Proporcional:** Vista previa centrada con proporción original para imágenes, videos, audios y stickers sin distorsiones ni desbordes.
* **Identificación Visual en Bandeja:** Identificadores con emojis (📷 Imagen, 📹 Video, 🎵 Audio, 💟 Sticker, 📄 Archivo) para saber al instante el contenido del último mensaje.
* **Persistencia Total de Citas:** Carga garantizada de multimedia citada incluso al actualizar la página (F5).

⚡ Base de Datos de Alta Eficiencia (O(1))
* **Paginación Continua por Cursor:** Navegación por fecha e identificador (beforeCreatedAt / beforeId) en lugar de saltos pesados de OFFSET; navegación fluida en historiales con miles de mensajes.
* **Índices Compuestos de Alto Desempeño:** Consultas y filtros acelerados en PostgreSQL ejecutados en menos de 10ms.
* **Resolución Polimórfica UUID/ID:** Consultas de mensajes optimizadas para soportar identificadores numéricos y UUID sin fallos de conversión de tipos.

🔇 Control Operativo y Productividad
* **Cabecera Colapsable y Barra Ultra-Compacta:** Pestaña deslizante con Chevron (Up/Down) en cabecera de tickets para alternar entre vista completa y modo compacto (46px), maximizando el espacio de lectura.
* **Identificador Visual NO-BOT:** Etiqueta roja en bandeja para detectar al instante los contactos con chatbot desactivado.
* **Control Flexible de Etiquetas en Ajustes:** Opciones en `/settings` para mostrar u ocultar selectivamente etiquetas de conexión, agentes, tags y última interacción.
* **Modo Silencio Absoluto (disableBot):** Desconexión integral de bots, respuestas automáticas y encuestas de salida para una atención 100% humana y limpia.
* **Privacidad de Archivos:** Ocultación del nombre técnico de archivos adjuntos en el chat del receptor.
* **Respuestas Rápidas Inteligentes:** Búsqueda exacta y por similitud con envío directo vía atajo (ej. /hola) en modo carrusel o popup flotante estilo WhatsApp Web.

📋 NOVEDADES Y MEJORAS DESTACADAS

* 🟩 **Cabecera Colapsable y Barra Ultra-Compacta en Tickets:** Pestaña interactiva con icono Chevron centrada sobre el borde del módulo de contacto y etiquetas, permitiendo alternar entre vista completa y barra ultra-compacta (46px) para maximizar el área de lectura en pantalla con transiciones suaves `<Collapse>` y memoria en `localStorage`.
* 🟩 **Etiqueta Roja "NO-BOT" en Tickets:** Identificador visual en vivo para contactos con chatbot deshabilitado, ubicado junto al badge de última interacción y optimizado en `React.memo` para actualización instantánea vía WebSockets.
* 🟩 **Control de Visibilidad de Etiquetas (/settings):** Parametrización en panel de opciones para mostrar u ocultar la etiqueta de última interacción, canal de conexión, nombre de agente asignado y tags de clasificación.
* 🟩 **Resolución Robusta de Mensajes por UUID:** Soporte bidireccional en `ListMessagesService` para identificadores numéricos y UUID, evitando errores de conversión 22P02 en PostgreSQL y agilizando la apertura de conversaciones.
* 🟩 **Auditoría de Migraciones y Nuevas Empresas:** 188 migraciones verificadas y sincronización automática de valores por defecto en `CreateCompanyService` para garantizar instalaciones desde cero 100% estables.
* 🟧 **Persistencia de Archivos Citados (F5):** Corrección definitiva de resolución de rutas relacionales (companyId), evitando el mensaje "Error al mostrar archivo".
* 🟧 **Paginación Indexada por Cursor y Scroll Suave:** Lote optimizado a 35 mensajes con carga progresiva y loader sutil sin tirones visuales.
* 🟧 **Blindaje y Watchdog de Conexiones:** Purga de listeners y reconexión con retroceso exponencial en Baileys, más watchdog de 30s en Evolution API.
* 🟩 **Previsualización de Multimedia en Tickets:** Emojis y etiquetas claras en el último mensaje de cada ticket sustituyendo el guión "-".
* 🟩 **Foco Continuo en Asignación de Tags:** El cursor permanece activo en el campo de etiquetas al escribir, seleccionar o presionar Enter, permitiendo ingresar múltiples tags seguidos sin perder el foco ni interrumpir la sincronización.
* 🟩 **Miniaturas Ligeras ffmpeg:** Compresión a baja resolución en chat con caché inmutable y carga bajo demanda del archivo original en alta definición.

🛠️ HERRAMIENTAS Y MÓDULOS INTEGRADOS

* 📊 **Panel de Monitoreo:** Métricas de atención, gráficos de rendimiento y reportes en tiempo real.
* 🗂️ **Gestor de Tickets y Kanban:** Organización visual por estados (Atendiendo, Esperando, Atendidos), filas y etiquetas personalizadas.
* 💬 **Respuestas Rápidas Flotantes:** Popup interactivo tipo WhatsApp Web para selección rápida.
* 📱 **Compatibilidad Móvil Total:** Interfaz responsive con anclaje firme de cabecera y barra de chat adaptada al teclado virtual.
* 🔐 **Seguridad Avanzada:** Autenticación de dos factores (2FA), gestión granular de permisos por roles y respaldo seguro de datos.