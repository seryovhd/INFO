🎉 ¡Bienvenido a Clezapp PRO 3.7.21! 🚀
¡Gracias por confiar en Clezapp! Estás utilizando la versión PRO de nuestra plataforma de atención omnicanal, diseñada para ofrecer la máxima velocidad, estabilidad y productividad para tu equipo. 🎯

✨ VENTAJAS Y VIRTUDES DE CLEZAPP PRO
💎 Rendimiento Ultra-Fluido (60 FPS & 0ms Reactivity)
* **Recepción y Actualización Instantánea de Mensajes Editados (0ms Reactivity):** Soporte en vivo para mensajes editados en WhatsApp tanto en Baileys como en Evolution API; el contenido se actualiza inmediatamente en pantalla y en la base de datos sin requerir recargar la página, mostrando la marca y hora de modificación.
* **Resolución Unificada de Privacidad LID / JID (Cero Conversaciones Duplicadas):** Motor inteligente de identidad para WhatsApp que resuelve identificadores de privacidad (@lid) al número de teléfono real tanto en conexiones directas de Baileys como en webhooks de Evolution API. Auto-fusión en segundo plano de historiales y mensajes huérfanos con notificación en tiempo real sin intervención de los asesores.
* **Envío Inmediato (Optimistic UI):** Los mensajes se despachan en 0ms; el operador redacta continuamente sin pausas ni esperas de servidor.
* **Alternancia Instantánea de Chats (SWR 0ms Ticket Switch):** Memoria en caliente que renderiza contactos, cabeceras, etiquetas y mensajes previos en cero milisegundos, eliminando pantallas de "cargando..." y parpadeos al alternar rápidamente entre chats, sin afectar la suavidad ni el desplazamiento original.
* **Elevación de Ticket en Tiempo Real (0ms Lift):** El chat salta automáticamente al primer lugar de la bandeja apenas llega o se envía un mensaje.
* **Arquitectura Asíncrona (Code-Splitting):** Carga modular bajo demanda que reduce el peso inicial en más del 36%, optimizando el arranque en móviles y escritorio.

🛡️ Estabilidad 24/7 y Blindaje Anti-Caídas
* **Blindaje de Conexiones WhatsApp (Baileys & Evolution API):** Keep-Alive proactivo cada 20-25s, purga total de memoria ante sesiones cerradas y monitorización pasiva (watchdog) de 30s que libera hasta un 90% de CPU en el servidor.
* **Heartbeat Ultra-Rápido y Detección de Caídas:** Reducción del ciclo de detección de microcortes de 36s a 10s con reconexión progresiva en 1 segundo y tolerancia avanzada a suspensión de pestañas en el navegador.
* **Suscripción Garantizada en Tiempo Real:** Recepción fluida de mensajes entrantes y salientes en tiempo real para administradores, supervisores y operadores asignados a colas o tickets pendientes, sin bloqueos de sala.
* **Protección Anti-Saturación de Grupos:** Descarte inmediato en paso 0 de mensajes de grupos masivos con caché en memoria, evitando sobrecargar RAM y CPU.

📦 Gestión Multimedia Inteligente y Ultraligera
* **Miniaturas Dinámicas (~12 KB):** Reducción de ancho de banda del 99.4% en fotos, videos y stickers en burbujas de chat; el original HD se descarga únicamente al abrir el visor.
* **Visor Cinemático Proporcional:** Vista previa centrada con proporción original para imágenes, videos, audios y stickers sin distorsiones ni desbordes.
* **Identificación Visual en Bandeja:** Identificadores con emojis (📷 Imagen, 📹 Video, 🎵 Audio, 💟 Sticker, 📄 Archivo) para saber al instante el contenido del último mensaje.
* **Persistencia Total de Citas:** Carga garantizada de multimedia citada incluso al actualizar la página (F5).

⚡ Base de Datos de Alta Eficiencia (O(1))
* **Paginación Continua por Cursor:** Navegación por fecha e identificador (beforeCreatedAt / beforeId) en lugar de saltos pesados de OFFSET; navegación fluida en historiales con miles de mensajes.
* **Consultas Insensibles a Mayúsculas/Minúsculas:** Búsqueda rápida optimizada con funciones de texto insensible en PostgreSQL para etiquetas y respuestas rápidas.
* **Índices Compuestos de Alto Desempeño:** Consultas y filtros acelerados en base de datos ejecutados en menos de 10ms.
* **Resolución Polimórfica UUID/ID:** Consultas de mensajes optimizadas para soportar identificadores numéricos y UUID sin fallos de conversión de tipos.

