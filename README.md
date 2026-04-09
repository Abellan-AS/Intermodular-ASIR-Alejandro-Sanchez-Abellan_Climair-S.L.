# ❄️ ClimAir S.L. - Sistema Integral de Gestión de Climatización

![Status](https://img.shields.io/badge/Status-Desplegado-green)
![OS](https://img.shields.io/badge/OS-Ubuntu_24.04_LTS-orange)
![Cloud](https://img.shields.io/badge/Cloud-AWS-blue)

Este repositorio contiene la arquitectura tecnológica completa de **ClimAir S.L.**, una PYME dedicada al sector de la climatización. El proyecto integra administración de sistemas, seguridad avanzada, gestión de datos relacionales y despliegue en la nube para ofrecer una solución operativa 24/7.

---

## 📌 Visión General
ClimAir S.L. nace de la necesidad de modernizar la operativa de una empresa de servicios técnicos. La infraestructura está diseñada para conectar de forma segura la oficina administrativa con los técnicos desplazados en campo, garantizando la **integridad de los datos** y la **continuidad del negocio**.

---

## 🏗️ Pilares del Proyecto

### 1. Infraestructura y Sistemas (Core)
El corazón del proyecto es un servidor **Ubuntu 24.04 LTS** diseñado para ser eficiente y escalable:
* **Almacenamiento Inteligente:** Implementación de **LVM** para gestionar el crecimiento de datos en caliente.
* **Interoperabilidad:** Servidor de archivos **Samba** para integración transparente con clientes Windows 11.
* **Automatización:** Sistema de copias de seguridad automáticas (Bash + Cron) con rotación y auditoría de logs.

### 2. Gestión de Datos y Persistencia
Centralización de la información mediante un modelo relacional robusto en **MySQL**:
* **Arquitectura de Datos:** Diseño normalizado (3FN) que gestiona técnicos, clientes, intervenciones y facturación.
* **Seguridad de Datos (DCL):** Control de acceso granular; los usuarios solo acceden a la información necesaria para su rol (Principio de Mínimo Privilegio).

### 3. Visualización y Flujo de Información
Modelado de datos para la monitorización en tiempo real:
* **Intercambio de Datos:** Uso de estándares **JSON y XML** para la comunicación entre dispositivos.
* **Dashboard Operativo:** Interfaz web de alto contraste (Cyberpunk Style) para el seguimiento visual del estado de los partes de trabajo.

### 4. Estrategia Cloud y Escalabilidad
Migración estratégica a la nube de **Amazon Web Services (AWS)**:
* **Alta Disponibilidad:** Despliegue mediante instancias **EC2** y bases de datos gestionadas **RDS**.
* **Red y Seguridad:** Aislamiento de recursos en una **VPC** privada y gestión de identidades mediante **IAM**.

---

## 🛡️ Seguridad y Hardening
La seguridad no es un módulo, es la base de todo el despliegue:
* **Blindaje SSH:** Acceso remoto endurecido y limitado.
* **Firewall Perimetral:** Configuración de **UFW** y **Security Groups** bajo política de denegación total por defecto.
* **Estándares:** Arquitectura alineada con los controles de la normativa **ISO/IEC 27001**.

---

## 📂 Estructura del Proyecto
```bash
.
├── /systems        # Configuraciones de SO, Scripts y Samba
├── /database       # Modelo E/R y Scripts SQL
├── /web-interface  # Dashboard y modelado de datos (JSON/XML)
├── /docs           # Documentación técnica y estrategia Cloud
└── README.md       # Guía global (este archivo)
