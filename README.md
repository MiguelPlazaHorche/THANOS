# THANOS
“App de chat básica para simular flujo DevOps completo con CI/CD y gestión ágil.”

1. Rutas principales de la aplicación:
La aplicación se estructura en tres rutas clave:
- /register: pantalla de registro de nuevos usuarios.
- /login: pantalla de inicio de sesión.
- /chat: sala de chat para usuarios autenticados.

Estas rutas se gestionan mediante React Router y permiten un flujo de navegación claro y modular.


2. Registro e inicio de sesión (modo local):
Mientras el backend no esté disponible, se simula la autenticación utilizando localStorage:
- Los datos del usuario (email y contraseña) se almacenan localmente en el navegador.
- El componente de login valida las credenciales contra los datos guardados.
- Se recomienda encapsular el estado del usuario en un contexto global (UserContext) para facilitar el acceso desde cualquier componente.

Este enfoque permite probar el flujo completo sin necesidad de un servidor.


3. Chat básico funcional:
El componente de chat permite:
- Visualizar mensajes en pantalla.
- Escribir y enviar nuevos mensajes.
- Simular una conversación entre usuarios.
Los mensajes se gestionan mediante useState y se almacenan temporalmente en memoria. Esta funcionalidad puede evolucionar fácilmente hacia una implementación en tiempo real con sockets.


4. Preparación para integración con backend:
Una vez disponible el backend y el pipeline de CI/CD, se realizarán las siguientes mejoras:
- Sustitución de localStorage por llamadas a API REST para registro e inicio de sesión.
- Persistencia de usuarios y mensajes en base de datos (MongoDB, PostgreSQL, etc.).
- Implementación de comunicación en tiempo real mediante socket.io o similar.
- Validación de tokens (JWT) y protección de rutas privadas.

Estas mejoras permitirán escalar la aplicación y simular un entorno DevOps completo.



5. Flujo visual del usuario:
Usuario → /register → /login → /chat → Mensajes


Este flujo representa el recorrido básico del usuario desde el registro hasta la interacción en el chat.




