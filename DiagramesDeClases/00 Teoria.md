# Debug (depurar)

**Debug** és el procés de trobar i corregir errors del codi. D'aquest procés en diem **depuració**.

Per debugar un programa:

- Identifiquem un error
- Posem **breakpoints**, punts de control on volem veure l'estat del programa
- Inspeccionem el valor de les variables
- Executem el programa pas a pas
- Corregim l'error

## Extensió "Python Debugger"

L'extensió **"Python Debugger"** ens permet debugar el codi python (id: ms-python.debugpy).

<center>
<img src="./assets/dbg0300.png" style="width: 90%; max-width: 250px">
</center>

Mireu que l'extensió estigui instal·lada:

<center>
<img src="./assets/dbg0301.png" style="width: 90%; max-width: 350px">
</center>

## Afegir breakpoints

En arxius de codi python, es poden afegir **breakpoints** fent click al costat de la linia on volem aturar l'execució.

En aquest exemple, el codi s'aturarà a les linies 5 i 7 per poder inspeccionar l'estat del programa.

<center>
<img src="./assets/dbg0302.png" style="width: 90%; max-width: 350px">
</center>

Els **breakpoints** apareixen com a punts vermells, al costat de les linies on s'aturarà l'execució.

## Executar en mode debug.

Es pot executar un arxiu **".py"** en mode debug a través del botó **"Python Debugger"** de les opcions d'execució:

<center>
<img src="./assets/dbg0303.png" style="width: 90%; max-width: 350px">
</center>

Aleshores comença l'execució en mode **debug**:

- Apareixen les opcions de **debug** al **Visual Studio Code**
- El codi s'aturarà al primer **breakpoint**

Les opcions de debug són:

<table>
    <tr>
        <td><img src="./assets/dbgIconContinue.png"></td>
        <td><b>Continue</b></td>
        <td>L'acció continua fins al següent breakpoint o final del programa</td>
    </tr>
    <tr>
        <td><img src="./assets/dbgIconOver.png"></td>
        <td><b>Step over</b></td>
        <td>Salta a la linia següent, permet debugar linia a linia</td>
    </tr>
    <tr>
        <td><img src="./assets/dbgIconInto.png"></td>
        <td><b>Step into</b></td>
        <td>Si la línia actual conté la crida a una funció, entra dins la funció</td>
    </tr>
    <tr>
        <td><img src="./assets/dbgIconOut.png"></td>
        <td><b>Step out</b></td>
        <td>Si la línia està dins d'una funció, surt de la funció</td>
    </tr>
    <tr>
        <td><img src="./assets/dbgIconRestart.png"></td>
        <td><b>Restart</b></td>
        <td>Reinicia l'execució del programa</td>
    </tr>
    <tr>
        <td><img src="./assets/dbgIconStop.png"></td>
        <td><b>Restart</b></td>
        <td>Atura l'execució del programa</td>
    </tr>
</table>


Quan estàs aturat en un **breakpoint**, posar el mouse sobre una variable, mostra el seu valor.

La línia que s'executarà a continuació apareix de color groc.

En aquest exemple, el **debugger** està aturat a la linia número 8, i hem posat el mouse a sobre de la **x**, per aquest motiu es veu un "10" al requadre sobre de la **x**.

<center>
<img src="./assets/dbg0305.png" style="width: 90%; max-width: 350px">
</center>

Cal tenir en compte, que en aquest moment, **y** encara no té valor. Si posem el mouse sobre de la **y** encara no apareix "5".

## Opcions avançades

Es poden posar condicions als **breakpoints** per tal que els ignori si es compleixen certes condicions.

- Amb el botó dret, fent click al **breakpoint** escollir **"edit breakpoint"**

<center>
<img src="./assets/dbg0306.png" style="width: 90%; max-width: 350px">
</center>

- Posar la condició que fa que el breakpoint s'aturi. En el següent exemple, només s'atura si **"x < 15"**

<center>
<img src="./assets/dbg0307.png" style="width: 90%; max-width: 350px">
</center>

Els **breakpoints** amb condicions apareixen amb un símbol **"="** dins del cercle vermell.

<center>
<img src="./assets/dbg0308.png" style="width: 90%; max-width: 350px">
</center>


