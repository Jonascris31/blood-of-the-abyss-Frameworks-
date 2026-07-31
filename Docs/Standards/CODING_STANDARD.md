# Padrão de Código

## Nomenclatura Unreal

- `A`: Actors — `ABloodCharacter`
- `U`: UObjects e Components — `UCombatComponent`
- `F`: Structs — `FDamageData`
- `E`: Enums — `ECombatState`
- `I`: Interfaces — `IDamageableInterface`

## Classes

Usar nomes que descrevam responsabilidade, não implementação genérica.

Bom:

```cpp
UHealthComponent
UCombatComponent
UBloodSaveSubsystem
```

Evitar:

```cpp
UManager
UHelper
UUtils
```

## Funções

Usar verbos explícitos:

```cpp
InitializeCombat();
ApplyDamage();
RestoreCheckpoint();
UpdateCombatState();
```

Funções booleanas devem expressar pergunta:

```cpp
CanAttack();
IsDead();
HasValidTarget();
```

## Variáveis

Evitar abreviações pouco claras. Preferir:

```cpp
CurrentHealth
MaximumHealth
AttackCooldown
```

## Boas práticas

- Métodos pequenos e com uma responsabilidade.
- Validar ponteiros antes do uso.
- Reduzir casts frequentes.
- Evitar lógica complexa no Tick.
- Expor ao Blueprint apenas o necessário.
- Documentar decisões não óbvias.
- Não armazenar segredos, tokens ou credenciais no repositório.

## Organização sugerida

```text
Source/BloodOfTheAbyss/
├── Characters/
├── Components/
├── Combat/
├── Interaction/
├── AI/
├── UI/
├── Save/
├── World/
└── Core/
```
