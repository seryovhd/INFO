🎉 ¡Bienvenido a Clezapp PRO 3.7.10! 🚀
¡Gracias por confiar en Clezapp!
Estás utilizando la versión PRO de nuestra plataforma. 🎯
Con Clezapp PRO disfrutas de todas las funciones esenciales para organizar, gestionar y hacer crecer tu día a día.
Todo lo que necesitas para empezar, en un solo lugar. 🔥

🐛 ERRORES REPORTADOS
🟩 Ninguno

✅ PARCHES APLICADOS
🟥 Crítico 🟧 Alto 🟨 Normal 🟩 Bajo
    🟨 Respuestas Rápidas (Búsqueda Exacta y Similitud): Implementación de coincidencia exacta que aísla el atajo (ej. /hola) para enviarlo o seleccionarlo de inmediato sin mostrar resultados irrelevantes; búsqueda inteligente por similitud para términos parciales.
    🟨 Privacidad Multimedia: Se ocultó el nombre y extensión técnica del archivo en el chat del receptor al enviar archivos o documentos en WhatsApp.
    🟩 Dashboard Scroll: Habilitación de desplazamiento vertical (scrollbar) en la vista general del Dashboard para poder navegar y visualizar todas las métricas inferiores.
    🟩 Dashboard Contraste: Ajuste del color de fuente a blanco en las tarjetas del Dashboard para una óptima lectura.
    🟩 Contraste en Navegación: Corrección de contraste del botón de colapso de menú en tema claro y oscuro, y botón hamburguesa blanco en tema claro.
    🟩 Traducciones del Sistema: Corrección e incorporación de etiquetas multilenguaje faltantes en español, inglés y portugués (tickets.buttons.hideAll, tickets.inbox.closedAllTickets).
    🟩 Copiar Número al Portapapeles: Se incorporó un botón e ícono interactivo junto al número de WhatsApp en la cabecera de chats, visor de tickets, drawer de contacto, tarjetas Kanban y vistas previas de contacto (VCard), permitiendo copiar el número con un solo clic y confirmación visual inmediata.
    🟧 Edición de Usuarios y Contactos (Ubuntu/PostgreSQL): Corrección de validación de empresa en actualización de usuarios que provocaba rechazo por empresa inexistente; saneamiento y validación tolerante de números en edición de contactos sin depender de que WhatsApp esté activo; nueva migración de integridad 20261018150000 para asegurar la presencia de todas las columnas en Users y Contacts en servidores Ubuntu.
    🟩 Contraste de Mensaje Privado (Tema Oscuro): Corrección de contraste en el campo de texto al activar el modo Privado; el texto escrito, el cursor y el marcador de posición ahora se muestran en color oscuro/negro sobre el fondo amarillo claro, garantizando una visibilidad óptima.
    🟩 Visor Global de Foto de Perfil HD: Integración de visor interactivo en alta resolución en todas las miniaturas de contacto del sistema (Tickets en Atendiendo, Esperando, Atendidos, Buscador, Cabecera de Chat, Tabla de Contactos, Tablero Kanban y Tarjetas VCard), incluyendo aislamiento de clics (stopPropagation), descarga directa y sincronización HD con WhatsApp.
    🟩 Destacado WhatsApp en Número de Cabecera (Badge / Pill): Implementación de cápsula distintiva en verde WhatsApp con contraste automático (verde bosque corporativo #008069 en tema claro y verde neón #25D366 con resplandor en tema oscuro) para priorizar la visibilidad inmediata del número del cliente.
    🟨 Alerta Visual de Números @lid No Actualizados: La cápsula de número en la cabecera del chat cambia automáticamente a color rojo con ícono de advertencia (⚠️) y tooltip informativo cuando el contacto tiene un identificador provisional (@lid) pendiente de actualizar a su número telefónico real.
    🟧 Aceleración Web y Code-Splitting: División modular del frontend mediante React.lazy y Suspense reduciendo el bundle inicial en un 36% (de 1.19 MB a 758 KB) con 40+ chunks bajo demanda, acelerando el arranque en conexiones móviles y de escritorio.
    🟩 Caché Inmutable de Alto Rendimiento: Configuración de servidor express con compresión GZIP y cabeceras de caché inmutable (Cache-Control: public, max-age=31536000, immutable) para recursos estáticos con hash, garantizando navegación instantánea (< 0.5s) y cero saturación del VPS.
    🟧 Blindaje de Conexión Baileys: Implementación de Keep-Alive proactivo cada 25 segundos, supresión de sincronización innecesaria de historial masivo (syncFullHistory: false) y filtrado de eventos ruidosos (@newsletter y @call) para conexiones 24/7 sin desconexiones intermitentes.
    🟨 Estabilidad y Poda de Memoria en Evolution API: Implementación de poda automática de buffers y Sets en EvolutionMonitor para prevenir saturación de memoria RAM y caídas del proceso en el servidor.
    🟧 Índices Compuestos PostgreSQL en Messages: Nueva migración 20261019203000 que añade índices compuestos de alto rendimiento (idx_messages_company_ticket_createdAt, idx_messages_company_read, idx_messages_remoteJid), acelerando la carga y navegación de chats con miles de mensajes a menos de 10ms.
    🟥 Desconexión y Eliminación de Conexiones Baileys (Error 400 & Bad MAC): Corrección de la validación de empresa en ShowWhatsAppService y controladores que arrojaba error 400 al intentar desconectar o eliminar conexiones creadas con companyId nulo o gestionadas por SuperAdmin; reestructuración de removeWbot para expulsar inmediatamente de la memoria (sessions.splice) sesiones con llaves corruptas (Bad MAC) evitando bucles infinitos en PM2; y adición de limpieza previa en cascada en DeleteWhatsAppService (Baileys, BaileysChats, WhatsappQueue) para prevenir bloqueos por Foreign Key en PostgreSQL.
    🟩 Envío Instantáneo de Mensajes (Optimistic UI): Optimización del flujo de chat (MessageInput y MessageInputCustom) para vaciar el campo de texto en 0ms apenas se presiona Enter o Enviar, permitiendo al operador seguir escribiendo el siguiente mensaje sin pausas ni bloqueos mientras el envío se procesa en segundo plano, con restauración automática en caso de corte de red; y eliminación de consultas redundantes a la base de datos en SendWhatsAppMessage.
    🟩 Memoización y Aislamiento de Renderizado (React.memo): Optimización de TicketListItemCustom, TicketsListCustom, MarkdownWrapper, ModalImageCors y AvatarWithPreview mediante comparadores puros; suprime re-renderizados innecesarios de la lista de conversaciones al recibir mensajes o cambiar de chat, reduciendo en más del 80% el uso de CPU.
    🟩 Caché en Memoria de Conversaciones Recientes (0ms Ticket Switch): Implementación de almacenamiento LRU en MessagesList que hidrata al instante los mensajes de los últimos tickets consultados, eliminando por completo pantallas en blanco, parpadeos y esperas de red al alternar entre chats.
    🟩 Carga Perezosa y Decodificación Asíncrona (Lazy & Async Decode): Asignación de loading='lazy' y decoding='async' en todas las fotos de perfil y elementos multimedia para no bloquear el hilo de renderizado del navegador durante desplazamientos rápidos.
    🟨 Debounce Inteligente y Limpieza de Sockets: Reemplazo de desconexiones destructivas de Socket.IO por desvinculación selectiva de eventos (socket.off) y debounce de 1500ms en la sincronización en background de tickets para proteger la interfaz y el servidor contra ráfagas masivas de eventos.
    🟩 Orden Cronológico Estricto de Mensajes (sortMessages): Implementación de comparador cronológico absoluto por createdAt ASC en todas las transiciones del reducer de mensajes (HYDRATE_CACHED, LOAD_MESSAGES, ADD_MESSAGE, UPDATE_MESSAGE); garantiza que mensajes antiguos nunca se intercalen ni aparezcan al final de la conversación bajo ninguna circunstancia.
    🟩 Anclaje Instantáneo al Fondo del Chat (0ms Scroll Snap): Desplazamiento inmediato al último mensaje (scrollTop = scrollHeight) al entrar o alternar entre conversaciones sin animaciones lentas que generen desfasajes visuales o dejen la vista a mitad de la conversación.
    🟨 Bloqueo de Paginación en Carga Inicial (isInitialLoad): Protección del detector de desplazamiento superior en MessagesList; previene la solicitud accidental de páginas previas durante la apertura del chat, activando la paginación de mensajes antiguos únicamente cuando el operador hace scroll intencional hacia arriba.
    🟧 Visualización y Soporte de Stickers WhatsApp (Baileys y Evolution API): Corrección crítica en la descarga y guardado de stickers entrantes resolviendo el fallo de DNS de WhatsApp (a.whatsapp.net a mmg.whatsapp.net); integración de envío de stickers WebP vía endpoint nativo /message/sendSticker en Evolution API y buffer nativo en Baileys; ajuste de proporción a 200px × 200px con renderizado transparente (sin burbuja de chat ni bordes) y recuperación de stickers históricos corruptos.
    🟨 Visor Multimedia Proporcional Unificado (Material-UI Dialog): Sustitución del visor invasivo de pantalla completa (react-modal-image) por un modal centrado con proporciones nativas (object-fit: contain, max 88vw x 82vh) y fondo desenfocado; acotamiento de videos y GIFs en burbujas de chat y mensajes citados a dimensiones controladas (max 320x240px) para evitar desbordes de pantalla en resoluciones altas.
    🟧 Blindaje de Deshabilitar Chatbot (disableBot / Atención 100% Humana): Inclusión de atributo disableBot en ShowTicketService y ShowTicketFromUUIDService que corregía la omisión del parámetro en la resolución de tickets; anulación total de integraciones de fila (Typebot, N8N, Webhook, Dialogflow), prompts de IA (OpenAI/DeepSeek), submenús de opciones y FlowBuilder para contactos con bot desactivado; supresión absoluta de saludos de bienvenida de fila o canal (Opción B: silencio total), transferencias automáticas y mensajes de despedida o calificación al cerrar el ticket.

✨ NUEVAS FUNCIONES
🔧 INGENIERÍA INVERSA
    ⚡ Búsqueda y Selección Inteligente de Respuestas Rápidas: Coincidencias exactas aisladas y similitud por relevancia tanto en Modo Carrusel Tradicional como en Popup Flotante (estilo WhatsApp Web), con soporte para envío directo con Enter.
    🖼️ Visor Lightbox HD de Fotos de Perfil: Previsualización interactiva de avatar en alta resolución con controles de descarga y visualización limpia sin seleccionar ni abrir tickets.
    🟢 Cápsula Destacada de WhatsApp: Resaltado visual en verde WhatsApp corporativo en la cabecera de chat con botón de copiado rápido a un clic.
    🔴 Detección Inteligente de Contactos @lid: Alerta visual instantánea para identificar y gestionar contactos que aún no han compartido su número telefónico real.
    ⚡ Arquitectura Web de Carga Asíncrona (Code-Splitting): Carga perezosa de rutas y componentes secundarios para un inicio de sesión y apertura de aplicación ultrarrápida.
    🛡️ Monitor Proactivo Anti-Desconexión: Protocolos Keep-Alive y control de memoria integrados para garantizar estabilidad permanente en los motores de WhatsApp.
    🚀 Envío Optimista Ultrarrápido (0ms): Vaciado instantáneo del campo de redacción al dar Enter, permitiendo redactar fluidamente múltiples mensajes continuos sin tiempos de espera.
    🛡️ Purgado y Auto-Recuperación de Sesiones: Algoritmo de desvinculación forzada en caliente que expulsa llaves corruptas (Bad MAC) y registros huérfanos al desconectar o eliminar conexiones de WhatsApp.
    ⚡ Alternancia Instantánea de Chats (0ms Switch): Memoria caliente en frontend que abre conversaciones recientes en cero milisegundos sin parpadeo.
    💎 Máxima Fluidez de Interfaz (60 FPS): Desacople de re-renders de tickets, carga perezosa de medios y scroll suave estilo WhatsApp Web.
    ⏱️ Cronología Absoluta de Chat: Blindaje de ordenamiento temporal que garantiza que el flujo de mensajes siempre respete su secuencia real de envío y recepción.
    🎯 Enfoque Preciso de Últimos Mensajes: Apertura directa en el punto más reciente de la conversación con 0 ms de retraso sin saltos hacia mensajes anteriores.
    💟 Motor Nativo de Stickers WhatsApp: Compatibilidad bidireccional completa (envío y recepción) con Baileys y Evolution API, visualización flotante transparente de 200px y persistencia confiable en disco.
    🎬 Visor Cinemático y Proporcional de Medios: Reproducción y visualización elegante de fotos, videos, GIFs animados y stickers sin distorsión de formato, con barra de acciones rápidas, botón de descarga y cierre intuitivo.
    🔇 Modo Silencio Absoluto y Atención 100% Humana (disableBot): Desconexión total de automatizaciones, flujos e integraciones al ingresar a cualquier fila o departamento, derivando al cliente de forma directa, limpia y silenciosa a la bandeja de operadores humanos sin despedidas ni encuestas automáticas al finalizar.

1. Panel de Monitoreo
    📊 Gráficos en Tiempo Real: Visualización de las métricas más importantes de tu plataforma.
    📊 Estadísticas: Tendencias y comparativas para entender mejor el rendimiento.
    🚀 En Tiempo Real: Actualizaciones instantáneas sin necesidad de recargar la página.

2. Centro de Reportes
    🐛 Reportes de Errores: Sistema completo para reportar y gestionar errores en tiempo real.
    🗂️ Ticketing: Gestión de tickets con estados, prioridades y asignaciones.
    📝 Comentarios y Seguimiento: Comunicación fluida para resolver problemas eficientemente.
    📊 Métricas de Errores: Análisis detallado de los errores reportados.

3. Funciones de Productividad
    🔍 Buscador Avanzado: Búsqueda inteligente en conversaciones con filtros avanzados.
    💬 Respuestas Rápidas Mejoradas: Modo flotante interactivo y carrusel con filtrado por atajo exacto y similitud.
    🔄 Reenvío Masivo de Mensajes: Envía mensajes a múltiples contactos de forma rápida y eficiente.
    🧠 ChatIA: Asistente con IA para consultas rápidas y soporte en tiempo real.
    ⚙️ Configuración del Perfil: Gestión completa de la información personal.
    🔓 Autenticación de Dos Factores: Seguridad adicional para proteger tu cuenta.
    🎨 Temas Personalizados: Elige el tema que más te guste para personalizar tu experiencia.
    📱 Modo Smartphone: Optimizado para dispositivos móviles con acceso rápido a funciones esenciales.
    🌍 Selector de Idiomas: Configura tu idioma preferido con soporte multilingual.
    📤 Exportación de Datos: Exporta tus conversaciones y datos importantes a archivos locales.
    🔄 Reimportación de Datos: Restaura tus datos a partir de archivos locales.