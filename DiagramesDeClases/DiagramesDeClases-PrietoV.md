**Victor Prieto**  
**AMS1**  
**6/6/2025** 

# Diagrama de Classes en Java

El diagrama de classes és una eina fonamental en el disseny orientat a objectes que ens permet visualitzar l'estructura d'un sistema software.

## Què és un Diagrama de Classes? 

Representació visual de:
- Les classes que componen el sistema
- Els seus atributs i mètodes
- Les relacions entre elles

**Exemple bàsic:**
```
classDiagram
    class Persona {
        -String nom
        -int edat
        +caminar()
        +parlar()
    }
```

## Elements Principals 

### 1. Classes
Caixa dividida en 3 parts:
1. **Nom** (en negreta)
2. **Atributs** (visibilitat nom: tipus)
3. **Mètodes** (visibilitat nom(paràmetres): tipusRetorn)

```
classDiagram
    class CompteBancari {
        -String numeroCompte
        -double saldo
        +dipositar(double quantitat) void
        +retirar(double quantitat) boolean
    }
```

### 2. Modificadors d'Accés
- `+` Públic
- `-` Privat
- `#` Protegit
- `~` Paquet (default)

### 3. Relacions entre Classes

| Tipus | Símbol | Descripció |
|-------|--------|------------|
| Associació | ─────> | Relació bàsica entre classes |
| Herència | ───▷ | Estén d'una altra classe |
| Implementació | ╌╌▷ | Implementa una interfície |
| Agregació | ◇────> | Relació "té-un" (part independent) |
| Composició | ◆────> | Relació "té-un" (part dependent) |

## Exemple Complet 

```
classDiagram
    class Client {
        -String dni
        -String nom
        +realitzarOperacio() void
    }

    class Compte {
        <<abstract>>
        #String numero
        #double saldo
        +dipositar(double quantitat)* void
        +retirar(double quantitat)* boolean
    }

    class CompteCorrent {
        -double descobert
        +retirar(double quantitat) boolean
    }

    class CompteEstalvi {
        -double interes
        +calcularInteres() void
    }

    class Banc {
        -String nom
        +afegirCompte() void
    }

    Client "1" *-- "0..*" Compte: Possueix
    Compte <|-- CompteCorrent
    Compte <|-- CompteEstalvi
    Banc "1" o-- "0..*" Compte: Administra
```


## Eines per Crear-los 

1. **PlantUML**: Llenguatge textual per generar diagrames
2. **Visual Paradigm**: Eina professional
3. **draw.io**: Gratuït i online
4. **IntelliJ IDEA**: Té generador integrat
