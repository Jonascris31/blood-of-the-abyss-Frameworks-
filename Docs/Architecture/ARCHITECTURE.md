# Arquitetura do Projeto

## Objetivo

Manter os sistemas de gameplay desacoplados, testáveis e reutilizáveis, evitando dependências diretas desnecessárias entre personagem, combate, interface e mundo.

## Princípios

1. **Responsabilidade única:** cada classe deve possuir um propósito claro.
2. **Composição sobre herança:** comportamentos reutilizáveis devem preferencialmente viver em componentes.
3. **Baixo acoplamento:** sistemas se comunicam por interfaces, eventos e contratos explícitos.
4. **Dados separados de comportamento:** configurações devem utilizar Data Assets ou estruturas de dados quando apropriado.
5. **Blueprints como camada de composição:** regras centrais ficam em C++; Blueprints organizam conteúdo e iteração visual.

## Camadas sugeridas

```text
Input
  ↓
Character / Controller
  ↓
Gameplay Components
  ↓
Domain Systems
  ↓
World, UI and Persistence
```

## Sistemas planejados

- Character Framework
- Movement System
- Combat System
- Health and Damage
- Interaction System
- Checkpoint and Save
- Inventory
- Enemy AI
- UI and HUD
- Level Transition
- Narrative Events

## Comunicação entre sistemas

Preferir:

- Delegates e eventos
- Interfaces da Unreal
- Componentes reutilizáveis
- Subsystems para serviços globais

Evitar:

- Casts encadeados
- Referências globais desnecessárias
- Regras de gameplay dentro do Level Blueprint
- Dependências circulares

## Estrutura de classes sugerida

```text
ABloodCharacter
├── UBloodMovementComponent
├── UHealthComponent
├── UCombatComponent
├── UInteractionComponent
└── UInventoryComponent

ABloodPlayerController
UBloodGameInstance
UBloodSaveSubsystem
ABloodCheckpoint
```

## Regra de decisão

Antes de criar uma nova classe, responder:

1. Qual responsabilidade ela possui?
2. Quem depende dela?
3. Ela precisa ser um Actor, Component, Object ou Subsystem?
4. Seus dados devem ficar em código, Blueprint ou Data Asset?
5. Como ela será testada e demonstrada?
