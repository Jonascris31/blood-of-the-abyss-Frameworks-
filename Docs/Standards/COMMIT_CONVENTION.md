# Convenção de Commits

## Formato principal

```text
ÁREA-NÚMERO: descrição objetiva
```

## Áreas

- `GAME`: integração geral de gameplay
- `WORLD`: níveis, salas e transições
- `COMBAT`: combate, dano e armas
- `PLAYER`: personagem e movimentação
- `AI`: inimigos e comportamento
- `UI`: HUD e menus
- `SAVE`: checkpoints e persistência
- `AUDIO`: música e efeitos
- `ART`: conteúdo visual
- `DOCS`: documentação
- `FIX`: correções
- `REFACTOR`: reorganização sem alterar comportamento

## Exemplos

```text
WORLD-003: cria blockout da sala de tutorial
COMBAT-002: adiciona janela de invulnerabilidade
SAVE-001: implementa estrutura inicial de checkpoint
FIX-004: corrige colisão nas plataformas móveis
DOCS-003: documenta arquitetura do sistema de combate
```

## Regras

- Um commit deve representar uma mudança coerente.
- Evitar commits com arquivos não relacionados.
- Não usar mensagens como `teste`, `ajustes`, `final` ou `funcionando`.
- Não fazer commit de arquivos gerados pela Unreal.
- Antes de integrar uma feature, confirmar que o projeto abre e compila.