🔇 Control Operativo y Productividad
* **Borradores Persistentes en Chats (Drafts 0ms):** Preservación automática de textos no enviados al cambiar de conversación o recargar la página (F5), con identificación visual en verde `Borrador: [texto]` en la bandeja de tickets estilo WhatsApp Web y Telegram.
* **Búsqueda Inteligente por Relevancia en Respuestas Rápidas:** Algoritmo de coincidencia estricta con la columna de acceso directo (`Exact Match` -> `Starts-With` -> `Contains`) con soporte nativo para comandos con o sin barra diagonal (ej. `/promo` o `promo`).
* **Buscador Insensible en Etiquetas:** Localización inmediata de tags sin distinción entre mayúsculas y minúsculas con cálculo de paginación blindado.
* **Cabecera Colapsable y Barra Ultra-Compacta:** Pestaña deslizante con Chevron (Up/Down) en cabecera de tickets para alternar entre vista completa y modo compacto (46px), maximizando el espacio de lectura.
* **Identificador Visual NO-BOT:** Etiqueta roja en bandeja para detectar al instante los contactos con chatbot desactivado.
* **Control Flexible de Etiquetas en Ajustes:** Opciones en ajustes para mostrar u ocultar selectivamente etiquetas de conexión, agentes, tags y última interacción.
* **Modo Silencio Absoluto (disableBot):** Desconexión integral de bots, respuestas automáticas y encuestas de salida para una atención 100% humana y limpia.
* **Privacidad de Archivos:** Ocultación del nombre técnico de archivos adjuntos en el chat del receptor.

