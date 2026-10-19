Plataforma de Virtualización con Proxmox VE

Informe técnico desarrollado para la materia Sistemas Operativos en la Universidad Privada Franz Tamayo (UNIFRANZ), sede Cochabamba.

Docente: Ing. Diego Patrick Cárdenas Sejas
Estudiante: Elia Solis Escobar
Fecha: Octubre 2026

Descripcion del proyecto

Este trabajo presenta el diseño de una plataforma de virtualización basada en Proxmox VE 9.2.2 sobre un servidor HP Z820 Workstation ubicado en el Laboratorio 302 de la universidad. La plataforma organiza los recursos en cuatro entornos diferenciados: Producción, Laboratorios, Desarrollo y Pruebas.

El informe abarca el diagnóstico del hardware y software existente, la distribución de recursos por entorno, una propuesta de expansión (RAM y almacenamiento ZFS), y las estrategias operativas recomendadas para administrar máquinas virtuales KVM y contenedores LXC.

Contenido del repositorio
Archivo	Descripcion
Informe_Tecnico_Proxmox_VE.pdf	Informe técnico completo
Diagrama_Arquitectura_Proxmox.png	Diagrama de la arquitectura de virtualización
README.md	Este archivo
Tecnologias y herramientas
Proxmox VE 9.2.2 (Hypervisor Tipo 1, bare-metal)
KVM (máquinas virtuales) y LXC (contenedores)
ZFS (almacenamiento con redundancia)
Resource Pools y RBAC (control de acceso)
VZDump (respaldos) y Snapshots
Arquitectura propuesta

La plataforma divide los recursos del servidor en cuatro entornos:

Produccion: servicios en uso real (KVM, 32 GB RAM, ZFS)
Laboratorios: contenedores LXC para docentes y estudiantes (48 GB RAM, ZFS)
Desarrollo: proyectos en construccion con clones enlazados (24 GB RAM, ZFS)
Pruebas: entorno efimero para experimentacion (16 GB RAM, thin-pool)
Licencia

Documento academico de uso educativo.
