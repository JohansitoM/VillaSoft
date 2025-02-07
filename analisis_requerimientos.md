# **Documentación del Sistema de Administración del Conjunto Residencial "Villa del Sol"**

## **1. Información General del Proyecto**

- **Nombre**: VillaSoft  
- **Versión**: 1.0  
- **Fecha**: 2025-01-30  

---

## **2. Alcance**

Este sistema está diseñado para facilitar la administración del conjunto residencial **"Villa del Sol"** mediante la digitalización de procesos clave.  

### **Incluye:**  
- Gestión de propietarios e inquilinos.

- Control de acceso y registro de visitantes.

- Administración de pagos y estado de cuenta de propietarios.

- Comunicación entre la administración y los residentes.

- Gestión de apartamentos y usuarios del sistema.

- Autenticación y seguridad.

- Dashboard administrativo.
### **Fuera del Alcance:**  
- Funcionalidades de mantenimiento de infraestructura.  

- Integración con hardware de acceso biométrico o tarjetas de acceso.  

- Módulo avanzado de contabilidad o facturación.  

---

## **3. Módulos del Sistema**

### **3.1 Módulo de Gestión de Propietarios e Inquilinos**  

**Descripción**: Este módulo permite gestionar los propietarios e inquilinos del conjunto residencial.  

#### **Requerimientos Funcionales**  
|**Código**|**Requerimiento**|**Rol**|**Descripción**|**Prioridad**
|--------|--------|---------|--------|--------|
|**RF_GPI01**|Registrar, editar y eliminar sus inquilinos|Propietario|Solo podrá registrar inquilinos en su apartamento, podrá editar todos los datos de sus inquilinos, excepto la cedula y sus apartamentos|Alta|
|**RF_GPI02**|Registrar, editar y eliminar propietarios|Administración|Debe permitir la edición de todos los datos y de todos los tipos de usuario|Alta|
|**RF_GPI03**|Actualizar datos personales| Propietario/Inquilino|Podrán actualizar todos sus datos excepto la cédula y el apartamento|Alta|
|**RF_GPI04**|El sistema debe permitir buscar propietarios o inquilinos|Administrador / propietario / vigilante /inquilino|Administrador: Acceso a todos los datos. Propietario: Solo sus inquilinos. Vigilante: Solo por apartamento para control. Inquilino: Solo su información.|Media|


#### **Requerimientos No Funcionales**  

|**Código**|**Requerimiento**|
|----------|-----------------|
|**RNF_GPI01**|La información de los propietarios e inquilinos debe ser protegida mediante autenticación segura.  |
|**RNF_GPI02**|Solo los administradores pueden modificar datos de propietarios. | 
|**RNF_GPI03**|La búsqueda debe estar disponible para todos los usuarios autenticados.|

#### **Criterios de Aceptación**  

- Los propietarios solo pueden registrar inquilinos en apartamentos donde sean titulares.  
- Los datos de cédula y apartamento no deben poder modificarse una vez registrados.  
- La búsqueda de propietarios e inquilinos debe ser rápida y eficiente, con un tiempo de respuesta inferior a 2 segundos.  

---

### **3.2 Módulo de Control de Acceso y Seguridad**  

**Descripción**: Este módulo permite gestionar el control de acceso y seguridad del conjunto residencial.  

#### **Requerimientos Funcionales**  

|**Código**|**Requerimiento**|**Rol**|**Descripción**|**Prioridad**
|--------|--------|---------|--------|--------|
|**RF_CAS01**|Registrar la entrada y salida de visitantes|Vigilante|En el registro se incluirá el nombre, cédula, apartamento a visitar y hora de ingreso del visitante|Alta|
|**RF_CAS02**|Pre-registrar visitantes para agilizar su acceso|Propietarios / Inquilinos|Podrán registrar previamente visitantes para agilizar su acceso|Media|
|**RF_CAS03**|Consultar el historial de visitas|Vigilante / Administración|Consultas por apartamento o visitante|Media|
|**RF_CAS04**|Consultar el historial de visitas|Inquilino|Por el nombre del visitante|Baja|  
|**RF_CAS05**|Consultar el historial de visitas|Propietario|Consultar el historial de visitas en sus apartamentos, permitiendo búsqueda por nombre de visitante y número de apartamento.|Baja|  
|**RF-CAS06**|Reportar incidentes de seguridad en el sistema|Vigilante|El reporte se debe notificar a la administración|Alta|

