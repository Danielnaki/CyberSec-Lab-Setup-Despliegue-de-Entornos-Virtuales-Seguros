📋 Introducción Técnica
Este repositorio documenta el proceso de despliegue y configuración optimizada de Oracle VM VirtualBox 7.x para la creación de laboratorios de ciberseguridad. En la fase inicial de la formación como analista de seguridad (Siguiendo el roadmap de ISC2 CC y Cisco), el dominio de la virtualización es crítico, ya que permite la segregación de entornos, el análisis de malware y las pruebas de red de forma segura y controlada.

<img width="963" height="941" alt="image" src="https://github.com/user-attachments/assets/548f6463-0a20-4b14-920d-68b0146a4bb9" />

Imagen de referencia de la interfaz principal de VirtualBox.

🎯 Objetivos de la Guía
Establecer un entorno aislado (sandboxing) para pruebas técnicas sin riesgo para el sistema anfitrión (Host).

Optimizar el rendimiento de las máquinas virtuales (VMs) aprovechando la arquitectura de hardware moderna (AMD Ryzen).

Configurar redes virtuales seguras para simular escenarios de ataque y defensa.

Documentar las mejores prácticas de administración de VMs (Snapshots, Hardening).

💻 Contexto de Hardware: Optimización para AMD Ryzen 7
Esta guía pone especial énfasis en la configuración de la Capa de Abstracción de Hardware (HAL) para procesadores con múltiples núcleos y hilos, como el AMD Ryzen 7 5800H/6800H (procesador de referencia en este laboratorio).

Requerimiento Crítico: Para que la virtualización sea funcional y performante, es imperativo habilitar el SVM Mode (Secure Virtual Machine) en la BIOS/UEFI del equipo.

<img width="1600" height="721" alt="Bios_Pc" src="https://github.com/user-attachments/assets/ff57db52-a1f3-4fea-a481-461b90dec933" />
 
Captura de referencia de la BIOS mostrando SVM Mode habilitado (Enable).

Validación en el Sistema Anfitrión (Windows):

<img width="961" height="737" alt="Captura de pantalla 2026-05-08 094255" src="https://github.com/user-attachments/assets/49ee7c94-e767-480f-83e5-a3833b870689" />

Captura del Administrador de Tareas (Rendimiento > CPU) mostrando 'Virtualización: Habilitado'.

🛠️ Justificación Técnica de la Herramienta (Oracle VM VirtualBox)
Se ha seleccionado VirtualBox como hipervisor tipo 2 principal para este repositorio por las siguientes razones técnicas:

Cero Fricción de Despliegue: A diferencia de otras soluciones propietarias, la versión Open Source de VirtualBox no requiere registro ni autenticación para su descarga e instalación, lo que facilita su despliegue inmediato.

Modularidad (Extension Pack): Permite extender las capacidades del hipervisor (soporte USB 3.0, cifrado de disco) mediante paquetes modulares.

Gestión Versátil de Redes: Ofrece una granularidad avanzada para configurar interfaces de red (NAT, Puente, Red Interna, Host-Only), esencial para simular topologías de red empresariales.
