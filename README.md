# C.P.D. - das fun/tastische, farbenfrohe, digitale Pong Spiel!

## Von der Idee zum Spiel

[Die Idee!](#eins)

[Das Programm](#zwei)

[Das Spiel](#drei)

[Das Grundgerüst](#vier)

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
 
 
## Das Grundgerüst <a name="vier"></a>

In unserem Spiel werden folgende Globale Variablen verwendet. Globale Variablen heißt, sie werden am Anfang des Codes definiert und im weitern Spiel mit Werten belegt.

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
var Ballgeschwindigkeit;   

var counter1 = 0;  
var counter2 = 0;
```  

Unser Spiel hat verschiedene Zustände, welche im Zustandsdiagramm zusehen sind.

bild Zustandsdiagramm

Zu jedem Zustand gibt es ein Screen, wobei jeder Screen durch eine eigene init initialisiert wird und die Logic in einer jeweilligen Logicfunktion abgearbeitet wird.
Die einzelnen Zustände, bzw. Screens werden über die Hauptschleife gesteurt. Dies ist möglich durch die Boolean Variablen, die aussagen, ob eine Aussage wahr oder falsch ist. Dadurch ist es möglich, einen Screen als wahr darzustellen, während alle anderen Screens falsch sind, so dass der "wahre" Screen initialisiert wird und auch die Logicfunktion abgearbeitet wird. 

```   
// function draw (Hauptschleife)
function draw(){

  if (Screen_start_active) {
      Screen_start_logic();
  }

  if (Screen_spiel_active) {
      Screen_spiel_logic();
  }
  
  if (Screen_gameover_active){
      Screen_gameover_logic();
  }
  
  if (Screen_pause_active){
      Screen_pause_logic();
  }

  if (Screen_changed_start) {
      Screen_start_destroy();
      Screen_start_active = false;
      Screen_spiel_active = true;
      Screen_spiel_init();
      Screen_changed_start = false;
  }
  
  if (Screen_changed_pause){
      Screen_spiel_destroy();
      Screen_spiel_active = false;
      Screen_pause_active = true;
      Screen_pause_init();
      Screen_changed_pause = false;
  }
  
  if (Screen_changed_weiter){
      Screen_pause_destroy();
      Screen_pause_active = false;
      Screen_spiel_active = true;
      Screen_spiel_init();
      Screen_changed_weiter = false;
      
  }
  
  if (Screen_changed_gameover){
      Screen_spiel_destroy();
      Screen_spiel_active = false;
      Screen_gameover_active = true;
      Screen_gameover_init();
      Screen_changed_gameover = false;
  }  
  
  if (Screen_changed_neu){
      Screen_gameover_destroy ();
      Screen_gameover_active = false;
      Screen_spiel_active = true;
      Screen_spiel_init();
      Screen_changed_neu = false;
      counter1 = 0;
      counter2 = 0;
  }

drawSprites();
  
}
```   
Zu jedem Screen gibt es eine eigene if-Funktion. Das heißt wenn die Aussage Screen_start_active "wahr" ist, so wird die Funktion Screen_start_logic abgearbeitet. Dadurch kann zwischen den verschiedenen Screens gewechselt werden. 

<hr>

 
## Der Startbildschirm <a name="fünf"></a>
 
 ![Screenshot_2019-08-28 Bild-Startbildschirm](https://user-images.githubusercontent.com/54102292/63863667-e54c8300-c9ae-11e9-9a05-4cec282734e9.png)
 Neues Bild!!
 
Der Code für den Startbildschirm ist einmal in der Funktion Screen_start_init und in der Funktion Screen_start_logic zufinden.
Damit der Startbildschirm sofort zusehen ist, wenn das Programm gestartet wird, wird als erstes der Startbildschirm initialisiert.

```  
// Screen_start_init
Screen_start_init();
```  

 <details>
  <summary>function Screen_start_init</summary>
 
 
 In der Funktion Screen_start_init wurde der Hintergrund (Hintergrund_start) als weiß festgelegt. Bei der Schrift (Text_start) wird einmal die Größe, die Schriftart, die Farbe und zum Schluss noch den eigentlichen Text mit der Position, wo dieser stehen soll, festgelgt.
  
   ```
  //Hintergrund_start 
      Hintergrund_start = backround("white");  
      
  //Text_start  
      Text_start = textSize(100);  
      Text_start = textFont("Calibri");  
      Text_start = fill("blue");  
      Text_start = text("PONG", 70,200);  
  ```
  ---
 Der Startblock (Startblock) wird ebenfalls in der Funktion Screen_start_init festgelegt. Hierbei wird durch den Befehl "createSprite" festgelegt, wo dieser Startblock liegen soll. Es wird neben der x und y Position auch die Höhe und die Breite festgelgt. Durch den Befehl "setAnimation" wird der Startblock mit der entsprechenden Animation ausgegeben. Die Animation ist bei Code.org im Zeichentrickbereich hinterlegt.

```
 //Startblock  
      Startblock = createSprite (200,285,150,50);  
      Startblock.seeAnimation("flatDark41_1");  
```
---
Der Ball welcher auf dem Startbildschirm "herumfliegt" wird ebenfals in dieser Funktion definiert. Hierbei wird einmal festgelgt das der Ball ein "EdgeSprite" ist, das bedeutet das sobald er eine Bildschirmseite berührt abprallt. Dies ist ein vorgefertigter Befehl von Code.org. Auch hier haben wir wieder ein Sprite definiert mit einer x,y Koordinate. Ebenfalls haben wir die Weite und Höhe des Balles definiert und auch eine Farbe.
Damit der Ball sich bewegt, haben wir ebenfalls einen vorgefertigten Befehl von Code.org benutzt. Dieser heißt "Ball.velocity" wobei dann immer die jeweillige Achse mit rangehängt wird (Ball.velocityX). Damit wird die Geschwindigkeit in x- oder y- Richtung bestimmt.

```
//Ball
    createEdgeSprites();
    Ball = createSprite ();
      Ball.x = 200;
      Ball.y = 200;
      Ball.width = 15;
      Ball.height = 15;
      Ball.shapeColor = "red";
      
      Ball.velocityX = 8;
      Ball.velocityY = 5;
  ``` 
  ---
Desweitern haben wir in dieser Funktion auch die Bildschirmgrenze definiert. Diese haben wir in Abhängikeit zur Spielfeldgröße gesetzt. Somit ist es egal, in welcher Größe das Spielfeld angezeigt wird. Dies haben wir mit dem Befehl World.height, bzw. World.width gemacht.
  ```
//Screen_height_start
    Screen_height = 0;

//Screen_bottom_start
    Screen_bottom = World.height;
      
//Screen_Rand_links
    Screen_rand_links = 0;
      
//Screen_Rand_rechts
    Screen_rand_rechts = World.width;
```
---
    
  
  ![Screenshot_2019-08-28 Startbutton-Bild](https://user-images.githubusercontent.com/54102292/63864321-ed58f280-c9af-11e9-909a-866e0d629293.png)

  </details> 

<details>
  <summary>function_screen_start_destroy</summary>
  
  
  
  
  
  
  </details>

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
  
  
