

### 1. Información de la reunión

**Proyecto:** ____________________________  
**Cliente / Empresa:** ____________________________  
**Fecha:** ____ / ____ / ______  
**Entrevistador:** ____________________________  
**Participantes:** ____________________________

---

## 2. Objetivo del negocio

### Problema actual

- ¿Qué proceso hacen hoy manualmente?
    
- ¿Qué les hace perder tiempo o dinero?
    
- ¿Qué errores ocurren con frecuencia?
    

**Resumen del problema:**

---

### Objetivo principal

Ejemplo:

- Reducir tiempos de atención.
    
- Automatizar reservas.
    
- Centralizar información de clientes.
    
- Vender productos en línea.
    

**Objetivo definido:**

---

---

## 3. Usuarios del sistema

|Tipo de usuario|Qué hace|Nivel técnico|
|---|---|---|
|Administrador|Configura el sistema|Alto|
|Empleado|Opera diariamente|Medio|
|Cliente final|Compra / reserva / consulta|Bajo|

Agregar tantos roles como sea necesario.

---

## 4. Requisitos funcionales

### Formato recomendado

|ID|Requisito|Prioridad|
|---|---|---|
|RF-01|El usuario debe poder iniciar sesión con email y contraseña|Alta|
|RF-02|El administrador debe poder crear, editar y eliminar productos|Alta|
|RF-03|El cliente debe poder ver el historial de pedidos|Media|
|RF-04|El sistema debe enviar una notificación al confirmar una reserva|Media|

### Prioridades

- **Alta:** imprescindible para lanzar.
    
- **Media:** importante, pero puede esperar.
    
- **Baja:** deseable o futura mejora.
    

---

## 5. Requisitos no funcionales

### Rendimiento

|ID|Requisito|
|---|---|
|RNF-01|El tiempo de respuesta de las páginas principales debe ser menor a **2 segundos**|
|RNF-02|Las búsquedas deben responder en menos de **500 ms**|
|RNF-03|El sistema debe soportar al menos **100 usuarios concurrentes**|

### Seguridad

|ID|Requisito|
|---|---|
|RNF-04|Las contraseñas deben almacenarse cifradas|
|RNF-05|Todas las comunicaciones deben usar **HTTPS**|
|RNF-06|El sistema debe registrar intentos de acceso fallidos|
|RNF-07|Los usuarios solo podrán acceder a funciones autorizadas según su rol|

### Disponibilidad y confiabilidad

|ID|Requisito|
|---|---|
|RNF-08|Disponibilidad mínima del **99%**|
|RNF-09|Copias de seguridad automáticas diarias|
|RNF-10|Recuperación ante fallos en menos de **4 horas**|

### Usabilidad

|ID|Requisito|
|---|---|
|RNF-11|La interfaz debe ser responsive para móviles y escritorio|
|RNF-12|Las acciones principales deben poder realizarse en **máximo 3 clics**|
|RNF-13|Los mensajes de error deben ser claros y comprensibles|

---

## 6. Requisitos de interfaz / apariencia

### Identidad visual

- Colores de la marca: __________________
    
- Logo disponible: Sí / No
    
- Tipografía preferida: __________________
    

### Referencias visuales

- Sitio similar 1: __________________
    
- Sitio similar 2: __________________
    
- Aplicación que les gusta: __________________
    

### Pantallas necesarias

|Pantalla|Descripción|
|---|---|
|Login|Acceso de usuarios|
|Dashboard|Resumen principal|
|Gestión de clientes|Alta, baja y modificación|
|Reportes|Estadísticas y exportación|
|Configuración|Parámetros del sistema|

---

## 7. Flujo principal del negocio

### Caso de uso: Crear una reserva

1. El cliente selecciona una fecha.
    
2. El sistema muestra horarios disponibles.
    
3. El cliente confirma sus datos.
    
4. El sistema registra la reserva.
    
5. Se envía una confirmación por email o WhatsApp.
    

**Resultado esperado:** la reserva queda visible para el administrador.

---

## 8. Integraciones externas

