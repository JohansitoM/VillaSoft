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

### **Fuera del Alcance:**  
- Funcionalidades de mantenimiento de infraestructura.  
- Integración con hardware de acceso biométrico o tarjetas de acceso.  
- Módulo avanzado de contabilidad o facturación.  

---

## **3. Módulos del Sistema**

### **3.1 Módulo de Gestión de Propietarios e Inquilinos**  

**Descripción**: Este módulo permite gestionar los propietarios e inquilinos del conjunto residencial.  

#### **Requerimientos Funcionales**  

- **RF-GPI01**: El sistema debe permitir a la administración registrar a los propietarios con datos como nombre, cédula, teléfono y email.  
- **RF-GPI02**: El sistema debe permitir a los propietarios registrar y administrar sus inquilinos.  
- **RF-GPI03**: Los propietarios e inquilinos deben poder actualizar sus datos personales, excepto la cédula y el apartamento.  
- **RF-GPI04**: La administración debe poder modificar o eliminar registros de propietarios e inquilinos.  
- **RF-GPI05**: El sistema debe permitir buscar propietarios o inquilinos por nombre, cédula o apartamento.  

#### **Requerimientos No Funcionales**  

- **RNF-GPI01**: La información de los propietarios e inquilinos debe ser protegida mediante autenticación segura.  
- **RNF-GPI02**: Solo los administradores pueden modificar datos de propietarios.  
- **RNF-GPI03**: La búsqueda debe estar disponible para todos los usuarios autenticados.  

#### **Criterios de Aceptación**  

- Los propietarios solo pueden registrar inquilinos en apartamentos donde sean titulares.  
- Los datos de cédula y apartamento no deben poder modificarse una vez registrados.  
- La búsqueda de propietarios e inquilinos debe ser rápida y eficiente, con un tiempo de respuesta inferior a 2 segundos.  

---

### **3.2 Módulo de Control de Acceso y Seguridad**  

**Descripción**: Este módulo permite gestionar el control de acceso y seguridad del conjunto residencial.  

#### **Requerimientos Funcionales**  

- **RF-CAS01**: Los vigilantes deben poder registrar la entrada y salida de visitantes con nombre, cédula, apartamento a visitar y hora de ingreso.  
- **RF-CAS02**: Los propietarios e inquilinos deben poder pre-registrar visitantes para agilizar su acceso.  
- **RF-CAS03**: El sistema debe permitir consultar el historial de visitas por apartamento o visitante.  
- **RF-CAS04**: Los vigilantes deben poder reportar incidentes de seguridad en el sistema.  

#### **Requerimientos No Funcionales**  

- **RNF-CAS01**: La información de acceso debe almacenarse en tiempo real.  
- **RNF-CAS02**: Solo vigilantes y administradores pueden registrar y ver el historial de visitantes.  

#### **Criterios de Aceptación**  

- Los registros de entrada y salida deben quedar almacenados con sello de tiempo.  
- Solo se deben permitir accesos a visitantes previamente autorizados o registrados.  
- Los reportes de incidentes deben poder visualizarse en un panel administrativo.  

---

### **3.3 Módulo de Pagos y Finanzas**  

**Descripción**: Este módulo permite gestionar los pagos y finanzas del conjunto residencial.  

#### **Requerimientos Funcionales**  

- **RF-PF01**: La administración debe poder registrar y actualizar el pago de cuotas de administración por apartamento.  
- **RF-PF02**: Los propietarios deben poder consultar el estado de cuenta de su apartamento.  
- **RF-PF03**: El sistema debe enviar notificaciones a los propietarios con pagos pendientes.  
- **RF-PF04**: El sistema debe generar reportes de pagos y deudas por apartamento.  
- **RF-PF05**: Los propietarios deben poder pagar sus cuotas de administración en línea por medio de PSE o tarjeta de débito o crédito.  

#### **Requerimientos No Funcionales**  

- **RNF-PF01**: El sistema debe permitir exportar reportes en formatos PDF y Excel.  
- **RNF-PF02**: La información financiera debe estar protegida mediante encriptación.  

#### **Criterios de Aceptación**  

- Los pagos deben reflejarse en el estado de cuenta en un tiempo máximo de 5 minutos.  
- Los reportes de pagos y deudas deben poder descargarse en formatos PDF y Excel.  
- Solo los propietarios pueden acceder a la información de pagos de su apartamento.  

---

### **3.4 Módulo de Comunicación y Notificaciones**  

**Descripción**: Este módulo permite gestionar las comunicaciones y notificaciones del conjunto residencial.  

#### **Requerimientos Funcionales**  

- **RF-CN01**: La administración debe poder enviar notificaciones a propietarios e inquilinos sobre eventos, mantenimientos o avisos importantes.  
- **RF-CN02**: Los propietarios e inquilinos deben poder enviar quejas o solicitudes a la administración.  
- **RF-CN03**: El sistema debe permitir visualizar un historial de comunicaciones.  

#### **Requerimientos No Funcionales**  

- **RNF-CN01**: Las notificaciones deben enviarse por correo electrónico y/o en la plataforma.  

#### **Criterios de Aceptación**  

- Los mensajes deben enviarse a todos los destinatarios en un tiempo máximo de 1 minuto.  
- El historial de comunicaciones debe estar disponible por un período mínimo de 12 meses.  

---

### **3.5 Módulo de Administración del Conjunto**  

**Descripción**: Este módulo permite gestionar la administración del conjunto residencial.  

#### **Requerimientos Funcionales**  

- **RF-AC01**: La administración debe poder registrar, modificar y eliminar apartamentos.  
- **RF-AC02**: La administración debe poder asignar propietarios a cada apartamento.  
- **RF-AC03**: El sistema debe permitir la gestión de usuarios y permisos.  

#### **Requerimientos No Funcionales**  

- **RNF-AC01**: Solo la administración puede acceder a la gestión de apartamentos y usuarios.  

#### **Criterios de Aceptación**  

- Solo los administradores pueden modificar o eliminar apartamentos.  
- Cada apartamento debe tener un único propietario registrado en el sistema.  
- Los cambios en la asignación de propietarios deben quedar registrados con un historial de modificaciones.  

---

Este documento establece las bases para el desarrollo del sistema. **¿Necesitas algún ajuste o agregar más detalles?** 🚀  

<!-- ### 2.6 Módulo de Reservas de Áreas comunes (Versión 2)

**Descripción**: Este módulo permite gestionar las reservas de áreas comunes como el salón para eventos, la cancha de futbol, la piscina, gimnasio del conjunto residencial

**Requerimientos Funcionales**:
- RF-RAC01: Los propietarios e inquilinos deben poder reservar áreas comunes para eventos o actividades.
- RF-RAC02: El sistema debe permitir consultar el historial de reservas de áreas comunes.
- RF-RAC03: El sistema debe permitir cancelar reservas de áreas comunes.
- RF-RAC04: El sistema debe permitir consultar la disponibilidad de cada área
- RF-RAC05: El sistema debe permitir a la administración asignar un costo por hora para cada área -->