#### **Requerimientos No Funcionales**  
|**Código**|**Requerimiento**|
|--------------|--------------|
|**RNF-CAS01**|La información de acceso debe almacenarse en tiempo real.  
|**RNF-CAS02**|Solo vigilantes y administradores pueden registrar y ver el historial de visitantes.  

#### **Criterios de Aceptación**  

- Los registros de entrada y salida deben quedar almacenados con sello de tiempo.  
- Solo se deben permitir accesos a visitantes previamente autorizados o registrados.  
- Los reportes de incidentes deben poder visualizarse en un panel administrativo.  

---

### **3.4 Módulo de Comunicación y Notificaciones**  

**Descripción**: Este módulo permite gestionar las comunicaciones y notificaciones del conjunto residencial. 

#### **Requerimientos Funcionales**  

| **Código**   | **Requerimiento** | **Rol** | **Descripción** | **Prioridad** |
|-------------|------------------|---------|----------------|--------------|
| **RF-CN01** | Enviar notificaciones sobre eventos, mantenimientos o avisos | Administración | Permitirá enviar mensajes a propietarios e inquilinos con información relevante sobre el conjunto | Alta |
| **RF-CN02** | Enviar quejas o solicitudes | Propietario/Inquilino | Podrán enviar quejas o solicitudes a la administración para su gestión | Alta |
| **RF-CN03** | Visualizar historial de comunicaciones | Administración/Propietario/Inquilino | Permitirá consultar el historial de notificaciones y mensajes enviados o recibidos | Media |
| **RF-CN04** | Enviar correo de bienvenida tras el registro | Sistema | Se enviará un correo automático a cada usuario registrado en la app con instrucciones y bienvenida | Alta |

#### **Requerimientos No Funcionales**  

| **Código**   | **Requerimiento** |
|-------------|------------------|
| **RNF-CN01** | Las notificaciones deben enviarse por correo electrónico y/o en la plataforma |

#### **Criterios de Aceptación**  

- Los mensajes deben enviarse a todos los destinatarios en un tiempo máximo de 1 minuto.  
- El historial de comunicaciones debe estar disponible por un período mínimo de 12 meses.    

---

### **3.5 Módulo de Administración del Conjunto**  

**Descripción**: Este módulo permite gestionar la administración del conjunto residencial.  

#### **Requerimientos Funcionales**  

| **Código**   | **Requerimiento** | **Rol** | **Descripción** | **Prioridad** |
|-------------|------------------|---------|----------------|--------------|
| **RF-AC01** | Registrar, modificar y eliminar apartamentos | Administración | Permitirá gestionar los apartamentos disponibles en el sistema | Alta |
| **RF-AC02** | Asignar propietarios a apartamentos | Administración | Cada apartamento deberá tener un único propietario registrado en el sistema | Alta |
| **RF-AC03** | Gestionar usuarios y permisos | Administración | Permitirá crear, modificar y asignar permisos a los usuarios del sistema | Alta |
| **RF-AC04** | Visualizar información de apartamentos e inquilinos | Propietario | Cada propietario podrá ver los apartamentos donde sea titular y los inquilinos registrados en ellos | Media |

#### **Requerimientos No Funcionales**  

| **Código**   | **Requerimiento** |
|-------------|------------------|
| **RNF-AC01** | Solo la administración puede acceder a la gestión de apartamentos y usuarios |

#### **Criterios de Aceptación**  

- Solo los administradores pueden modificar o eliminar apartamentos.  
- Cada apartamento debe tener un único propietario registrado en el sistema.  
- Los cambios en la asignación de propietarios deben quedar registrados con un historial de modificaciones.  

### **3.6 Módulo de Pagos y Finanzas**  

**Descripción**: Este módulo permite gestionar los pagos y finanzas del conjunto residencial.  

#### **Requerimientos Funcionales**  

