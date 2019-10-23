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
  
<details>
  <summary>Farbcode</summary>
 Während man auf code.ord programmiert, wird man mit verschidenen Typen und Farben konfrontiert. Dabei variieren die Farben je nachdem in welcher Sprache man programmiert.
  
  Die Bausteine:
  * eine programmiete _Funktion_ ist immer grün
  * ein Baustein, der die _World_ beschreibt und definiert ist immer gelb
  * ein _Sprite_ oder _Groupe_ ist immer rot
  * die Bauteine der Kategorie _Drawing_ ist immer hellblau
  * ein Comment wird grau angezeigt
  * ein Baustein aus _Kontroll_ ist in einem mittelblau
  * eine Variable ist lila angezeigt
  * die Kategorie _Mathe_ ist orange
  
In diesem Spiel wurde allerdings in Javaskript geschrieben. Auch hier gibt es in code.org einen Farbencode, jedoch unterscheiden sich diese von dem Bausteincode.

  * die Variablen _var_ sowie die Funktionen wie zum Beispiel _if_ werden lila angezeigt
  * _Comments_ sind grün 
  * variierbare Element wie _Farben_ oder _Positionsangaben_ werden blau angezeigt
  * alle aderen _Texte_ sind grau
  * die Boolean, welche _true_ und _false_ definieren, sind blau
  
  </details>
  
  <hr>
 
 
## Das Spiel <a name="drei"></a>  

Hier in diesem Spiel wird der alte Klassiker PONG aufgegriffen und verbessert. Der Spieler hat die Möglichkeit das Spiel mit einem Klick auf den Startbotton zu beginnen. Im Spiel selbst 
 
 <hr>
 
 
## Die Variablen <a name="vier"></a>

In dem gesammten Spiel werden globale Variablen verwendet. Diese beziehen sich auf das gesammte Spiel und werden sie direkt am Anfang definiert und in allen weiteren Codes verwendet.

```  
var Hintergrund_start;  
var Hintergrund_spiel;  
var Hintergrund_gemeover;  
var Hintergrund_pause;  

var Schlaeger_links;  
var Schlaeger_rechts;  
var Schlaegergeschwindigkeit = 10;  

var Mittellinie;  

var Startblock;  
var New_game_block;  
var Pauseknopf;  

var Text_start;  
var Text_gameover;  

var Screen_start_active = Boolean (true);  
var Screen_spiel_active = Boolean (false);  
var Screen_gameover_active = Boolean (false);  
var Screen_pause_active = Boolean (false);  

var Screen_changed_start = Boolean (false);  
var Screen_changed_pause = Boolean (false);  
var Screen_changed_gameover = Boolean (false);  
var Screen_changed_neu = Boolean (false);  
var Screen_changed_weiter = Boolean (false);  

var Screen_hight;  
var Scgreen_bottom;  
var Screen_rand_links;  
var Screen_rand_rechts;  

var Ball;  

var counter1 = 0;  
var counter2 = 0;
```  
<hr>

 
## Der Startbildschirm <a name="fünf"></a>
 
 ![Screenshot_2019-08-28 Bild-Startbildschirm](https://user-images.githubusercontent.com/54102292/63863667-e54c8300-c9ae-11e9-9a05-4cec282734e9.png)
 Neues Bild!!
 
 <details>
  <summary>Hintergrund</summary>
  Hierbei wurde ien weißer Hintergrund mit blauene Großbuchstaben gewählt. Dies steht im Kontrast zu dem Starbutton gebildet, weshalb es für den Spieler ansprechender gestalttet wurde.
  </details>
  
<details>
  <summary>Startbutton</summary>
  Der Startbildschirm wurde mit einer vorgefertigten Animation aus der Animationsbibliothek von code.org gestallt. Hierbei kann durch einen Mausklick auf den Startbutton der Startbildschirm verlassen wreden und das eigentliche Spielfeld erscheint. Als Design wurde ein schwarzes Rechteck mit weißen Großbuchstaben.
  
  ![Screenshot_2019-08-28 Startbutton-Bild](https://user-images.githubusercontent.com/54102292/63864321-ed58f280-c9af-11e9-909a-866e0d629293.png)

  </details> 
  
<details> 
  <summary>Code</summary>  
  
  ```
  //function Screen_start_init  
  function Screen_start_init() {  
  
  //Hintergrund_start 
      Hintergrund_start = backround("white");  
      
  //Text_start  
      Text_start = textSize(100);  
      Text_start = textFont("Calibri");  
      Text_start = fill("blue");  
      Text_start = text("PONG", 70,200);  
      
  //Startblock  
      Startblock = createSprite (200,285,150,50);  
      Startblock.x = 200;  
      Startblock.y = 285;  
      Startblock.seeAnimation("flatDark41_1");  
      
  //Ball
  ```
  <hr>
 
 
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
  
  
