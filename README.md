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
Infraestructura física y redundancia para la continuidad de negocio.
* **Equipamiento:** 2 Servidores críticos (CPM), 2 estaciones de desarrollo, 3 de administración y 10 para formación.
* **Redundancia RAID:** * **RAID 1 (Mirror):** En estaciones de desarrollo para proteger el código local.
* **RAID 6 (Doble Paridad):** En servidores CPM, permitiendo el fallo de hasta 2 discos sin pérdida de datos.
* **Despliegue:** Estandarización mediante imágenes maestras (**Sysprep**) y clonación masiva con **Clonezilla**

### 🌐 [Redes] Planificación y Administración de Redes
Diseño de red jerárquica segmentada para una estructura de dos plantas.
* **Topología:** Estrella extendida con enrutamiento **Router-on-a-Stick** (Gig0/0 y Gig0/1).
* **Segmentación (VLANs):** * **V10/V20:** Administración y Dirección (Planta Baja).
    * **V30/V40/V50:** Desarrollo, Soporte y Formación (1ª Planta).
    * **V60:** Servidores (CPD) | **V99:** Gestión y WiFi.
* **Seguridad:** Implementación de **ACLs** para restricción de tráfico inter-VLAN y acceso VTY restringido a la VLAN de Gestión.

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
