**Victor Prieto**  
**AMS1**  
**6/6/2025** 
# Diagrama de Classes en Java

## Relacions Detallades entre Classes

### 1. Associació
Relació més bàsica entre classes, indica que hi ha una connexió lògica.

```java
class Professor {
    private List<Curs> cursosImpartits;
}

class Curs {
    private Professor professor;
}
```

```
classDiagram
    Professor "1" --> "0..*" Curs : imparteix
```

### 2. Herència (Generalització)
Relació "és-un" entre classes.

```java
abstract class Vehicle {
    abstract void moure();
}

class Cotxe extends Vehicle {
    @Override
    void moure() { /* implementació */ }
}
```

```
classDiagram
    Vehicle <|-- Cotxe
    Vehicle <|-- Moto
```

### 3. Implementació
Classe que implementa una interfície.

```java
interface Auditable {
    void auditar();
}

class Factura implements Auditable {
    @Override
    public void auditar() { /* implementació */ }
}
```

```
classDiagram
    Auditable <|.. Factura
```

### 4. Agregació
Relació "té-un" on el fill pot existir sense el pare.

```java
class Departament {
    private List<Professor> professors;
}

class Professor {
    // Pot existir sense departament
}
```

```
classDiagram
    Departament "1" o-- "0..*" Professor : conté
```

### 5. Composició
Relació "té-un" més forta, el fill no pot existir sense el pare.

```java
class Edifici {
    private List<Aula> aules = new ArrayList<>();
    
    public Edifici() {
        aules.add(new Aula()); // Aula no existeix sense Edifici
    }
}

class Aula {
    // No té sentit sense Edifici
}
```

```
classDiagram
    Edifici "1" *-- "1..*" Aula : conté
```

## Classes Abstractes i Interfícies

### Classe Abstracta
```java
abstract class Figura {
    protected String color;
    
    abstract double area();
    
    public String getColor() {
        return color;
    }
}
```

### Interfície
```java
interface Renderitzable {
    void renderitzar();
    void canviarMida(double factor);
}
```

```
classDiagram
    class Figura {
        <<abstract>>
        #String color
        +getColor() String
        +area()* double
    }
    
    class Renderitzable {
        <<interface>>
        +renderitzar()* void
        +canviarMida(double factor)* void
    }
```

## Exemple Avançat: Sistema d'Universitats

```java
// Classe abstracta
abstract class Persona {
    protected String dni;
    protected String nom;
    
    public abstract void mostrarInformacio();
}

// Interfície
interface Matriculable {
    void matricular(Curs curs);
    void llistarMatricules();
}

// Classe concreta
class Estudiant extends Persona implements Matriculable {
    private List<Curs> cursosMatriculats = new ArrayList<>();
    
    @Override
    public void mostrarInformacio() {
        System.out.println("Estudiant: " + nom);
    }
    
    @Override
    public void matricular(Curs curs) {
        cursosMatriculats.add(curs);
    }
    
    @Override
    public void llistarMatricules() {
        cursosMatriculats.forEach(System.out::println);
    }
}

// Relació d'agregació
class Departament {
    private String nom;
    private List<Professor> professors;
    
    public void afegirProfessor(Professor p) {
        professors.add(p);
    }
}

// Relació de composició
class Universitat {
    private String nom;
    private List<Facultat> facultats = new ArrayList<>();
    
    public Universitat() {
        facultats.add(new Facultat("Informàtica"));
    }
}

class Facultat {
    private String nom;
    
    public Facultat(String nom) {
        this.nom = nom;
    }
}
```

```
classDiagram
    class Persona {
        <<abstract>>
        #String dni
        #String nom
        +mostrarInformacio()* void
    }
    
    class Matriculable {
        <<interface>>
        +matricular(Curs curs)* void
        +llistarMatricules()* void
    }
    
    class Estudiant {
        -List~Curs~ cursosMatriculats
        +mostrarInformacio() void
        +matricular(Curs curs) void
        +llistarMatricules() void
    }
    
    class Departament {
        -String nom
        -List~Professor~ professors
        +afegirProfessor(Professor p) void
    }
    
    class Universitat {
        -String nom
        -List~Facultat~ facultats
    }
    
    class Facultat {
        -String nom
    }
    
    Persona <|-- Estudiant
    Matriculable <|.. Estudiant
    Departament "1" o-- "0..*" Professor
    Universitat "1" *-- "1..*" Facultat
    Estudiant "0..*" -- "0..*" Curs : matricula
```



## Eines Addicionals

1. **StarUML**: Eina específica per a diagrames UML
2. **Lucidchart**: Altra opció online popular
3. **Eclipse Papyrus**: Plugin d'Eclipse per a modelat UML
4. **ArgoUML**: Eina UML de codi obert

