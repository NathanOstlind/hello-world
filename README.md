int num = 60; // size of shape 

float mx[] = new float[num]; // movement of mouse horizontally
float my[] = new float[num]; // movement of mouse vertically

void setup() { // setup things
  size(640, 360); // screen size
  noStroke(); // line of circles
  fill(255, 153); // fill of shape trail
}

void draw() { // start draw
  background(51); // background color
  
  
  int which = frameCount % num; // framecount 
  mx[which] = mouseX; // position of mouse horizontally
  my[which] = mouseY; // position of mouse vertically
  
  for (int i = 0; i < num; i++) {   // lag of the circles that follow 
    int index = (which+1 + i) % num; // circles that fallow
    ellipse(mx[index], my[index], i, i); //
  } //end for loop
} //end code 