📋 NOVEDADES Y MEJORAS DESTACADAS
* 🟩 **Soporte Integral para Mensajes Editados en Tiempo Real (Baileys & Evolution API - v3.7.21):** Captura instantánea de eventos de edición de mensajes de WhatsApp enviados por los clientes. El sistema detecta y procesa la modificación en segundo plano, actualizando el contenido en la base de datos, registrando la marca de edición, sincronizando el último mensaje en la bandeja de tickets y emitiendo el evento por WebSockets para que el chat abierto y la lista de conversaciones reflejen el nuevo texto en vivo con su distintivo de edición.
* 🟩 **Resolución Automática Unificada de Identidad LID/JID y Auto-Fusión (v3.7.20):** Implementación integral del motor de identidades para WhatsApp, compatible tanto con conexiones Baileys como con Evolution API. Los mensajes entrantes con identificadores de privacidad (@lid) se analizan en 0ms y se resuelven contra metadatos del paquete, diccionario persistente en base de datos y almacén de sesiones. Si existe una conversación o contacto provisional generado previamente por un LID huérfano, el sistema realiza una fusión automática en segundo plano: traspasa mensajes, tickets y etiquetas al contacto con el número real y actualiza la vista de los asesores por WebSockets en vivo, erradicando chats duplicados sin necesidad de intervención manual.
* 🟩 **Transición Instantánea sin Bloqueos y Blindaje de Sockets en Vivo (v3.7.18):** Implementación de memoria en caliente para datos de tickets. Al alternar entre conversaciones, los datos del chat se muestran inmediatamente (0ms) sin activar el spinner de carga bloqueante ("cargando..."), revalidando en segundo plano de manera transparente y sin alterar la suavidad ni el desplazamiento visual. Se optimizó el heartbeat de sockets a 10s con reconexión progresiva en 1s ante microcortes, se flexibilizó el acceso a salas en tiempo real para que operadores y supervisores en colas o tickets pendientes reciban eventos en vivo sin restricciones, y se securizó la confirmación de mensajes salientes.
* 🟩 **Buscadores de Alta Precisión en Respuestas Rápidas y Etiquetas (v3.7.18):** Reorientación integral del buscador en respuestas rápidas para coincidir exclusivamente con la columna de acceso directo, admitiendo términos con o sin barra diagonal inicial y aplicando ordenamiento algorítmico por relevancia (coincidencia exacta primero, luego inicios y finalmente contenidos). En etiquetas, se implementó búsqueda insensible a mayúsculas y minúsculas en base de datos, estabilizando el cálculo de agrupamiento y conteo.
* 🟩 **Sistema de Borradores Persistentes y Reactivos en Vivo (WhatsApp & Telegram Style - v3.7.17):** Guardado automático en memoria local de textos redactados no enviados al cambiar de conversación o recargar la página (F5). En la bandeja lateral, el chat muestra en verde WhatsApp el prefijo `Borrador: [texto]` sin retrasos ni llamadas al servidor. Al regresar a la conversación, el mensaje se restaura de inmediato en la caja de texto con foco activo, depurándose automáticamente al enviarse.
* 🟩 **Blindaje Integral y Resiliencia en Envío de Tickets (v3.7.16):** Sanitización y validación estricta en el despacho de mensajes, notas de voz, adjuntos y respuestas rápidas con soporte bidireccional (UUID y numérico), previniendo errores por identificadores no definidos al abrir chats rápidamente sin requerir recargar la página.
* 🟩 **Transición Fluida de Tickets y Carga Continua:** Eliminación de parpadeos de esqueletos de carga al alternar entre chats; la cabecera actual se conserva suavemente durante la carga en segundo plano sin reiniciar ni recargar la vista.
* 🟩 **Sincronización Inteligente con Caché de Memoria Dual:** Indexación polimórfica en caliente de mensajes para eliminar el retraso de sincronización en bandejas con alto volumen de conversaciones.
* 🟩 **Cancelación Automática de Peticiones Obsoletas:** Descarte instantáneo de solicitudes en vuelo de mensajes y tickets al navegar rápidamente entre conversaciones, previniendo sobrecarga de red y estados de carga colgados.
* 🟩 **Indicador de Progreso Suave:** Animación de carga circular sutil con desvanecimiento gradual en la bandeja de chat, eliminando apariciones y desapariciones bruscas.
* 🟩 **Optimización de Renderizado en Bandeja de Tickets:** Actualizaciones por lote y referencias estables en filtros de tickets para evitar re-renderizados innecesarios ante ráfagas de eventos de WebSocket.
* 🟩 **Cabecera Colapsable y Barra Ultra-Compacta en Tickets:** Pestaña interactiva para alternar entre vista completa y barra ultra-compacta (46px), maximizando el espacio de lectura en pantalla con transiciones suaves y memoria de estado.
* 🟩 **Etiqueta Roja "NO-BOT" en Tickets:** Identificador visual en vivo para contactos con chatbot deshabilitado, optimizado para actualización instantánea vía WebSockets.
* 🟩 **Control de Visibilidad de Etiquetas en Ajustes:** Parametrización en panel de opciones para mostrar u ocultar la etiqueta de última interacción, canal de conexión, nombre de agente asignado y tags de clasificación.
* 🟩 **Resolución Robusta de Mensajes por UUID:** Soporte bidireccional para identificadores numéricos y UUID, agilizando la apertura y consulta de conversaciones.
* 🟩 **Auditoría Integral de Migraciones y Nuevas Instalaciones:** 190 migraciones verificadas y sincronizadas al 100% entre TypeScript y distribución compilada, con métodos de reversión y control de integridad para garantizar despliegues limpios y actualizaciones continuas sin errores.
* 🟧 **Persistencia de Archivos Citados:** Resolución garantizada de rutas relacionales para archivos adjuntos citados, evitando mensajes de error al recargar la página.
* 🟧 **Paginación Indexada por Cursor y Scroll Suave:** Lote optimizado a 35 mensajes con carga progresiva y navegación fluida sin tirones visuales.
* 🟧 **Blindaje y Monitoreo de Conexiones:** Purga de escuchadores y reconexión con retroceso exponencial en WhatsApp, optimizando el rendimiento del servidor.
* 🟩 **Previsualización de Multimedia en Tickets:** Emojis y etiquetas claras (imágenes, videos, audios, stickers y archivos) en el último mensaje de cada ticket sustituyendo guiones vacíos.
* 🟩 **Foco Continuo en Asignación de Tags:** El cursor permanece activo en el campo de etiquetas al escribir, seleccionar o presionar Enter, permitiendo ingresar múltiples tags seguidos sin perder el foco.
* 🟩 **Miniaturas Ligeras de Alta Eficiencia:** Compresión ligera en chat con caché inmutable para ahorro de ancho de banda y carga bajo demanda del archivo original en alta definición.

🛠️ HERRAMIENTAS Y MÓDULOS INTEGRADOS
* 📊 **Panel de Monitoreo:** Métricas de atención, gráficos de rendimiento y reportes en tiempo real.
* 🗂️ **Gestor de Tickets y Kanban:** Organización visual por estados (Atendiendo, Esperando, Atendidos), filas y etiquetas personalizadas.
* 💬 **Respuestas Rápidas Flotantes:** Popup interactivo tipo WhatsApp Web para selección rápida.
* 📱 **Compatibilidad Móvil Total:** Interfaz responsive con anclaje firme de cabecera y barra de chat adaptada al teclado virtual.
* 🔐 **Seguridad Avanzada:** Autenticación de dos factores (2FA), gestión granular de permisos por roles y respaldo seguro de datos.