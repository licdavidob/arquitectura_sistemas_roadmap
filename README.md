# 🗺️ Arquitectura de Sistemas Roadmap

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Backend](https://img.shields.io/badge/Backend-Go%20%7C%20PHP%20%7C%20Laravel-007ACC?style=flat)]()
[![Infrastructure](https://img.shields.io/badge/Infrastructure-Docker%20%7C%20Kubernetes%20%7C%20GCP-326CE5?style=flat)]()

Este repositorio contiene mi ruta de aprendizaje, bitácora de estudio y evolución de proyectos prácticos orientados a dar el salto de **Desarrollador Backend** a **Arquitecto de Software y Sistemas Distribuidos**. 

El objetivo principal es consolidar los fundamentos teóricos de la arquitectura moderna mediante la implementación de un ecosistema de software evolutivo, escalable, resiliente y nativo de la nube.

---

## 🎯 Propósito del Repositorio

A diferencia de un aprendizaje puramente teórico, este repositorio funge como un **laboratorio práctico**. A lo largo de la ruta, se desarrollará un sistema que evolucionará modularmente: comenzando como un monolito bien estructurado con diseño guiado por el dominio, transformándose en una arquitectura de microservicios e implementando patrones avanzados de comunicación asíncrona, observabilidad y despliegue en entornos de orquestación.

### 🏗️ Arquitectura Objetivo del Proyecto
El destino final de los componentes desarrollados en este roadmap sigue el siguiente flujo distribuido:

🗺️ Ruta de Aprendizaje e Hitos de Estudio
Sigue mi progreso a través de los diferentes módulos del roadmap:

📦 Módulo 1: Diseño de Software y Arquitectura de Aplicaciones
Enfoque: Estructurar el código de un solo componente para que sea mantenible, desacoplado y testeable.

[ ] 1.1 Principios de Diseño Avanzados: Profundización en SOLID (especialmente DIP y LSP) y métricas de acoplamiento.

[ ] 1.2 Arquitecturas Limpias: Implementación de Arquitectura Hexagonal (Ports and Adapters) y Clean Architecture.

[ ] 1.3 Domain-Driven Design (DDD):

Estratégico: Bounded Contexts y Ubiquitous Language.

Táctico: Entities, Value Objects, Aggregates, Repositories y Domain Services.

[ ] 1.4 Patrones Locales: Aplicación de CQRS (Command Query Responsibility Segregation) a nivel de código.

🚀 Entregable Práctico: ../src/modulo-1-api-clean (API base aislando completamente las reglas de negocio del framework y la base de datos).

🗄️ Módulo 2: Arquitectura de Datos y Almacenamiento
Enfoque: Comprender el comportamiento, consistencia y escalabilidad de los datos en sistemas de alta disponibilidad.

[ ] 2.1 Teoría de Sistemas Distribuidos: Teorema CAP, Teorema PACELC y modelos de consistencia (Fuerte vs. Eventual).

[ ] 2.2 Escalabilidad en BD: Optimización de índices, estrategias de replicación (Read Replicas) y conceptos de Sharding.

[ ] 2.3 Capas de Caché: Patrones Cache-Aside, Write-Through, políticas de evicción (LRU/LFU) y mitigación de Cache Stampede.

🚀 Entregable Práctico: ../src/modulo-2-data-cache (Integración de Redis con estrategias de caché óptimas para consultas masivas).

🔌 Módulo 3: Sistemas Distribuidos y Comunicación
Enfoque: Romper el monolito. Diseñar interconexiones eficientes, tolerantes a fallas y seguras.

[ ] 3.1 Descomposición: Estrategias para dividir sistemas basados en capacidades de negocio o subdominios de DDD.

[ ] 3.2 Comunicación Síncrona: Implementación de contratos con gRPC y Protocol Buffers para comunicación de alta velocidad.

[ ] 3.3 Event-Driven Architecture (EDA):

Queues (RabbitMQ) vs. Event Streams (Kafka).

Patrones de mensajería, garantías de entrega (At-least-once) y el patrón Transactional Outbox.

🚀 Entregable Práctico: ../src/modulo-3-distribuidos (Separación en microservicios comunicados por gRPC y publicación de eventos asíncronos vía Message Broker).

☸️ Módulo 4: Infraestructura, Orquestación y Nube
Enfoque: Llevar la arquitectura del software hacia operaciones modernas y automatizadas en la nube.

[ ] 4.1 Contenedores Avanzados: Optimización de imágenes Docker mediante Multi-stage builds y seguridad en capas.

[ ] 4.2 Orquestación con Kubernetes (K8s): Control Plane, Pods, Deployments, Services, ConfigMaps y manejo de tráfico con Ingress.

[ ] 4.3 Cloud Native Architecture: Conceptos de VPC, subredes, API Gateways, autoescalado (HPA) y nociones de Infraestructura como Código (IaC) con Terraform.

🚀 Entregable Práctico: ../k8s/manifests (Definición de manifiestos para desplegar y orquestar todo el ecosistema localmente en Minikube o entornos Cloud).

🛡️ Módulo 5: Resiliencia, Seguridad y Observabilidad
Enfoque: Diseñar asumiendo que todo va a fallar. Crear sistemas auto-recuperables y 100% medibles.

[ ] 5.1 Patrones de Tolerancia a Fallos: Circuit Breaker, Rate Limiting, Bulkhead y reintentos con Exponential Backoff.

[ ] 5.2 Observabilidad: Los tres pilares (Métricas con Prometheus/Grafana, Logs estructurados y Trazabilidad Distribuida con OpenTelemetry/Jaeger).

[ ] 5.3 Seguridad Arquitectónica: Autenticación descentralizada con JWT/OAuth2 y gestión centralizada de secretos.

🚀 Entregable Práctico: ../src/modulo-5-observabilidad (Inyección de telemetría distribuida para rastrear peticiones end-to-end a través de los servicios).

📚 Recursos de Referencia Principales
Para el desarrollo de este roadmap me apoyo firmemente en la siguiente literatura técnica:

Designing Data-Intensive Applications — Martin Kleppmann.

Clean Architecture — Robert C. Martin.

Building Microservices — Sam Newman.

Documentación oficial de Kubernetes, Go, Laravel y tecnologías del ecosistema Cloud Native.
