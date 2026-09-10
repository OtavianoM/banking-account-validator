# 💳 Banking Account Validator Engine

![Java](https://img.shields.io/badge/Java-17-007396?style=for-the-badge&logo=java)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3-6DB33F?style=for-the-badge&logo=springboot)
![Clean Architecture](https://img.shields.io/badge/Architecture-Clean_%26_DDD-blue?style=for-the-badge)
![Mutation Testing](https://img.shields.io/badge/Mutation_Test-Pitest-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

Motor de Validação e Auditoria Financeira de alta performance construído para ambientes bancários enterprise. Aplica os princípios de **Clean Architecture**, **DDD (Domain-Driven Design)** e suíte defensiva de testes com **JUnit 5**, **Mockito** e **Pitest** (Testes de Mutação).

---

## 📐 Arquitetura Hexagonal / Clean Architecture

```text
[ Controller / REST API ] ──> [ Use Cases / Application ] ──> [ Domain Entities ]
                                          │
                                          └──> [ Ports / Repositories ] ──> [ Database ]
```

---

## 🛡️ Destaques Técnicos & Qualidade
- **Isolamento de Domínio:** Regras de negócio puras sem acoplamento a frameworks.
- **Idempotência:** Validação com chave única de idempotência (`Idempotency-Key`).
- **Testes de Mutação:** Verificação de eficácia da suíte de testes unitários via **Pitest**.
- **Tratamento de Exceções:** Padronização RFC 7807 (*Problem Details for HTTP APIs*).

---

## 🚀 Como Executar

```bash
# Executar a suíte completa de testes unitários e de mutação
mvn clean test pitest:run
```

---

## 🗺️ Roadmap & Backlog
Consulte o [ROADMAP.md](./ROADMAP.md) para o backlog de tarefas e o **Swarm Grill-Me Profundo**.
