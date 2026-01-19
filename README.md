# Tesis: Sistema de Alambrado Virtual para Ganado Bovino (WIP)

Este repositorio documenta el diseño y arquitectura de mi Trabajo Final Integrador para la carrera de Ingeniería Electrónica (UNRN). El proyecto consiste en un sistema de geocerca activa que permite monitorear y contener ganado mediante estímulos conductuales.

## Arquitectura del Sistema
El sistema se basa en una arquitectura de nodos Maestro y Esclavo con integración en la nube:

- **Nodo Esclavo (Collar):** Basado en el SoC **LoRa Wireless Tracker**, integra GPS para geoposicionamiento y comunicación LoRa. Cuenta con un circuito generador de pulsos de alto voltaje para el estímulo correctivo.
- **Nodo Maestro (Gateway):** Gestiona la comunicación LoRaWAN y sirve de puente hacia la infraestructura de red.
- **Backend e Infraestructura:** Uso de un servidor en la nube (**Fly.io**) y base de datos (**Neon**) que actúan como el motor del sistema.
- **Interfaz de Usuario:** Aplicación desarrollada en **Qt** para escritorio y móvil que permite visualizar el estado de los animales y enviar comandos en tiempo real.

## Tecnologías y Desafíos Técnicos
- **Gestión de Energía:** Uso de **FreeRTOS** para la planificación de tareas y optimización del consumo en los collares.
- **Comunicación:** Implementación de protocolos robustos para áreas rurales con baja cobertura.
- **Diseño Electrónico:** Desarrollo de una ECU (Electronic Control Unit) capaz de generar estímulos correctivos controlados.

> Actualmente se encuentra en **Desarrollo**
