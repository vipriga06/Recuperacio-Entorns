# Git amb Entorn Gràfic

Git és una eina molt potent per al control de versions i, tot i que es fa servir principalment des de la línia de comandaments, hi ha eines gràfiques que fan que treballar amb Git sigui molt més accessible. En aquest document, veurem com gestionar alguns dels aspectes més importants de Git mitjançant una interfície gràfica: *commits*, *branches*, *merge*, *stash* i *historial*.

## 1. Commits

Un *commit* en Git és una instantània dels canvis realitzats al teu projecte. És el punt on els canvis es guarden al repositori.

### Com fer un commit en una interfície gràfica:
- **Pas 1**: Realitza els canvis als arxius del teu projecte.
- **Pas 2**: Obre la teva eina gràfica (per exemple, **GitKraken**, **SourceTree** o **Git GUI**).
- **Pas 3**: Veureu els canvis realitzats a la teva àrea de treball. Selecciona els arxius que vols incloure al commit.
- **Pas 4**: Escriu un missatge descriptiu del commit al camp corresponent.
- **Pas 5**: Fes clic al botó de "Commit" o "Commit Changes".

### Consells:
- Escriu sempre missatges de commit clars i descriptius.
- Intenta fer commits petits i freqüents per mantenir un historial net.

---

## 2. Branches (Rames)

Les branques en Git permeten treballar en diferents línies de desenvolupament de manera paral·lela. Això és útil per treballar en noves característiques, corregir errors o experimentar sense afectar la branca principal (*main* o *master*).

### Com crear una branca en una interfície gràfica:
- **Pas 1**: Obre la teva eina gràfica de Git.
- **Pas 2**: Cerca l'opció "Branch" o "Nova Branca".
- **Pas 3**: Introdueix un nom per la nova branca.
- **Pas 4**: Crea la branca i canvia automàticament a ella.

### Consells:
- Nomena les teves branques de manera clara, per exemple: `feature/nova-caracteristica` o `bugfix/correccio-error`.
- Utilitza branques per cada tasca o característica en què estiguis treballant.

---

## 3. Merge (Fusionar)

El *merge* és el procés de combinar els canvis de diferents branques en una sola. Es fa normalment quan vols integrar una branca de característiques de nou a la branca principal.

### Com fer un merge en una interfície gràfica:
- **Pas 1**: Canvia a la branca en la qual vols fer el merge (per exemple, `main`).
- **Pas 2**: Cerca l'opció "Merge" o "Fusionar" a la teva eina gràfica.
- **Pas 3**: Selecciona la branca que vols fusionar amb la branca actual.
- **Pas 4**: Git resoldrà els canvis i, si tot va bé, farà el merge automàticament. Si hi ha conflictes, hauràs de resoldre'ls manualment.



---

## 4. Stash (Emmagatzematge Temporal)

El *stash* en Git et permet guardar canvis temporals sense comprometre'ls, per poder treballar en una altra cosa i després tornar a aquests canvis més tard.

### Com utilitzar el stash en una interfície gràfica:
- **Pas 1**: Obre la teva eina gràfica de Git.
- **Pas 2**: Fes clic a l'opció "Stash" o "Emmagatzemar canvis".
- **Pas 3**: Git emmagatzemarà els canvis no compromesos en un lloc segur.
- **Pas 4**: Quan estiguis llest per continuar treballant en aquests canvis, simplement selecciona "Pop" o "Aplicar Stash" des de la interfície gràfica.


---

## 5. Historial de Commits

L'historial de commits et permet veure els canvis realitzats al teu projecte al llarg del temps. Pots accedir a l'historial per veure quan i què canvis es van fer.

### Com veure l'historial en una interfície gràfica:
- **Pas 1**: Obre la teva eina gràfica de Git.
- **Pas 2**: Cerca l'opció "Historial" o "Log".
- **Pas 3**: Podràs veure una llista dels commits realitzats, amb els seus missatges de commit i les diferències entre ells.
- **Pas 4**: Pots fer clic en qualsevol commit per veure més detalls, com els arxius modificats i les diferències.



---

## Conclusió

L'ús d'eines gràfiques per treballar amb Git pot fer que sigui molt més fàcil i accessible gestionar el teu repositori, especialment si ets nou a Git o prefereixes una interfície visual en lloc de la línia de comandaments. Tot i això, els comandaments de Git sempre estan disponibles per un control més precís i per a casos més avançats.

Al familiaritzar-te amb conceptes com commits, branques, merges, stashes i historial, tindràs les eines necessàries per gestionar els teus projectes de manera eficient i efectiva.

### Eines recomanades:

- **Github Desktop**: L'eina gràfica oficial de github.
- **GitKraken**: Una eina gràfica popular i fàcil d'usar.
- **SourceTree**: Una opció gratuïta d'Atlassian, també molt completa.

