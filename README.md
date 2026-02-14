📅 Sistema de Captación de Clientes y Agenda de Citas - Luciana Ramirez Systems
Este módulo de Luciana Ramirez Systems está especializado en la conversión y gestión de prospectos. Su función es automatizar el ciclo completo desde que un cliente muestra interés hasta que la cita queda agendada y registrada en el CRM.

🛠️ Funcionalidad del Proyecto
El flujo se divide en dos procesos críticos de negocio:

1. Procesamiento de Formularios de Captación
Trigger: Se activa cuando un usuario completa el form de captacion.

IA de Respuesta: Utiliza un modelo de OpenAI para procesar el texto del formulario, generando una respuesta personalizada y profesional de forma inmediata.

Notificación: El sistema utiliza el nodo enviar_mensaje vía Gmail para alertar al equipo sobre el nuevo lead interesado.

2. Automatización de Citas y CRM
Sincronización con Cal.com: El flujo detecta automáticamente cuando se crea una nueva reserva mediante el evento BOOKING_CREATED.

Confirmación Automática: Envía un correo de confirmacion de cita al cliente para asegurar la asistencia.

Registro en CRM: Los datos de la cita se insertan automáticamente en una hoja de Google Sheets que actúa como CRM, manteniendo un historial organizado de todos los clientes.

⚙️ Detalles Técnicos
Integraciones Principales: Cal.com, Gmail API y Google Sheets.

Inteligencia Artificial: Nodo de OpenAI configurado para dar respuestas humanas y coherentes a los datos captados.

Arquitectura: Event-driven (basada en eventos), lo que garantiza que no se pierda ningún prospecto en el proceso.

📋 Cómo Replicar este Ecosistema
Configurar Cal.com: Crear una cuenta y conectar el webhook a n8n mediante la URL de ngrok generada por tu servidor local.

Preparar el CRM: Crear una hoja de cálculo con columnas para Nombre, Email, Fecha y Hora de la cita.

Despliegue: Importar el archivo workflow.json en tu instancia de n8n corriendo sobre Docker.
