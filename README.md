# 🛠️ Taller 3 - Arquitectura C4 (Compulens & Llanes SAS)

Este repositorio contiene la modelación de la **arquitectura actual del sistema del cliente Compulens & Llanes SAS**, realizado con el modelo **C4** en sus vistas **C1 (Contexto)** y **C2 (Contenedores)**.

---

## 📁 Estructura del repositorio

```
taller-03-arquitectura-c4/
├── README.md
└── entrega/
├── c1-contexto-final.drawio
├── c2-contenedores-final.drawio
├── informe.md
└── referencias.md
```



---

## 🎯 Objetivo
Representar la arquitectura actual de **Compulens & Llanes SAS** para:
- Identificar actores, sistemas y relaciones externas (**C1**).
- Describir los principales contenedores internos del sistema (**C2**).
- Analizar debilidades y oportunidades de mejora.

---

## 📊 Vistas del Modelo C4

### 🔹 C1 - Vista de Contexto
Muestra a los actores principales (Cliente final, Jefe Administrativa, Jefe de Producción), el sistema central (ERP Ocular + procesos manuales) y los sistemas externos (Plataforma Bancaria, Correo/WhatsApp).

Archivo: `entrega/c1-contexto-final.drawio`

---

### 🔹 C2 - Vista de Contenedores
Desglosa el sistema central en sus contenedores internos:
- **ERP Ocular** (facturación e inventario).
- **Registros manuales** (Excel, papel, llamadas).
- **Comunicación externa** (Correo/WhatsApp).

Archivo: `entrega/c2-contenedores-final.drawio`

---

## 📄 Documentación
- Informe técnico: [`entrega/informe.md`](./entrega/informe.md)  
- Referencias: [`entrega/referencias.md`](./entrega/referencias.md)  

---

## ✅ Conclusión
La arquitectura actual de **Compulens & Llanes SAS** combina un ERP especializado con procesos manuales y comunicación dispersa.  
La **digitalización de pedidos** y su **integración con el ERP Ocular** son la mayor oportunidad de mejora para reducir errores, eliminar la doble digitación y mejorar la experiencia del cliente.

---

## 📚 Referencias
- Brown, S. (2019). *C4 Model for Software Architecture*. https://c4model.com  
- The Open Group. (2022). *TOGAF® Standard – Core Concepts*  
- OMG. (2014). *Business Process Model and Notation (BPMN) Specification*  
