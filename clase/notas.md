# Notas de Clase - Taller 3 (RedExpress)

## 📌 ¿Qué es el Modelo C4?
El **Modelo C4** es un enfoque para documentar y visualizar arquitecturas de software.  
Se basa en mostrar la arquitectura en **cuatro niveles de detalle**, de mayor a menor:

1. **C1 – Contexto:**  
   - Muestra el sistema en su entorno.  
   - Identifica **actores** (personas o sistemas externos) y cómo interactúan con el sistema central.  
   - Responde a: *¿Quién usa el sistema y con qué otros sistemas se relaciona?*  

2. **C2 – Contenedores:**  
   - Divide el sistema en sus **contenedores internos** (apps, bases de datos, APIs, microservicios).  
   - Explica cómo se distribuyen las responsabilidades de alto nivel.  
   - Responde a: *¿De qué partes está hecho el sistema y cómo interactúan entre sí?*  

3. **C3 – Componentes:**  
   - Detalla la estructura interna de un contenedor.  
   - Ejemplo: dentro del API REST, ver qué módulos o componentes lo conforman.  
   - Responde a: *¿Qué componentes forman cada contenedor?*  

4. **C4 – Código:**  
   - Nivel más bajo: muestra clases, métodos o estructuras de código.  
   - Rara vez se documenta en talleres de arquitectura, pero sirve para vincular diseño y código.  

---

## 🖼️ Vista C1 - Contexto (RedExpress)
- **Actores:**
  - Usuario Final: rastrea paquetes y consulta estado.
  - Mensajero: recibe rutas y reporta entregas.
  - Operador Logístico: gestiona rutas y operaciones.
- **Sistema central RedExpress:**
  - App Cliente (Android/iOS o Web).
  - Web para Operadores.
  - Sistema Central de Logística (backend y APIs).
- **Sistemas externos:**
  - API de Notificaciones.
- **Relaciones clave:**
  - Los actores interactúan con el sistema central, y este envía notificaciones a través de un servicio externo.

---

## 🖼️ Vista C2 - Contenedores (RedExpress)
- **Contenedores internos:**
  - Gestión de Paquetes: CRUD de envíos y clientes.
  - Seguimiento GPS: ubicación en tiempo real de mensajeros.
  - Motor de Rutas: cálculo y optimización de rutas de entrega.
  - Sistema de Alertas: generación de notificaciones.
  - Base de Datos Distribuida: pedidos, rutas, clientes y eventos.
  - Balanceador de Carga: distribuye tráfico entre aplicaciones y servicios.
- **Sistemas externos:**
  - API de Notificaciones: SMS, Push y Email.
  - Proveedor de Geolocalización: Google Maps API.
- **Relaciones clave:**
  - El sistema central depende de servicios externos para notificaciones y mapas, lo cual puede ser un riesgo.

---


## ✅ Resumen
- El modelo **C4** ayuda a comprender la arquitectura de manera gradual: desde la visión general (C1) hasta los detalles más técnicos (C4).  
- En la práctica, los diagramas **C1 y C2** son los más usados para explicar la arquitectura actual de un sistema.  
- Para RedExpress, se evidenció la importancia de identificar dependencias externas (notificaciones y geolocalización) como puntos críticos de comunicación.
