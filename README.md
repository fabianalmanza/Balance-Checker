#  Balance Checker
[Imgur](https://i.imgur.com/sGoKEVC.gif)
## Descripción del Proyecto

VoiceGuard Balance Checker es una aplicación Node.js diseñada para monitorear y gestionar el saldo de una cuenta Twilio. Esta herramienta es crucial para mantener la continuidad de los servicios de comunicación, asegurando que siempre haya fondos suficientes para las operaciones.

## Características Principales

- **Verificación Automática de Saldo**: Consulta el saldo de la cuenta Twilio en tiempo real.
- **Alertas por Correo Electrónico**: Envía notificaciones automáticas cuando el saldo cae por debajo de un umbral predefinido.
- **Autenticación Segura**: Implementa JWT para proteger las rutas y asegurar que solo usuarios autorizados puedan acceder a la información del saldo.
- **Integración con AWS SES**: Utiliza Amazon Simple Email Service para el envío confiable de correos electrónicos.
- **Diseño Modular**: Arquitectura bien estructurada que separa las preocupaciones en modelos, controladores y rutas.

## Tecnologías Utilizadas

- Node.js
- Express.js
- JWT para autenticación
- Axios para peticiones HTTP
- Nodemailer para envío de correos electrónicos
- Twilio API
- Amazon SES

## Estructura del Proyecto

```
proyecto/
│
├── controllers/
│   └── balanceController.js
│
├── middleware/
│   └── auth.js
│
├── models/
│   └── twilioModel.js
│
├── routes/
│   └── balanceRoutes.js
│
├── mailer/
│   └── mailer.js
│
├── views/
│   └── emailTemplate.js
│
├── public/
│   └── EnlanubeVG.png
│
├── .env
├── index.js
└── README.md
```

## Configuración y Uso

1. Clona el repositorio.
2. Instala las dependencias con `npm install`.
3. Configura las variables de entorno en un archivo `.env`:
   ```
   TWILIO_ACCOUNT_SID=tu_sid
   TWILIO_AUTH_TOKEN=tu_token
   JWT_SECRETO=tu_secreto_jwt
   EMAIL_USER=tu_usuario_aws_ses
   EMAIL_PASS=tu_contraseña_aws_ses
   ```
4. Ejecuta la aplicación con `node index.js`.

## Características de Seguridad

- Autenticación mediante JWT.
- Verificación de clientId para prevenir uso no autorizado de tokens.
- Uso de variables de entorno para manejar información sensible.



Desarrollado con ❤️ por [Fabian Almanza]