| **Código**   | **Requerimiento** | **Rol** | **Descripción** | **Prioridad** |
|-------------|------------------|---------|----------------|--------------|
| **RF-PF01** | Registrar y actualizar pagos de cuotas | Administración | Permite registrar y actualizar los pagos de cuotas de administración por apartamento. | Alta |
| **RF-PF02** | Consultar estado de cuenta | Propietario | Permite a los propietarios visualizar el estado de cuenta de su apartamento. | Alta |
| **RF-PF03** | Notificar pagos pendientes | Sistema | Envía notificaciones automáticas a los propietarios con pagos pendientes. | Media |
| **RF-PF04** | Generar reportes de pagos y deudas | Sistema / Administración | Permite generar reportes financieros por apartamento. | Alta |
| **RF-PF05** | Pago en línea | Propietario | Los propietarios pueden pagar sus cuotas en línea a través de PSE o tarjeta de débito/crédito. | Alta |

#### **Requerimientos No Funcionales**  

| **Código**   | **Requerimiento** |
|-------------|------------------|
| **RNF-PF01** | El sistema debe permitir exportar reportes en formatos PDF y Excel. |
| **RNF-PF02** | La información financiera debe estar protegida mediante encriptación. |

#### **Criterios de Aceptación**  

- Los pagos deben reflejarse en el estado de cuenta en un tiempo máximo de 5 minutos.  
- Los reportes de pagos y deudas deben poder descargarse en formatos PDF y Excel.  
- Solo los propietarios pueden acceder a la información de pagos de su apartamento.  

### **3.X Módulo de Autenticación y Control de Acceso**  

**Descripción**: Este módulo gestiona la autenticación segura de los usuarios, asegurando el acceso autorizado al sistema.  

#### **Requerimientos Funcionales**  

| **Código**   | **Requerimiento** | **Rol** | **Descripción** | **Prioridad** |
|-------------|------------------|---------|----------------|--------------|
| **RF-AC01** | Inicio de sesión | Todos los usuarios | Permite a los usuarios autenticarse en el sistema con correo y contraseña. | Alta |
| **RF-AC02** | Recuperación de contraseña | Todos los usuarios | Permite restablecer la contraseña a través del correo electrónico registrado. | Alta |
| **RF-AC03** | Gestión de roles y permisos | Administración | Define los accesos y permisos de cada usuario dentro del sistema. | Alta |

#### **Requerimientos No Funcionales**  

| **Código**   | **Requerimiento** |
|-------------|------------------|
| **RNF-AC01** | La autenticación debe realizarse con protocolos de seguridad como JWT o OAuth2. |
| **RNF-AC02** | Las contraseñas deben almacenarse encriptadas. |

#### **Criterios de Aceptación**  

- El sistema debe validar credenciales correctamente antes de conceder acceso.  
- Solo los usuarios con permisos adecuados pueden acceder a módulos restringidos.  

---

### **3.X Módulo de Dashboard de Administración**  

**Descripción**: Este módulo proporciona una vista general de la administración del conjunto residencial, con acceso rápido a reportes y notificaciones.  

#### **Requerimientos Funcionales**  

| **Código**   | **Requerimiento** | **Rol** | **Descripción** | **Prioridad** |
|-------------|------------------|---------|----------------|--------------|
| **RF-DA01** | Visualizar resumen de pagos | Administración | Muestra un reporte de pagos recibidos, pendientes y estado financiero del conjunto. | Alta |
| **RF-DA02** | Ver incidentes reportados | Administración | Lista de reportes de seguridad o problemas en el conjunto. | Alta |
| **RF-DA03** | Generar reportes rápidos | Administración | Permite descargar informes de pagos, visitas y otros datos clave. | Media |

#### **Requerimientos No Funcionales**  

| **Código**   | **Requerimiento** |
|-------------|------------------|
| **RNF-DA01** | Los datos deben actualizarse en tiempo real. |
| **RNF-DA02** | Los reportes deben poder exportarse en formatos PDF y Excel. |

#### **Criterios de Aceptación**  

- La administración debe poder acceder a un resumen de pagos en menos de 2 segundos.  
- Los incidentes deben ser visibles con prioridad según su gravedad.  
- Los reportes deben poder descargarse en formatos accesibles para impresión y análisis.  
