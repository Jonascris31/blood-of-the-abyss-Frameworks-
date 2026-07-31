# Registro de Decisões Técnicas

Este arquivo registra decisões importantes para evitar que escolhas arquiteturais sejam esquecidas ou revertidas sem contexto.

## ADR-001 — Gameplay principal em C++

**Status:** Aceita

**Contexto:** O projeto precisa demonstrar competências técnicas e manter regras centrais reutilizáveis.

**Decisão:** Sistemas principais de gameplay serão implementados em C++, enquanto Blueprints serão usados para composição, conteúdo e ajustes visuais.

**Consequências:**

- Melhor organização e reutilização.
- Maior valor técnico para portfólio.
- Exige disciplina na exposição de propriedades e eventos ao Blueprint.

## ADR-002 — Salas modulares para o Jardim

**Status:** Aceita

**Contexto:** Construir todo o mapa de uma vez aumenta retrabalho e dificulta validação.

**Decisão:** O Jardim do Esquecimento será desenvolvido como conjunto de salas modulares e testáveis.

**Consequências:**

- Facilita blockout e testes.
- Permite reorganizar o fluxo.
- Exige métricas consistentes de escala, salto e câmera.
