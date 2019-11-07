# C.P.D. - das fun/tastische, farbenfrohe, digitale Pong Spiel!

## Von der Idee zum Spiel

[Die Idee!](#eins)

[Das Programm](#zwei)

[Das Spiel](#drei)

[Das Grundgerüst](#vier)

[Der Startbildschirm](#fünf)

[Das Spielfeld](#sechs)

[Die Pause](#sieben)

[Gameover](#acht)


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
  
![Screenshot_2019-11-06 Kurs-Blog](https://user-images.githubusercontent.com/54102292/68305936-dbc75180-00a8-11ea-8260-d0db680c4457.png)
  
Hier wird ein möglicher Kurs gezeigt. Hierbei soll der Benutzer den Künstler durch das Einsezten der vorhandenen Bausteine dazu bringen das vorgegebene Muster nachzumalen.  

![InkedScreenshot_2019-11-06 Kurs-fertig-Blog_LI](https://user-images.githubusercontent.com/54102292/68306539-04038000-00aa-11ea-95e8-10e89e56c5b5.jpg)

Wenn die Bausteine eigefügt sich und auf den Startbutton geklickt wird, dann beginnt der Künstler zu zeichnen und mit den richtigen Variablen (mit roten Pfeilen markiert) an der richtigen Stelle wird auch das gezeichnet. Klickt man auf den Progarmm zeigen Button (mit dem grünen Pfeil mariert), so wird der Javascriptcode angezeigt.

  ![Screenshot_2019-11-06 Kurs-Progamm-Blog](https://user-images.githubusercontent.com/54102292/68306932-b89da180-00aa-11ea-830a-a4265b615904.png)
  
  </details>
  
<details>
  <summary>Programmierfunktion</summary>
 Auf code.org können verschiedenen Module benutzt werden um ein Spiel oder sonstiges programmieren zu können. Um nun ein Spiel programmieren zu können, wird das Spielelabor ausgewählt. In diesem Labor kann alles auprobiert werden. code.org stellt bereits vorgefertigte Baussteine zur Verfügung. Diese können als Bausteine angezeigt werden oder aber auch als Javaskipt. Auch lassen sich eigende nicht vorhandene Befehle programmieren, wobei das Programm nicht alle Javaskript funktionen kennt.
  Es kann somit für Angfänger sowie fortgeschrittene leicht programmiert werden.
  Im App-Labor könne Spiele in Form einer App programmiert werden. Dadurch lassen sich diese Spiele auch auf Tablets oder Handys spielen.   
  Hierbei muss allerdings beachtet werden, dass code.org teilweise eigene Befehle verwendet, sodass eine Recherche für Javascriptbefehle schwierig wird, da das Programm diese oftmals nicht kennt. Dadurch muss der Benuzer vieles ausprobieren und kommt hauptsächlich mit den code.org Befehlen zu seinem Ziel
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

In unserem Spiel verwenden wir globale Variablen. Das heißt sie werden im Gegensatz zu lokalen Variablen am Anfang des Codes definiert und im weitern Spiel mit Werten belegt. Lokale Variablen werden erst in einer Funktion definiert und mit Werten belegt, allerdings kann dann auch nur diese Funktion auf die Variable zugreifen. Bei globalen Variablen können alle Funktion auf die Variablen zugreifen und diese mit Werten belegen.

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

var Screen_hight;  
var Scgreen_bottom;  
var Screen_rand_links;  
var Screen_rand_rechts;  

var Ball;  
var Ballgeschwindigkeit;   

var counter1 = 0;  
var counter2 = 0;
```
---
In unserem Variablen haben wir auch Boolean Variablen benutzt. Diese können Aussagen, wie zum Beispiel Screen_start_active, als "wahr" (true) oder "falsch" (false) definieren. Somit kann inerhalb einer if-Funktion zum Beispiel gesagt werden, wenn die Aussage "wahr" ist, soll 

var Screen_start_active = Boolean (true);  
var Screen_spiel_active = Boolean (false);  
var Screen_gameover_active = Boolean (false);  
var Screen_pause_active = Boolean (false);  

var Screen_changed_start = Boolean (false);  
var Screen_changed_pause = Boolean (false);  
var Screen_changed_gameover = Boolean (false);  
var Screen_changed_neu = Boolean (false);  
var Screen_changed_weiter = Boolean (false);  


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
Der Ball welcher auf dem Startbildschirm "herumfliegt" wird ebenfals in dieser Funktion definiert. Auch hier haben wir wieder ein Sprite definiert mit einer x,y Koordinate. Ebenfalls haben wir die Weite und Höhe des Balles definiert und auch eine Farbe.
Damit der Ball sich bewegt, haben wir ebenfalls einen vorgefertigten Befehl von Code.org benutzt. Dieser heißt "Ball.velocity" wobei dann immer die jeweillige Achse mit rangehängt wird (Ball.velocityX). Damit wird die Geschwindigkeit in x- oder y- Richtung bestimmt.

```
//Ball
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
  <summary>function Screen_start_logic</summary>
  
  Als erstes haben wir nochmal den Hintergrund und den Text definiert, damit der Ball welcher über den Bildschirm fliegt auch zu sehen ist und es nicht zu einer langen Reihe an Bällen kommt.
  Damit der Ball am Bildschirm Rand abprallt, haben wir if Funktion definiert. Die besagen, dass wenn der Ball den Bildschirmrand berührt, die Ballgeschwindigkeit (Ball.velocity) sich vom Vorzeichen her umdreht (mal -1). Dadurch verändert sich der X- bzw. Y-Wert, undsomit die Richtung des Balles. Dies haben wir bei allen vier Bildschirmrändern getan.  
  ```
//Ball.isTouching Screen_height
  if (Ball.y < Screen_height){
      Ball.velocityY = -1*Ball.velocityY;
  }
  
//Ball.isTouching Screen_bottom
  if (Ball.y > Screen_bottom){
      Ball.velocityY = -1*Ball.velocityY;
  }

// Ball.x < Screen_rand_links 
 if (Ball.x < Screen_rand_links){
      Ball.velocityX = -1*Ball.velocityX;
  }

// Ball.x > Screen_rand_rechts 
  if (Ball.x > Screen_rand_rechts){
      Ball.velocityX = -1*Ball.velocityX;
  }
```
---

Damit das Spiel gestartet werden kann, haben wir den Startblock. Wenn man auf diesen mit der Maus klickt, erklingt ein Sound, welchen wir aus der Soundbibliothek von Code.org haben. Desweitern wird definiert, das die Aussage Screen_changed_start "wahr" ist. Dadurch "springt" der Computer wieder in die Hauptschleife, um dort die if-Funktion für Screen_changed_start auszuführen.

```
// mousePressedOver (Startblock)
  if (mousePressedOver(Startblock)){
      Screen_changed_start=true;
      playSound ("https://audio.code.org/start1.mp3");
  }
```
  </details>
  
<details>
  <summary>function_screen_start_destroy</summary>
  
 In werden alle Angaben, welche wir in Screen_start_init gemacht haben "zerstört". Das heißt sie werden nicht mehr auf dem Bildschirm angezeigt, können aber falls man wieder in Screen_start_init kommt, wiederhergestellt werden. Diese Funktion brauchen wir, um zwischen den einzelnen Screens wechseln zu können.
 
``` 
function Screen_start_destroy (){
 
    Hintergrund_start.destroy;
    Text_start.destroy;
    Startblock.destroy();
    Ball.destroy();
}
``` 
</details>

 
 ## Das Spielfeld <a name="sechs"></a>
 
 <details>
  <summary>function Screen_spiel_init</summary>
Durch die Hauptschleife kommt man nun in die init-Funktion vom "Spiel". Als erstes haben wir wieder den Hintergrund (Hintergrund_spiel) defieniert. Hier haben wir uns für Grün entschieden, da wir somit eine Tischtennisplatten emittieren können. Desweitern haben wir noch eine Mittellinie (Mittellinie) definiert, damit die Spieler besser in die zwei Hälften unterscheiden können.
  
  ```
// Hintergrund_Spiel
    Hintergrund_spiel = background("green");

// Mittellinie
    Mittellinie = stroke("yellow");
    Mittellinie = strokeWeight("1");
    Mittellinie = line(World.wdith/2,World.height);
```
--- 

Die Schläger (Schlaeger_rechts / Schlaeger_links) haben wir wieder durch den Befehl createSprite programmiert. Die Schläger haben wir in Abhängigkeit zur Bildschirmgröße gesetzt, damit es egal ist, wie groß dieser später ist. Dies haben wir durch die World.height / bzw. World.width gemacht. So ist die Höhe der Schläger zum Beispiel ein achtel der Bildschirmgröße (World.width/8). So ist gewährleistet, dass der Schläger nicht zu klein, zu groß, zu breit, zu dünn für den Bildschrim ist. Auch haben wir die Position in Abhängigkeit zur Bildschirmgröße gestzt, so dass der Abstand zum Bildschirmrand immer gleich ist.
Die Schläger haben wir mit unterschiedlichen Farben belegt, damit man diese besser auseinanderhalten kann und die Spieler so einer Farbe zugewiesen werden.

```
//Schläger_rechts
    Schlaeger_rechts = createSprite ();
      Schlaeger_rechts.x = World.height/1.08;
      Schlaeger_rechts.y = World.height/2;
      Schlaeger_rechts.width = World.width/40;
      Schlaeger_rechts.height = World.width/8;
      Schlaeger_rechts.shapeColor = "blue";

//Schläger_links
    Schlaeger_links = createSprite();
      Schlaeger_links.x = World.height/13.33;
      Schlaeger_links.y = World.height/2;
      Schlaeger_links.width = World.width/40;
      Schlaeger_links.height = World.height/8;
      Schlaeger_links.shapeColor = "red";
```
--- 
Auch in dieser Funktion haben wir die Spielgröße definiert, allerdings anders als beim Startbildschirm. Die Ränder Links und Rechts (Screen_rand_links / Screen_rand_rechts) sind gleich geblieben. Die Höhe des Spielfeldes haben wir mit der Schlägergröße in Zusammenhang gesetzt. Da die normale Höhe in unserem Fall 0 ist, haben wir hier die Schlägergröße durch zwei grechnet, damit der Schläger nicht zur Hälfte verschwindet, da der Fixpunkt des Schläger die Mitte ist, wenn man ihn nach oben bewegt. Die Unterseite des Spielfeldes, haben wir durch die Bildschirmgröße (World.height) minus die Schlägergröße (Schlaeger_links.height)
durch zwei definiert. Dadurch verschwindet der Schläger beim runterbewegen auch nicht zur Hälfte, aufgrund des Fixpunktes in der Mitte des Schlägers.

```   
//Screen_height_spiel = (Schlägergröße / 2)
    Screen_height = (Schlaeger_links.height / 2);

//Screen_bottom_spiel = Bildschirmgröße - (Schlägergröße / 2)
    Screen_bottom = World.height - (Schlaeger_links.height / 2); 
      
//Screen_Rand_links
    Screen_rand_links = 0;
      
//Screen_Rand_rechts
    Screen_rand_rechts = World.width;
```
---

Den Spielball haben wir wie in der Funktion Screen_start_init definiert. Durch createSprite und die jeweilligen Größenangaben und Koordinaten. Diese mal haben wir den Ball mit der Farbe weiß belegt, damit er angepasst zum restlichen Spiel ist.

```
//Ball
    Ball = createSprite ();
      Ball.x = 200;
      Ball.y = 200;
      Ball.width = 15;
      Ball.height = 15;
      Ball.shapeColor = "white" ;
```
Die Ballgeschwindigkeit, wird hier zufällig gewählt. Dies haben wir durch ein Funktion (function zufaellige_zahl) ausgedrückt. Hierbei wird für die Geschwindigkeit und Richtung eine zufällige Zahl zwischen -8 und 8 (randomNumber (-8,8)) vom Computer ausgewählt. Wenn diese bei der X-Koordinate allerdings null beträgt, greift die if-funktion Ball.velocityX = 0. Dort wird die Geschwindigkeit mit einer festen Zahl belegt. Dies haben wir gemacht, damit der Ball nicht in der Mitte des Spielfeldes sich nur nach oben und unten bewegt.

```
Ballgeschwindigkeit = zufaellige_zahl();
  function zufaellige_zahl (){
    Ball.velocityY = randomNumber (-8,8);
    Ball.velocityX = randomNumber (-8,8);
    if (Ball.velocityX == 0){
      Ball.velocityX = 3.5;
    }
  }
```
  </details>
  
<details>
  <summary>Screen_spiel_logic</summary>
Auch hier haben wir den Hintergrund und die Mittellinie nochmals definiert, damit der Ball sich auch wirklich bewegt und es sich nicht mehrer Bälle bilden.
Desweitern haben wir hier den Spielstand (counter1 /counter2) eingefügt, dieser ist eine Variable, welche wir bei den globalen Variablen mit null belegt haben. Diese Variablen wird nun durch den Befehl text angezeigt. 
 
```
// Hintergrund2
    Hintergrund_spiel = background("green");

// Mittellinie
    Mittellinie = stroke("white");
    Mittellinie = strokeWeight("5");
    Mittellinie = line(200,0,200,400);

//Counter 
    fill ("white");
    text(counter1,130,80);
    text(counter2,220,80);
```
---
Damit der Ball während des Spieles, dass heißt zwischen zwei Punkten, nicht bei der gleichen Geschwindigkeit bleibt, haben wir den Ball so programmiert, dass dieser mit der Zeit schneller wird. Allerdings nimmt er eher langsam an Geschwindigkeit zu, damit er falls der Ball grundsätzlich eher schneller ist nicht zu schnell wird. Das schnellerwerden haben wir durch den Befehl Ball.getSpeedAndDirection programmiert. Hierbei wird die Geschwindigkeit immer um 0,005 erhöht und die Richtung bleibt gleich.

```
//Ball wird schneller
    Ball.setSpeedAndDirection(Ball.getSpeed()+0.005,Ball.getDirection()+0);
 ``` 
 --- 
 Wenn der x-Koordinate des Balles (Ball.x) größer ist als der Wert für den linken Bildschrimrand (Scree_rand_links), wird der entsprechende Zählstand um eins ehöt und der Ball wird wieder in der Mitte des Spielfeldes angezeigt.
Der Zählstand wird um eins erhöt, in dem beim entsprechenden Counter +1 gerechnet wird. 
Beim Ball werden x- und y-Koordinaten festgelegt, wo dieser wieder auftauchen soll, nach dem er über den Bildschirmrand geflogen ist. Damit der Ball nicht immer in die gleiche Richtung fliegt und auch nicht immer die gleiche Geschwindigkeit hat, haben wir diese (Ball.velocity) wieder mit einer zufälligen Zahl (randomNumber) belegt. Dabei haben wir den Zahlenbereich immer so festgelgt, dass der Ball auf die Spielhälfte fliegt, als ob der Spieler der ein Punkt gemacht hat, einen Aufschlag ausführen würde. Das heißt, beim linken Rand ist der Bereich der x-Geschwindigeit -8 bis -4 und die y-Geschwindigkeit -8 bis 8. Somit fliegt der Ball zuerst in die linke Spielfeldhälfte. Allerdings immer in einem anderen Winkel, so dass dies nicht absehbar ist. Beim rechten Spielfeldrand ist es genauso, nur das der Bereich der x-Geschwindigkeit 4 bis 8 ist und die y-Geschwindigkeit einen Bereich von -8 bis 8 hat.

```
// Ball.x < Screen_rand_links counter2  
   if (Ball.x < Screen_rand_links){
  
      Ball.velocityX = randomNumber (-8,-4);
      Ball.velocityY = randomNumber (-8,8);
      Ball.x = 200;
      Ball.y = 200;
      counter2 += 1;
  }

// Ball.x > Screen_rand_rechts counter1 
  if (Ball.x > Screen_rand_rechts){
    
      Ball.velocityX = randomNumber (4,8);
      Ball.velocityY = randomNumber (-8,8);
      Ball.x = 200;
      Ball.y = 200;
      counter1 += 1;
  }
  ```
  --- 
  Auch haben wir einen "Drall" des Balles programmiert. Wenn der Schläger sich bewegt, während der Ball diesen trifft, prallt er in einem anderen Winkel ab, als wenn der Schläger sich nicht bewegen würde. Das heißt damit dieser Drall durchgeführt wird, müssen die Bedingungen, dass der Schläger sich bewegt und das der Ball den Schläger brührt, beide erfüllt sein. Dies haben wir durch eine if-Funktion definiert. Wenn diese Bedingungen beide erfüllt werden, wird die y-Geschwindigkeit (Ball.velocityY) des Balles - bzw. + 1,5 gerechnet. - wird gerechnet, wenn der Schläger sich nach oben bewegt und + wenn der Schläger sich nach unten bewegt. Dadurch verändert sich die Richtung sowie auch zum Teil die Geschwindigkeit.

```
// Drall beim Wegziehen Schlaeger_links
  if (keyDown("W") && Ball.isTouching (Schlaeger_links)){
      Ball.velocityY -= 1.5;
  }
  if (keyDown ("S") && Ball.isTouching (Schlaeger_links)){
      Ball.velocityY +=1.5;
  }
  
// Drall beim Wegziehen Schlaeger_rechts
  if (keyDown ("up") && Ball.isTouching (Schlaeger_rechts)){
      Ball.velocityY -=1.5;
  }
  if (keyDown ("down") && Ball.isTouching (Schlaeger_rechts)){
      Ball.velocityY +=1.5;
  }
  ```
  --- 

Die Schlägerbewegung haben wir an Tasten gebunden. So sind die Tasten "W" und "S" für den linken Schläger, zum hoch und runter bewegung. Und die Pfeiltasten für den rechten Schläger zum hoch und runter bewegen. 
Auch dies haben wir wieder durch eine if-Funktion programmiert. Diese sagt aus, dass wenn der die Taste sich nach unten bewegt (keyDown), das die y-Koordinate des Schlägers um die Schlägergeschwindigkeit addiert oder subtrahiert wird. Die Schlägergeschwindigkeit haben wir in den globalen Variablen mit 10 definiert. Das heißt die y-Koordinate wird immer um 10 subtrahiert, bzw. addiert. Desweitern haben wir in der Bedingung der if-Funktion noch definiert, dass der die y-Koordinate (Schlaeger_links.y) nicht größer bzw. kleiner als die Bildschirmhöhe bzw. der Bildschirmrand unten sein darf. 

```
// keyDown (up)
  if (keyDown("W")&& (Schlaeger_links.y > Screen_height)){
      //Schlaeger_links.y = Schlaeger_links.y-Schlaegergeschwindigkeit;
        Schlaeger_links.y -= Schlaegergeschwindigkeit;
  }

//keyDown (down)
  if (keyDown("S")&& (Schlaeger_links.y < Screen_bottom)) {
     //Schlaeger_links.y = Schlaeger_links.y + Schlaegergeschwindigkeit;
      Schlaeger_links.y += Schlaegergeschwindigkeit;
  }

//keyDown (W)
  if (keyDown("up")&&(Schlaeger_rechts.y > Screen_height)) {
      //Schlaeger_rechts.y = Schlaeger_rechts.y - Schlaegergeschwindigkeit;
        Schlaeger_rechts.y -= Schlaegergeschwindigkeit;
  }

//keyDown (S)
  if (keyDown("down")&&(Schlaeger_rechts.y < Screen_bottom)) {
     //Schlaeger_rechts.y = Schlaeger_rechts.y + Schlaegergeschwindigkeit;
      Schlaeger_rechts.y += Schlaegergeschwindigkeit;
  }
```
--- 
Damit der Ball auch vom Schläger abprallt, haben wir beim Drall eine if-Funktion programmiert, die ausgeführt wird, wenn der Ball den Schläger berührt. Dies haben wir durch Ball.isTouching definiert. Wenn der Ball nun den Schläger berührt, wir die x-Geschwindigkeit (Ball.velocityX) des Balles mal -1 gerechnent, da diese sich somit ändert und der Ball in dem Winkel Einfallswinkel = Ausfallswinkel weiterfliegt.
Außerdem wird immer ein Sound gespielt, welcher aus der Soundbibliothek von Code.org ist. Dies haben wir  über den Befehl playSound programmiert.

```
//Ball.isTouching Schlaeger_links
  if (Ball.isTouching(Schlaeger_links)){
      Ball.velocityX = -1*Ball.velocityX;
      playSound ("https://audio.code.org/goal1.mp3");
      
  }
  
//Ball.isTouching Schlaeger_rechts
  if (Ball.isTouching(Schlaeger_rechts)){
      Ball.velocityX = -1*Ball.velocityX;
      playSound ("https://audio.code.org/goal1.mp3");

``` 
--- 
Damit der Ball wie auf dem Startbildschirm von der oberen Kante des Bildschirmes und der unteren Kante des Bildschirmes abprallt, haben wir auch hier ein if-Funktion programmiert. Sobald die y-Kooradinate des Balles (Ball.y) kleiner bzw. größer als die Bildschirmhöhe (Screen_height) bzw. Blidschirmunterkante (Screen_bottom) wird auch hier die y-Geschwindigkeit (Ball.velocityY) mit -1 multipliziert. Desweiteren wird bei der x-Geschwindigkeit (Ball.velocityX) plus eins gerechnet.

```
//Ball.isTouching Screen_height
  if (Ball.y < Screen_height){
      Ball.velocityY = -1*Ball.velocityY;
      Ball.x = Ball.x+1;
  }
  
//Ball.isTouching Screen_bottom
  if (Ball.y > Screen_bottom){
      Ball.velocityY = -1*Ball.velocityY;
      Ball.x = Ball.x+1;
  }
  
  ```
  --- 
  Um das Spiel zu pausieren, muss man die Leertaste drücken. Dies haben wir wieder durch eine if-Funktion programmiert. Sobald die Leertaste gedrückt wird (keyDown), wird die Aussage Screen_changed_pause als "wahr" definiert. Dadurch wird durch die Hauptschleife der Bildschirm für die Pause initalisiert.

```
// Pause
  if (keyDown ("space")){
      Screen_changed_pause = true;
  }
```
--- 
Das gleiche wie bei der Pausefunktion gilt auch bei der Gameoverfunktion. Nur das hier die Bedingung erfüllt sein muss, dass einer der Beiden counter die 10 als Wert haben muss. Dann wird auch hier die Aussage Screen_changed_gameover als "wahr" definiert. Desweitern wird noch ein Sound gespielt, welcher wieder durch den Befehl playSound ausgeführt wird.

```
// Game Over
  if (counter1 === 10 || counter2 === 10 ){
      Screen_changed_gameover = true;
      playSound ("https://audio.code.org/failure3.mp3");
  }
}
```  
  </details>
  
<details>
  <summary>function Screen_spiel_destroy</summary>
  Genauso wie beim Startbildschirm haben wir auch hier wieder ein destroy-Funktion. Diese brauchen wir, damit wir zwischen den Screens wechslen können.
  
  ```
  Hintergrund_spiel.destroy;
  Mittellinie.destroy;
  Schlaeger_rechts.destroy ();
  Schlaeger_links.destroy ();
  Ball.destroy ();
  
  ```  
  </details>
  
  ## Die Pause <a name="sieben"></a>
  
  <details>
  <summary>function Screen_pause_init</summary>
  In der init-Funktion haben wir wie bei den anderen Zuständen den Hintergrund definiert. Auch haben wir den Zählstand anzeigen lassen, damit die Spieler auch während der Pause immer wissen wie es steht. Um weiter Spielen zu können, haben wir wie beim Startblock eine Animation für einen Continue-knopf eingefügt.
  
  ```
  //Hintergrund_pause
    Hintergrund_pause = background ("green");
  
//Pauseknopf
    Pauseknopf =createSprite (200,300,200,200);
      Pauseknopf.setAnimation("continue.jpg_1");

//Counter
    
    text(counter1,130,80);
    text(":", 190,70);
    text(counter2,220,80);
 
 ```
   </details>
   
   <details>
  <summary> function Screen_pause_logic</summary>
  In der logic-Funktion wurde nur definiert, was passiert wenn der der Continue-Knopf gedrückt wird. Dies haben wir durch eine if-Funktion und den mousePressedOver Befehl ausgerückt. Wenn der Knopf gedrückt wird, wird die Aussage Screen_changed_weiter als "wahr" definiert und durch die Hauptschleife wird das Spiel wieder initalisiert und es kann weiter gespielt werden.
  
  ```
   if (mousePressedOver (Pauseknopf)){
      Screen_changed_weiter = true;
      playSound ("https://audio.code.org/start1.mp3");
  }
  ```
  </details>
  <details>
  <summary> function Screen_pause_destory</summary>
 Wie bei allen Screens haben wir auch hier eine destroy-Funktion, damit zwischen den Screens gewechselt werden kann. 
  
  ```
   Hintergrund_pause.destroy;
    Pauseknopf.destroy();
 ``` 
</details>

## Gameover <a name="acht"></a>

<details>
<summary> function Screen_gameover_init</summary>
Der letzte Zustand den es gibt ist Gameover bzw. das einer der beiden Spieler gewonnen hat. Auch hier haben wir wie bei den vorherigen Zuständen auch mit einer init-Funktion angefangen. 
Hierbei haben wir zuerst den Hintergrund (background) schwarz definiert und den Zählstand wieder als Text ausgegeben.

```
// Hintergrund_gameover
    Hintergrund_gameover = background ("black");
    
// Counter
    
    text(counter1,100,80);
    text(":", 200,70);
    text(counter2,230,80);
```
--- 
Damit klar wird wer gewonnen hat, haben wir einen Text ausgeben lassen, der aber unterschiedlich ausfällt, da es davon abhängt wer gewonnen hat. Dies kontrollieren wir wieder über eine if-Funktion. Das heißt der Spieler dessen counter-Variable den Wert 10 bekommt den Text ausgegeben. So wird zum Beispiel wenn Spieler 1 gewonnen hat der Text: "You won red" ausgegeben. Beim Text haben wir dann noch definiert, wo, wie groß und welche Schriftart ausgegeben werden soll.

```
// Text = GameOver
  if (counter1 === 10){
      Text_gameover = textSize(50);
      Text_gameover = textFont("Calibri");
      Text_gameover = text("You won red", 70,200);
      
  }
  
  if (counter2 === 10){
      Text_gameover = textSize ("50");
      Text_gameover = textFont ("Calibri");
      Text_gameover = text ("You won blue", 70,200);
  }
```
 ---
 Damit man das Spiel nach einer Partie nochmal spielen kann, ohne das gesamte Programm neu starten zu müssen haben wir einen New_Game-Block programmiert. Auch hier haben wir wieder eine Animation aus dem Zeichentrickfilm Bereich von code.org benutzt. Den New-Game_Block haben wir durch den Befehl createSprite erzeugt, mit Angaben wo dieser erscheinen soll, und mit dem Befehl New_game_block.setAnimation haben wir ihn durch eine Animation ersetzt.
 
 ```
 // New_game_block
  New_game_block = createSprite (200,285,150,50);
    New_game_block.setAnimation("new Game button.jpg_1");
 ```
</details>

<details>
  <summary> function Screen_gameover_logic</summary>
In dieser Funktion haben wir, wie bei der Pause, nur den New_Game-Button. Das heißt durch eine if-Funktion haben wir die Bedingung erschaffen, dass wenn die Maus auf den Button klickt (mousePressedOver) die Aussage Screen_changed_neu als "wahr" definiert wird. Dadurch wird in der Hauptschleife wieder das Spiel initalisiert und man kann wieder von vorne anfangen zu spieln. Wichtig hierbei ist, dass diesem nicht nur das Spiel wie sonst initalisiert wird, sonder in der Hauptschleife auch der Wert der beiden counter auf null gesetzt wird.
  Desweitern haben wir auch hier wieder einen Sound durch den Befehl playSound eingefügt.
  
```
if (mousePressedOver(New_game_block)){
      Screen_changed_neu = true;
      playSound ("https://audio.code.org/start1.mp3");
  }
``` 
</details>
<details>
<summary> function Screen_gamover_destory</summary>
  Wie auch voher haben wir auch bei diesem Zustand eine destroy-Funktion. Diese bewirkt wie immer, das die voher initialiserten Bestandteile des Screens "zerstört" werden.
  
```
  Hintergrund_gameover.destroy ;
    Text_gameover.destroy ;
    New_game_block.destroy();
}
```
</details>

  

  
  
