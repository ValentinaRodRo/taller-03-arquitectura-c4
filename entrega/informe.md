# Informe Técnico - Arquitectura Actual Compulens & Llanes SAS

## 1. Introducción
El objetivo de este documento es describir la arquitectura actual de **Compulens & Llanes SAS** mediante el modelo C4 en sus vistas **C1 (Contexto)** y **C2 (Contenedores)**.  
Esto permitirá entender cómo interactúan los actores con los sistemas actuales y cuáles son las debilidades que limitan la eficiencia del negocio.

---

## 2. Vista de Contexto (C1)
En esta vista se muestran los **actores principales**, el **sistema central** y los **sistemas externos** con los que interactúan.

- **Actores:**
  - Cliente final: solicita y consulta pedidos ópticos.
  - Jefe Administrativa: gestiona facturación y control administrativo.
  - Jefe de Producción: coordina órdenes en el laboratorio óptico.

- **Sistema central:**
  - ERP Ocular + procesos manuales (registros en Excel, papel y llamadas).

- **Sistemas externos:**
  - Plataforma bancaria (pagos electrónicos).
  - Correo/WhatsApp (canales de comunicación con clientes).

📌 En el diagrama C1 se observa cómo:
- El cliente entrega pedidos en físico o por llamada.
- La jefa administrativa gestiona facturación desde el ERP.
- El jefe de producción coordina las órdenes de laboratorio.
- El sistema central procesa pagos con la plataforma bancaria.
- Las confirmaciones se envían a clientes vía correo/WhatsApp.

---

## 3. Vista de Contenedores (C2)
En esta vista se desglosan los **contenedores internos** del sistema central y sus relaciones con actores y sistemas externos.

- **Contenedores internos:**
  - ERP Ocular: software especializado en facturación e inventario.
  - Registros manuales: pedidos gestionados en Excel, papel o llamadas.
  - Canal de comunicación externa: correo electrónico y WhatsApp.

- **Contenedor externo:**
  - Plataforma bancaria: pagos electrónicos.

📌 En el diagrama C2 se observa cómo:
- El cliente registra pedidos en los canales manuales.
- La jefa administrativa utiliza el ERP Ocular para la facturación.
- El jefe de producción coordina órdenes apoyándose en registros manuales.
- El ERP se conecta a la plataforma bancaria para pagos.
- El ERP envía confirmaciones mediante el canal de comunicación externa.

---

## 4. Debilidades actuales
- **Doble digitación:** pedidos en papel/Excel que luego deben pasarse al ERP.  
- **Falta de integración:** no hay conexión fluida entre pedidos, facturación y producción.  
- **Errores y demoras:** por dependencia de procesos manuales.  
- **Comunicación dispersa:** uso de correo/WhatsApp sin centralización.  

---

## 5. Conclusiones
La arquitectura actual de **Compulens & Llanes SAS** combina un ERP especializado con procesos manuales, lo que genera redundancias, riesgos de error y retrasos.  
La digitalización de los pedidos y su integración directa con el ERP Ocular representan la mayor oportunidad de mejora, junto con la centralización de la comunicación con clientes.

---
