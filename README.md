# 🎬 Microservices Spring Boot

<p align="center">
  <b>Architecture Microservices avec Spring Boot & Spring Cloud</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-21+-orange?style=for-the-badge&logo=openjdk" />
  <img src="https://img.shields.io/badge/Spring%20Boot-4.x-brightgreen?style=for-the-badge&logo=springboot" />
  <img src="https://img.shields.io/badge/Spring%20Cloud-Microservices-blue?style=for-the-badge&logo=spring" />
  <img src="https://img.shields.io/badge/Gradle-Build-02303A?style=for-the-badge&logo=gradle" />
</p>

---

## 📌 Description

**Microservices-Spring-Boot** est un projet basé sur une architecture **microservices** avec **Java, Spring Boot et Spring Cloud**.

L'objectif du projet est de mettre en pratique les principales technologies utilisées dans une architecture distribuée moderne :

- 🔎 Service Discovery avec Eureka
- 🌐 API Gateway
- ⚙️ Configuration centralisée avec Spring Cloud Config
- 🎬 Services métier indépendants
- 📡 Communication entre microservices
- 🔍 Distributed Tracing avec Zipkin
- 🧩 Architecture découplée et scalable

---

## 🏗️ Architecture

```text
                         ┌─────────────────┐
                         │    Web Client   │
                         │   webapp.html   │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │   API Gateway   │
                         │  Spring Cloud   │
                         └────────┬────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
                    ▼                           ▼
          ┌───────────────────┐       ┌────────────────────┐
          │ Movie Catalog     │       │ Movie Streaming    │
          │ Service           │       │ Service            │
          └─────────┬─────────┘       └──────────┬─────────┘
                    │                            │
                    └────────────┬───────────────┘
                                 │
                                 ▼
                       ┌──────────────────┐
                       │ Eureka Server    │
                       │ Service Registry  │
                       └──────────────────┘

                       ┌──────────────────┐
                       │  Config Server   │
                       │ Centralized Conf │
                       └──────────────────┘

                       ┌──────────────────┐
                       │      Zipkin      │
                       │ Distributed      │
                       │     Tracing      │
                       └──────────────────┘