|Servicio|Obligatorio|Observaciones|
|---|---|---|
|Mercado Pago|Sí|Cobro de reservas|
|WhatsApp|Sí|Confirmaciones automáticas|
|Google Calendar|No|Sincronización opcional|
|Sistema contable|No|Evaluar en una segunda etapa|

---

## 9. Restricciones del proyecto

- **Fecha deseada de entrega:** __________________
    
- **Presupuesto estimado:** __________________
    
- **Tecnologías requeridas por la empresa:** __________________
    
- **Hosting actual:** __________________
    
- **Dominio disponible:** Sí / No
    

---

## 10. Riesgos detectados

|Riesgo|Impacto|
|---|---|
|No existe un proceso definido actualmente|Alto|
|Los datos históricos están en Excel|Medio|
|El cliente aún no tiene proveedor de hosting|Medio|

---

## 11. Criterios de aceptación

### Módulo de autenticación

- El usuario puede iniciar sesión correctamente.
    
- Si la contraseña es incorrecta, el sistema muestra un mensaje adecuado.
    
- Después de 5 intentos fallidos, la cuenta se bloquea temporalmente.
    
- La sesión expira tras 30 minutos de inactividad.
    

### Módulo de clientes

- Crear cliente.
    
- Editar cliente.
    
- Eliminar cliente.
    
- Buscar por nombre o teléfono.
    
- Exportar listado a PDF o Excel.
    

---

## 12. Preguntas clave para cualquier entrevista

### Sobre el negocio

1. ¿Cuál es el principal problema que quieren resolver?
    
2. ¿Qué pasa si no hacen este proyecto?
    
3. ¿Cómo miden hoy el éxito de ese proceso?
    

### Sobre los usuarios

4. ¿Quién usará la aplicación todos los días?
    
5. ¿Qué conocimientos técnicos tienen?
    
6. ¿Necesitan acceso desde celular?
    

### Sobre funcionalidades

7. ¿Qué tareas son obligatorias desde el primer día?
    
8. ¿Qué funcionalidades serían “un plus”?
    
9. ¿Qué reportes o estadísticas necesitan?
    

### Sobre operaciones

10. ¿Cuántos usuarios usarán el sistema?
    
11. ¿En qué horarios tendrá más uso?
    
12. ¿Necesitan trabajar sin conexión a Internet?
    

### Sobre seguridad

13. ¿Habrá datos sensibles (DNI, pagos, direcciones, salud, etc.)?
    
14. ¿Necesitan distintos niveles de permisos?
    
15. ¿Requieren auditoría de acciones realizadas?
    

---

## 13. Resumen ejecutivo para enviar al cliente

### Necesidad detectada

---

### Solución propuesta

---

### Alcance inicial (MVP)

-  Autenticación
    
-  Gestión de usuarios
    
-  Gestión principal del negocio
    
-  Reportes básicos
    
-  Panel administrativo
    

### Funcionalidades futuras

-  Notificaciones automáticas
    
-  Integración con pagos
    
-  Aplicación móvil
    
-  Dashboard avanzado
    
-  API para terceros
    

### Próximos pasos

1. Validación de requisitos.
    
2. Diseño de pantallas (wireframes).
    
3. Estimación de tiempo y costo.
    
4. Desarrollo del prototipo.
    
5. Revisión con el cliente antes de comenzar la implementación completa.
    

---

## Consejo profesional

Durante la reunión llevá siempre una **matriz simple de prioridad**:

|Funcionalidad|¿La necesita sí o sí para trabajar?|
|---|---|
|Login|Sí|
|Gestión principal|Sí|
|Reportes|Sí|
|Tema oscuro|No|
|Notificaciones push|No|
|Integración con IA|No|

Eso te permite separar rápidamente:

- **MVP (versión mínima viable)** → lo imprescindible.
    
- **Fase 2** → mejoras importantes.
    
- **Fase 3** → ideas futuras.
    

Con esta plantilla podés documentar desde una **barbería, un sistema de turnos, un e-commerce, una app universitaria o un panel administrativo empresarial** manteniendo una estructura profesional similar a la utilizada en análisis funcional y gestión de proyectos de software.