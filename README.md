# ❄️ ClimAir S.L. - Proyecto Intermodular ASIR
![Status](https://img.shields.io/badge/Status-Desplegado-green)
![OS](https://img.shields.io/badge/OS-Ubuntu_24.04_LTS-orange)
![Cloud](https://img.shields.io/badge/Cloud-AWS-blue)

Este repositorio centraliza la infraestructura tecnológica completa de **ClimAir S.L.**, una PYME del sector de climatización. El proyecto demuestra la capacidad de integrar sistemas operativos, bases de datos, redes, hardware y soluciones en la nube en un entorno empresarial real y seguro.

---

## 🏗️ Estructura del Proyecto

### 🐧 [ISO] Implantación de Sistemas Operativos
Corazón del sistema basado en **Ubuntu Server 24.04 LTS**.
* **Almacenamiento:** Configuración de volúmenes elásticos mediante **LVM**.
* **Seguridad:** Hardening de SSH, configuración de **Samba** para interoperabilidad y gestión de permisos granulares.
* **Automatización:** Scripts en Bash para backups automáticos programados mediante Cron.

### 🗄️ [BBDD] Bases de Datos
Gestión de la persistencia de datos mediante **MySQL**.
* **Modelo Relacional:** Diseño normalizado (3FN) para la gestión de técnicos, clientes e intervenciones.
* **Seguridad DCL:** Implementación de roles (Administración/Técnicos) bajo el principio de mínimo privilegio.

### ☁️ [Cloud] Computación en la Nube
Estrategia de migración y despliegue en **Amazon Web Services (AWS)**.
* **Infraestructura:** Uso de instancias **EC2**, almacenamiento **EBS** y bases de datos gestionadas **RDS**.
* **Networking & Identity:** Aislamiento en **VPC** y control de accesos mediante **IAM**.
* **Viabilidad:** Análisis de costes (TCO) optimizado bajo el modelo *Free Tier*.

### 🖥️ [FUHAR] Fundamentos de Hardware
Especificaciones técnicas de los activos físicos de la empresa.
* **Servidores:** Selección de arquitectura x86_64 con redundancia **RAID** para asegurar la integridad física de los datos.
* **Continuidad:** Protección eléctrica mediante Sistemas de Alimentación Ininterrumpida (**SAI**).

### 🌐 [Redes] Planificación y Administración de Redes
Diseño de la conectividad local y remota.
* **Segmentación:** Organización de la red mediante **VLANs** y direccionamiento **IPv4/VLSM**.
* **Seguridad:** Topología en estrella con dispositivos gestionables y políticas de filtrado.

### 📋 [Lenguaje_Marcas] Lenguajes de Marcas
Modelado y visualización de la información operativa.
* **Intercambio de Datos:** Estructuras en **JSON y XML** validadas mediante DTD.
* **Dashboard:** Interfaz de monitorización técnica desarrollada en **HTML5/CSS3**.

---

## 📂 Organización del Repositorio
Siguiendo la estructura mostrada en la raíz del proyecto:

* `/BBDD`: Scripts SQL de creación, inserción y consultas.
* `/Cloud`: Documentación de arquitectura AWS y estimación de costes.
* `/FUHAR`: Especificaciones de hardware y redundancia física.
* `/ISO`: Configuraciones del servidor, scripts de backup y hardening.
* `/Lenguaje_Marcas`: Dashboard web, archivos JSON y validaciones XML.
* `/Redes`: Esquemas de red y direccionamiento IP.

---

## 🛡️ Estándares de Seguridad
Toda la infraestructura ha sido diseñada siguiendo las directrices de la **ISO/IEC 27001**, garantizando la Confidencialidad, Integridad y Disponibilidad de la información de ClimAir S.L.

---
**Desarrollado por:** Alejandro Sánchez Abellán  
**Curso:** 2025-2026 | Ciclo Formativo de Grado Superior ASIR
