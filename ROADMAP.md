# 🗺️ Product Roadmap & Backlog — Banking Account Validator

> **Swarm Reviewers:** @arch | @impl | @bug | @dba-paranoico | @qa-destrutivo

---

## 🎯 Em Progresso (Sprint 1 — Core Domain & Quality)
- [ ] **@arch:** Desacoplamento do domínio aplicando **Clean Architecture** e isolando regras de negócio bancárias de frameworks externos.
- [ ] **@qa-destrutivo:** Elevação da cobertura de testes para > 95% com **Pitest** (Testes de Mutação) e JUnit 5.

## 📋 Backlog de Evolução Técnica
- [ ] **@impl:** Suporte a validação síncrona/assíncrona de contas usando **Spring WebFlux / R2DBC** para I/O não bloqueante.
- [ ] **@dba-paranoico:** Otimização de consultas de chave PIX / CPF com índices compostos no PostgreSQL e mitigação de lock de tabela.
- [ ] **@bug:** Implementação de chave de idempotência (`Idempotency-Key` header) no endpoint de validação.

---

## 🌶️ Grill-Me Profundo do Componente (@banking-account-validator)

### ❓ Perguntas de Refinamento Técnico:
1. **[Design de Código / @arch]:** Como o motor de regras garante que validações bancárias de diferentes instituições (Bradesco, Itaú, BACEN) sigam o princípio Open/Closed (SOLID) sem exigir um `if/else` gigante?
2. **[Idempotência / @bug]:** Se duas requisições idênticas com o mesmo lote de validação chegarem simultaneamente em réplicas diferentes da API, como a camada de persistência garante a idempotência sem causar Deadlock no banco?
3. **[Qualidade / @qa-destrutivo]:** Qual é o score de sobrevivência de mutantes aceitável no Pitest e como lidar com mutantes falsos-positivos na camada de DTOs?
