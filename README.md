# JAVA-2
/*
Your name: Elias Han

Date: 9/28/18

Project/assignment name: Java Sketch

Description: A sketch

Credits for code referenced:
https://processing.org/tutorials/color/
https://processing.org/tutorials/pshape/
https://processing.org/reference/mousePressed.html
https://processing.org/tutorials/transform2d/
https://processing.org/examples/rotate.html

Notes: Uses Pshape, rotate, ellipse, draw, color, mousepressed
*/

PShape ellipse;

void setup() {  //sets up our shape
  size(800,400,P2D);
  ellipseMode(CORNER);
 ellipse = createShape(ELLIPSE,-100,-50,100,50);
  ellipse.setStroke(color(0,0,255));
 ellipse.setStrokeWeight(4);
  ellipse.setFill(color(255,0,255));
}

void draw() {  //sets up mouse movement correlation to shape
  background(25,255,255);
  translate(mouseX, mouseY);
  shape(ellipse);
}
void mousePressed() {
  ellipse.rotate(HALF_PI);  //rotates the object 90 degrees when you click the mouse
}
