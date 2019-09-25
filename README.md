# Projekt-im-Informatikkurs

## Von der Idee zum Spiel

[Die Idee!](#eins)

[Das Programm](#zwei)

[Das Spiel](#drei)

[Die Variablen](#vier)

[Der Startbildschirm](#fünf)

[Das Spielfeld](#sechs)


## Die Idee! <a name="eins"></a>

Ein altes Spiel, welches aber jeder kennt. **PONG!** Das Spiel ist angelehnt an den Klassiker. Jedoch sind einige Funktionen hinzugefügt. Im Folgenden Blog werden alle Funktionen, sowie der Code für das Spiel erklärt und dargestellt.
<hr>


## Das Programm <a name="zwei"></a>
### code.org

<details>
  <summary>Grundsätzlich</summary>
  
  * Schüler sollen weltweit kostenlosen Zugang haben Informatik zu lernen. 
  * Über diese Seite kann der Lehrer einen Lehreraccount erstellen, sodass er alle Projekte der Schüler jederzeit abrufen kann. 
  * Mehrere Unternehmen unterstützen code.org. Z.B. Google, Microsoft und viele mehr.
  
  </details>

<details>
  <summary>Kurse</summary>
  Bei code.org können Nutzer auch ohne Anmeldung Kurse zum Thema programmieren machen. Dabei werden in verschiedene Altersstufen unterschieden. Auch gibt es Kurse für Nichtleser, sodass auch schon die Kleinsten programmieren lernen können.
  </details>
  
<details>
  <summary>Programmierfunktion</summary>
 Auf code.org können verschiedenen Module benutzt werden um ein Spiel oder sonstiges programmieren zu können. Um nun ein Spiel programmieren zu können, wird das Spielelabor ausgewählt. In diesem Labor kann alles auprobiert werden. code.org stellt bereits vorgefertigte Baussteine zur Verfügung. Diese können als Bausteine angezeigt werden oder aber auch als Javaskipt. Auch lassen sich eigende nicht vorhandene Befehle programmieren, wobei das Programm nicht alle Javaskript funktionen kennt.
  Es kann somit für Angfänger sowie fortgeschrittene leicht programmiert werden.
  Im App-Labor könne Spiele in Form einer App programmiert werden. Dadurch lassen sich diese Spiele auch auf Tablets oder Handys spielen. 
  </details>
  
  <hr>
 
 
## Das Spiel <a name="drei"></a>
 
 <hr>
 
 
## Die Variablen <a name="vier"></a>

In dem gesammten Spiel werden Boolean Variablen verwendet. Diese beziehen sich auf das gesammte Spiel und sind globale Variablen. Dadurch werden sie direkt am Anfang definiert und in allen weiteren Codes verwendet.

```  
var Hintergrund2;  

var Schlaeger_links;  
var Schlaeger_rechts;  
var Schlaegergeschwindigkeit = 10;  

var Mittellinie;
```  
<hr>

 
## Der Startbildschirm <a name="fünf"></a>
 
 ![Screenshot_2019-08-28 Bild-Startbildschirm](https://user-images.githubusercontent.com/54102292/63863667-e54c8300-c9ae-11e9-9a05-4cec282734e9.png)

 
 <details>
  <summary>Hintergrund</summary>
  Hierbei wurde ien weißer Hintergrund mit blauene Großbuchstaben gewählt. Dies steht im Kontrast zu dem Starbutton gebildet, weshalb es für den Spieler ansprechender gestalttet wurde.
  
  ![Screenshot_2019-08-28 Code-Startbildschirm](https://user-images.githubusercontent.com/54102292/63863940-4ffdbe80-c9af-11e9-87ec-1d861c2b6eb7.png)

  </details>
  
<details>
  <summary>Startbutton</summary>
  Der Startbildschirm wurde mit einer vorgefertigten Animation aus der Animationsbibliothek von code.org gestallt. Hierbei kann durch einen Mausklick auf den Startbutton der Startbildschirm verlassen wreden und das eigentliche Spielfeld erscheint. Als Design wurde ein schwarzes Rechteck mit weißen Großbuchstaben.
  
  ![Screenshot_2019-08-28 Startbutton-Bild](https://user-images.githubusercontent.com/54102292/63864321-ed58f280-c9af-11e9-909a-866e0d629293.png)
  
  ![Screenshot_2019-08-28 Startbutton-Code](https://user-images.githubusercontent.com/54102292/63864378-06fa3a00-c9b0-11e9-8c4e-9fbb9343c465.png)

  </details> <hr>
 
 
 ## Das Spielfeld <a name="sechs"></a>
 
 <details>
  <summary>Hintergrund und Mittellinie</summary>
  Der Hintergrund ist in einem einnafchen grau gehlten, damit alle weiteren Inhalte besser zu sehen ist.

  ![Screenshot_2019-08-28 Mittellinie-Hintergrund-Code](https://user-images.githubusercontent.com/54102292/63867479-32cbee80-c9b5-11e9-8251-13f84a6361c0.png)
  
  </details>
  
<details>
  <summary>Schläger</summary>
  Die Schläger können durch Tastenkombinationen bewegt wreden. Der Rechte, also blaue, Schläger wird durch die Pfeilentaste "Hoch" und "Runter" bewegt. Der Linke, also rote, Schläger kann durch "W" hoch und durch "S" runter bewegt werden. Beide Schläger steoppen am Ende des Spielfeldes. 
  Die Mittelinie ist für den Spieler eingezeichent worde. Dadurch lässt leichter die eigene Hälfte erkennen. Sie hat dadurch für die Grundfunktionen keine Funktion.
  
  (Code einfügen)
  
  </details>
  
<details>
  <summary>Ball</summary>
  
  </details>
  
<details>
  <summary>Zählstand</summary>
  
  </details>
  
  
