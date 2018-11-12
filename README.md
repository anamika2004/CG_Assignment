var p1,p2;
var stars = [];

function setup() {
  createCanvas(windowWidth,windowHeight); 
  background(50);
  for (var i = 0;i < 800;i++) {
    stars.push(random(-width,width));
    stars.push(random(-height,height));
  }
}  

function draw () {

//STELLE
  
background(0, 0, 40);
  push();
  translate(width/2,height/2);
  rotate(frameCount/70);
  for (var i = 0;i<stars.length;i+=2) {
    fill(random(0, 255), random(0, 255), random(0, 255));
    noStroke();
    ellipse(stars[i],stars[i+1],dist(0,0,stars[i],stars[i+1])/150);
    if (dist(0,0,stars[i],stars[i+1])>height) {
      stars[i] = random(-500,500);
      stars[i+1] = random(-500,500);
    }
  }
  pop();

//CALZINI

if(mouseX > 300 && mouseX < 900 && mouseY > 200 && mouseY < 600){
    fill(random(0, 255), random(0, 255), random(0, 255));
    noStroke();
  }
  else{
    fill(230, 32, 106);
  }
    
noStroke();
quad(675, 415, 700, 415, 704, 455, 694, 455);
  
noStroke();
quad(650, 415, 675, 415, 672, 455, 663, 455);
  
  
//CORPO
  
noStroke();
fill(30);
bezier(650, 415, 550, 285, 800, 285, 700, 415); 

noStroke();
fill(40);
quad(635, 415, 715, 415, 700, 300, 650, 300);

noStroke();
fill(50);
quad(650, 415, 675, 415, 675, 450, 660, 450);

noStroke();
fill(50);
quad(675, 415, 700, 415, 705, 450, 690, 450);

noStroke();
fill(50);
ellipse(700, 459, 20, 10)

noStroke();
fill(50);
ellipse(667, 459, 20, 10)

//CAPELLI

noStroke();
fill(113, 59, 7);
bezier(600, 300, 550, 175, 800, 175, 750, 300);

noStroke();
fill(113, 59, 7);
ellipse(675, 200, 80, 70);

noStroke();
fill(113, 59, 7);
bezier(625, 200, 650, 230, 800, 175, 655, 300);

noStroke();
fill(113, 59, 7);
bezier(623, 205, 650, 230, 800, 175, 655, 300);
  
//TESTA  

noStroke();
fill (235, 186, 161);
ellipse (600, 300, 10, 10);
  
noStroke();
fill (235, 186, 161);
ellipse (750, 300, 10, 10);

noStroke();
fill(235, 186, 161);
bezier(600, 300, 600, 350, 750, 350, 750, 300);

noStroke();
fill(235, 186, 161);
bezier(600, 300, 600, 200, 750, 200, 750, 300);
  
//VOLTO
  
noStroke();
fill (0);
ellipse (650, 280, 10, 10);

noFill();
strokeWeight(1);
stroke(0,0,0);
bezier(644, 275, 649, 280, 648, 280, 647, 273);

noStroke();
fill (400);
ellipse (649, 279, 3, 3);


noFill();
strokeWeight(1);
stroke(0,0,0);
bezier(705, 273, 703, 280, 704, 280, 707, 275);

noStroke();
fill (0);
ellipse (700, 280, 10, 10);

noStroke();
fill (400);
ellipse (699, 279, 3, 3);

noStroke();
fill(157, 114, 92);
bezier(670, 300, 670, 305, 680, 305, 680, 300);

}
