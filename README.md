# Erick Damian Gonzalez Aranda 👋
---
## Tech Lead | Cloud & Distributed Systems | AWS Architect | Ingeniero en Sistemas computacionales | Especialista desarrollo de software
---

Soy un Ingeniero de Software especializado en el diseño de arquitectura backend de alta disponibilidad, ingeniería de plataforma (Platform Engineering) y automatización de infraestructura en la nube. Mi enfoque profesional se centra en la creación de ecosistemas transaccionales resilientes, observabilidad distribuida avanzada, gobierno de seguridad perimetral y la construcción de "Golden Paths" que reducen la carga cognitiva de los equipos de desarrollo.

Inspirado por la disciplina y el pragmatismo de los marcos de pensamiento sistémicos, diseño software bajo la premisa de que **la viabilidad operativa de un sistema depende enteramente de su capacidad para ser observado, aislado y escalado de forma predecible.**

---

## 🛠️ El Ecosistema de Plataforma (Internal Developer Platform)

Los repositorios fijados en mi perfil no son utilerías aisladas; conforman el núcleo de una plataforma de desarrollo interna interconectada que resuelve problemas reales de producción, desde la frontera del tráfico hasta el almacenamiento de eventos:

~~~
[ Cliente HTTP ]
       │
       ▼
┌──────────────────────────────────────┐
│ 1. API-REST-Boilerplate              │ ◄── [ Arquitectura Hexagonal / DDD ]
│  El estándar de diseño transaccional │
└──────────┬───────────────────────────┘
           │
├───────────────────────────┐
▼ (Intercepción)            ▼ (Contexto Asíncrono)
┌──────────────────────────────────────┐ ┌──────────────────────────────────────┐
│ 2. GlobalHandler                     │ │ 3. Framework-Observabilidad          │
│    Escudo perimetral, sanitización   │ │    (logger-tracker)                  │
│    de errores y mitigación OWASP.    │ │    Inyección de Correlation IDs.     │
└──────────────────────────────────────┘ └──────────────────────────────────────┘
│
▼ (Mensajería Asíncrona)
┌──────────────────────────────────────┐
│ 4. MessagingCluster                  │ ◄── [ Cuenta Spoke Dedicada ]
│    Topología Híbrida Kafka (KRaft)   │      (Aislamiento de Blast Radius)
│    + RabbitMQ con persistencia real. │
└──────────────────────────────────────┘
~~~

### 📦 Componentes Core del Ecosistema:

*   **[API-REST-Boilerplate](https://github.com/DamianGonzalez27/API-REST-Boilerplate):** Estructura base para servicios distribuidos basada en Arquitectura Hexagonal y Domain-Driven Design (DDD). Desacopla de forma estricta las reglas de negocio de los protocolos de transporte y persistencia.
*   **[Framework-Observabilidad (logger-tracker)](https://github.com/DamianGonzalez27/logger-tracker):** Motor de telemetría inyectable diseñado para entornos asíncronos en Python. Gestiona el ciclo de vida de contextos dinámicos, inyectando de forma determinista *Correlation IDs* para garantizar la trazabilidad distribuida de punta a punta.
*   **[GlobalHandler](https://github.com/DamianGonzalez27/GlobalHandler):** Componente de resiliencia de frontera perimetral. Intercepta excepciones de la aplicación, mapea errores semánticos del dominio a contratos de transporte estandarizados y mitiga de forma nativa riesgos de fuga de información (*Information Leakage* - OWASP).
*   **[MessagingCluster](https://github.com/DamianGonzalez27/MessagingCluster):** Infraestructura como Código (IaC) para el aprovisionamiento de un clúster híbrido de mensajería (Apache Kafka en modo nativo KRaft y RabbitMQ). Diseñado bajo la estrategia de cuenta satélite (*Spoke*) para garantizar el aislamiento radical del radio de impacto (*blast radius*).

---

## 🚀 Core Competencies & Stack Tecnológico

*   **Arquitectura de Software:** Domain-Driven Design (DDD), Arquitectura Hexagonal (Puertos y Adaptadores), Patrones Transaccionales, Diseño Específico de APIs (REST, AsyncAPI).
*   **Ingeniería de Plataforma & IaC:** Docker, Docker Compose, diseño de topologías de red aisladas, aprovisionamiento de clústeres, observabilidad de infraestructura.
*   **Sistemas Distribuidos & Eventos:** Apache Kafka (KRaft Mode), RabbitMQ (AMQP), Event-Driven Architecture (EDA), Procesamiento Asíncrono.
*   **Observabilidad & Resiliencia:** Logs Estructurados, Rastreo Contextual Context-Aware, Monitoreo de MTTR, Políticas de Sanitización Perimetral de Errores.

---

## 📈 Filosofía de Ingeniería

> *"Un sistema complejo que funciona se encuentra invariablemente haber evolucionado de un sistema simple que funcionaba."* 
> Mis diseños priorizan la modularidad limpia, la tipificación estricta y la reducción de la deuda técnica mediante refactorizaciones continuas alineadas a estándares modernos de rendimiento y seguridad. No adopto tecnologías por tendencia, sino mediante la evaluación rigurosa de *trade-offs* arquitectónicos.

---

<p align="center">
  <a href="https://www.linkedin.com/in/damiangonzalezdev/">🌐 Conéctemos en LinkedIn</a> • 
  <a href="mailto:ing.gonzaleza@outlook.com">✉️ Contáctame por Email</a>
</p>
