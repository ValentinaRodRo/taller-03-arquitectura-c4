# 🛠️ Taller 3 - Arquitectura C4

Este repositorio contiene la modelación de la **arquitectura actual de sistemas** utilizando el **modelo C4**, con vistas **C1 (Contexto)** y **C2 (Contenedores)**.  
Se desarrolla en dos fases:

- **Parte 1 (Trabajo en clase):** Caso base RedExpress (plataforma logística).  
- **Parte 2 (Aplicación real):** Cliente Compulens & Llanes SAS (sector óptico y salud).  

---

## 📁 Estructura del repositorio

```
taller-03-arquitectura-c4/
├── README.md
├── clase/
│ ├── c1-contexto-borrador.drawio
│ ├── c2-contenedores-borrador.drawio
│ └── notas.md
└── entrega/
├── c1-contexto-final.drawio
├── c2-contenedores-final.drawio
├── informe.md
└── referencias.md
```



---


---

## 🎯 Objetivo
Representar la arquitectura actual de los sistemas para:
- Identificar actores, sistemas y relaciones externas (**C1**).
- Describir los principales contenedores internos y dependencias (**C2**).
- Analizar debilidades y oportunidades de mejora.

---

## 📊 Vistas del Modelo C4

### 🔹 Parte 1 – Caso RedExpress
- **C1 (Contexto):** Actores → Usuario final, Mensajero, Operador logístico.  
  Sistemas → App Cliente, Web Operadores, Sistema Central de Logística, API de notificaciones.  
- **C2 (Contenedores):**  
  - Contenedores internos: Gestión de Paquetes, Seguimiento GPS, Motor de Rutas, Sistema de Alertas, Base de Datos Distribuida, Balanceador de Carga.  
  - Sistemas externos: API de Notificaciones, Proveedor de Geolocalización.  

Archivos:  
- `clase/c1-contexto-borrador.drawio`  
- `clase/c2-contenedores-borrador.drawio`  

---

### 🔹 Parte 2 – Caso Compulens & Llanes SAS
- **C1 (Contexto):**  
  - Actores: Cliente final, Jefe Administrativa, Jefe de Producción.  
  - Sistema central: ERP Ocular + registros manuales.  
  - Sistemas externos: Plataforma Bancaria, Correo/WhatsApp (ahora conectados directamente con Cliente y Jefe Administrativa).  
- **C2 (Contenedores):**  
  - Internos: ERP Ocular, Registros Manuales.  
  - Externos: Plataforma Bancaria, Correo/WhatsApp.  
  - Relación clave: **Registros Manuales ↔ ERP Ocular** (doble digitación).  

Archivos:  
- `entrega/c1-contexto-final.drawio`  
- `entrega/c2-contenedores-final.drawio`  

---

## 📄 Documentación
- Informe técnico: [`entrega/informe.md`](./entrega/informe.md)  
- Referencias: [`entrega/referencias.md`](./entrega/referencias.md)  

---

## ✅ Conclusiones
- **RedExpress (Parte 1):** Arquitectura digitalizada, con integración de APIs externas, pero dependiente de servicios de terceros para notificaciones y mapas.  
- **Compulens & Llanes SAS (Parte 2):** Arquitectura fragmentada, con dependencia de procesos manuales y comunicación externa no centralizada.  
  - La **doble digitación** entre registros manuales y ERP Ocular representa el mayor problema.  
  - Se requiere digitalizar la toma de pedidos y centralizar la comunicación con clientes.  

---

## 📚 Referencias
- Brown, S. (2019). *C4 Model for Software Architecture*. https://c4model.com  
- The Open Group. (2022). *TOGAF® Standard – Core Concepts*  
- OMG. (2014). *Business Process Model and Notation (BPMN) Specification*  
