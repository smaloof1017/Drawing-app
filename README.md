var character1 = function(x, y, height){
 
    
//hair
triangle(x + 178*height/1,y + 76*height/1,x + 178*height/1,y + 1*height/1,x + 115*height/1,y + 111*height/1);
triangle(x + 178*height/1,y + 76*height/1,x + 178*height/1,y + 0*height/1,x + 256*height/1,y + 111*height/1 );

//head
ellipse(x + 188*height/1,y + 176*height/1,211*height/1,209*height/1);

//eyes
ellipse(x + 227*height/1,y + 137*height/1,53*height/1,29*height/1);
ellipse(x + 146*height/1,y + 138*height/1,53*height/1,29*height/1);

//glasses
line(x + 120*height/1,y + 138*height/1,x + 91*height/1,y + 134 *height/1);
line(x + 200*height/1,y + 134*height/1,x + 171*height/1,y + 134 *height/1);
line(x + 284*height/1,y + 132*height/1,x + 253*height/1,y + 138*height/1);

//mouth
arc(x + 187 *height/1,y + 193 *height/1,111*height/1,100*height/1,4,175);
line(x + 243*height/1,y + 197*height/1,x + 132*height/1,y + 198*height/1);
rect(x + 149*height/1,y + 197*height/1,13*height/1,15*height/1);
rect(x + 162*height/1,y + 197*height/1,13*height/1,15*height/1);
rect(x + 197*height/1,y + 197*height/1,13*height/1,15*height/1);
rect(x + 210*height/1,y + 197*height/1,13*height/1,15*height/1);
rect(x + 223*height/1,y + 197*height/1,13*height/1,15*height/1);
rect(x + 136*height/1,y + 197*height/1,13*height/1,15*height/1);
rect(x + 179*height/1,y + 227*height/1,13*height/1,15*height/1);

//nose
bezier(x + 186*height/1,y + 162*height/1,x + 193*height/1,y + 98*height/1,x + 116*height/1,y + 253*height/1,x + 211*height/1,y + 159*height/1);

};//puts character in scene1


//sets current scene
var currentScence = 0;
var currentColor = null;//set what color to paint with
var randomColor = (color(round(random(0,255)), round(random(0,255)),(round(random(0,255)))));//makes color random

//draws bitmoji
var drawHead = function(bitmojiX,bitmojiY,bitmojiHeight){
    
    // hat part 1
    fill(76, 203, 232);
    arc(bitmojiX+(bitmojiHeight/150*-1),bitmojiY+(bitmojiHeight/150*-2),bitmojiHeight/150*77,bitmojiHeight/150*62,177,886);
    //hair
    fill(69, 31, 31);
    rect(bitmojiX-(bitmojiHeight/150*42),bitmojiY+(bitmojiHeight/150*11),bitmojiHeight/150*80,bitmojiHeight/150*29);
    //left ears
    fill(255, 219, 172);
    ellipse(bitmojiX-(bitmojiHeight/150*36),bitmojiY+(bitmojiHeight/150*46),bitmojiHeight/150*20,bitmojiHeight/150*20);
    //right ear
    fill(255, 219, 172);
    ellipse(bitmojiX+(bitmojiHeight/150*33),bitmojiY+(bitmojiHeight/150*46),bitmojiHeight/150*20,bitmojiHeight/150*20);
    //face
    fill(255, 219, 172);
    ellipse(bitmojiX-(bitmojiHeight/150*2),bitmojiY+(bitmojiHeight/150*46),bitmojiHeight/150*72,bitmojiHeight/150*80);
    //hat part 2
    fill(230, 14, 39);
    rect(bitmojiX-(bitmojiHeight/150*73),bitmojiY-(bitmojiHeight/150*0),bitmojiHeight/150*113,bitmojiHeight/150*15);
    //left eyes 1
    fill(2554, 255, 255);
    ellipse(bitmojiX-(bitmojiHeight/150*19),bitmojiY+(bitmojiHeight/150*29),bitmojiHeight/150*21,bitmojiHeight/150*22);
    //right eyes 2
    fill(255, 255, 255);
    ellipse(bitmojiX+(bitmojiHeight/150*10),bitmojiY+(bitmojiHeight/150*30),bitmojiHeight/150*21,bitmojiHeight/150*22);
    //left eys puplis
    fill(66, 30, 30);
    ellipse(bitmojiX-(bitmojiHeight/150*19),bitmojiY+(bitmojiHeight/150*30),bitmojiHeight/150*7,bitmojiHeight/150*7);
    //right eye puplis
    fill(66, 30, 30);
    ellipse(bitmojiX+(bitmojiHeight/150*11),bitmojiY+(bitmojiHeight/150*30),bitmojiHeight/150*7,bitmojiHeight/150*7);
};
var drawBody = function (bitmojiX,bitmojiY,bitmojiHeight){
   
    //mouth line
    line(bitmojiX-(bitmojiHeight/150*23),bitmojiY+(bitmojiHeight/150*57),bitmojiX+(bitmojiHeight/150*17),bitmojiY+(bitmojiHeight/150*58));
    fill(238, 237, 242);
    //mouth
    fill(255, 255, 255);
    arc(bitmojiX-(bitmojiHeight/150 *3),bitmojiY+(bitmojiHeight/150*59),bitmojiHeight/150*42,bitmojiHeight/150*30,2,182);
    //neck
    fill(255, 219, 172);
    rect(bitmojiX-(bitmojiHeight/150*20),bitmojiY+(bitmojiHeight/150*81),bitmojiHeight/150 *36,bitmojiHeight/150*31);
    //shirt
    fill(25, 46, 232);
    rect(bitmojiX-(bitmojiHeight/150 *41),bitmojiY+(bitmojiHeight/150*86),bitmojiHeight/150*82,bitmojiHeight/150*33);
    var myname=("AM");
    textSize(bitmojiHeight/150*30);
    fill(255, 255, 255);
    text(myname,bitmojiX-(bitmojiHeight/150*21),bitmojiY+(bitmojiHeight/150*87));
};
var drawBitmoji2 = function(bitmojiX,bitmojiY,bitmojiHeight){
    drawHead(bitmojiX,bitmojiY,bitmojiHeight);
    drawBody(bitmojiX,bitmojiY,bitmojiHeight);
};
var drawBitmojiHead = function(x,y,emojiHeight){
        noStroke();
    //shirt
    fill(8, 8, 8);
    quad(x + 154*emojiHeight/1,y + 323*emojiHeight/1,x + 261*emojiHeight/1,y + 318*emojiHeight/1,x + 239*emojiHeight/1,y + 260*emojiHeight/1,x + 113*emojiHeight/1,y + 268*emojiHeight/1);
    //face
    fill(230, 192, 115);
    ellipse( x + 200*emojiHeight/1, y + 200*emojiHeight/1, 135*emojiHeight/1, 150*emojiHeight/1);
    //jawline
    fill(255, 255, 255);
    arc(x + 125*emojiHeight/1,y + 305*emojiHeight/1,100*emojiHeight/1,163*emojiHeight/1,0,361);//left chisel
    arc(x + 275*emojiHeight/1,y + 305*emojiHeight/1,100*emojiHeight/1,163*emojiHeight/1,0,361);//rigth chisel
     //glasses
    stroke(0, 0, 0);
    fill(230,192,115);
    ellipse(x + 175*emojiHeight/1,y + 177*emojiHeight/1,25*emojiHeight/1,25*emojiHeight/1);//left lens
    ellipse(x + 225*emojiHeight/1,y + 177*emojiHeight/1,25*emojiHeight/1,25*emojiHeight/1);//right lens
    line(x + 137*emojiHeight/1,y + 172*emojiHeight/1,x + 163*emojiHeight/1,y + 175*emojiHeight/1);//left g
    line(x + 212*emojiHeight/1,y + 177*emojiHeight/1,x + 187*emojiHeight/1,y + 177*emojiHeight/1);//middle g
    line(x + 263*emojiHeight/1,y + 172*emojiHeight/1,x + 237*emojiHeight/1,y + 175*emojiHeight/1);//right g
    //nose
    bezier(x + 208*emojiHeight/1,y + 207*emojiHeight/1,x+ 187*emojiHeight/1,y + 205*emojiHeight/1,x + 177*emojiHeight/1,y + 216*emojiHeight/1,x + 200*emojiHeight/1,y + 189*emojiHeight/1);//nose
    //mouth
    fill(222, 49, 98);
    bezier(x + 216*emojiHeight/1,y + 233*emojiHeight/1,x + 235*emojiHeight/1,y + 259*emojiHeight/1,x + 180*emojiHeight/1,y + 284*emojiHeight/1,x + 190*emojiHeight/1,y + 233*emojiHeight/1);
    fill(5, 5, 5);
    line(x + 215*emojiHeight/1,y + 232*emojiHeight/1,x + 184*emojiHeight/1,y + 232*emojiHeight/1);
    line(x + 202*emojiHeight/1,y + 255*emojiHeight/1,x + 202*emojiHeight/1,y + 237*emojiHeight/1);
   
    noStroke();
    fill(252, 249, 249);
    ellipse(x + 175*emojiHeight/1,y + 177*emojiHeight/1,17*emojiHeight/1,15*emojiHeight/1);//left eye
    ellipse(x + 225*emojiHeight/1,y + 177*emojiHeight/1,17*emojiHeight/1,8*emojiHeight/1);//right eye
   
    fill(107, 117, 219);
    ellipse(x + 225*emojiHeight/1,y + 177*emojiHeight/1,11*emojiHeight/1,3*emojiHeight/1);//right blue eye
    ellipse(x + 175*emojiHeight/1,y + 177*emojiHeight/1,10*emojiHeight/1,9*emojiHeight/1);//left blue eye
   
    fill(5, 5, 5);
    ellipse(x + 175*emojiHeight/1,y + 177*emojiHeight/1,4*emojiHeight/1,4*emojiHeight/1);//left pupil
    ellipse(x + 225*emojiHeight/1,y + 177*emojiHeight/1,4*emojiHeight/1,1*emojiHeight/1);//right pupil
   
   
   
    fill(247, 247, 247);
    arc(x + 201*emojiHeight/1,y + 163*emojiHeight/1,119*emojiHeight/1,97*emojiHeight/1,-180,0);//hat
    fill(125, 116, 11);
    arc(x + 200*emojiHeight/1,y + 156*emojiHeight/1,30*emojiHeight/1,45*emojiHeight/1,-180,0);//hat hair
   
    };
   
 var drawBitmojiBody = function(x,y,emojiHeight){
                //shirt
    fill(8, 8, 8);
    quad(x + 153*emojiHeight/1,y + 312*emojiHeight/1,x + 247*emojiHeight/1,y + 310*emojiHeight/1,x + 219*emojiHeight/1,y + 275*emojiHeight/1,x + 176*emojiHeight/1,y + 281*emojiHeight/1);
    rect(x + 153*emojiHeight/1,y + 310*emojiHeight/1,94*emojiHeight/1,95*emojiHeight/1);
   
    //shirt text
    fill(255, 0, 0);
    textSize(40*emojiHeight/1);
    text ("SM",x + 171*emojiHeight/1,y + 338*emojiHeight/1);
    };
   
    var drawBitmoji=function(x,y,emojiHeight){
        drawBitmojiHead(x,y,emojiHeight);
        drawBitmojiBody(x,y,emojiHeight);
    };
    var draw = function() {
       var drawBitmoji;
    };

    
//Khan Button code
var Button = function(config) {
    this.x = config.x || 0;
    this.y = config.y || 0;
    this.width = config.width || 150;
    this.height = config.height || 50;
    this.label = config.label || "Click";
    this.onClick = config.onClick || function() {};
};

Button.prototype.draw = function() {
    fill(255, 255, 255);
    rect(this.x+35, this.y, this.width, this.height, 5);
    fill(0, 0, 0);
    textSize(19);
    textAlign(LEFT, TOP);
    text(this.label, this.x+46, this.y+this.height/4);
};

Button.prototype.isMouseInside = function() {
    return mouseX > this.x &&
           mouseX < (this.x + this.width) &&
           mouseY > this.y &&
           mouseY < (this.y + this.height);
};

Button.prototype.handleMouseClick = function() {
    if (this.isMouseInside()) {
        this.onClick();
    }
};

// button to draw with blue color 
var colorButton1 = new Button({
    x: 271,
    y: 10,
    width: 85,
    label: "Blue" ,
    onClick: function() {
        currentColor =color(0,0,255) ;
    }           
});
// button to draws with red color
var colorButton2 = new Button({
    x: 272,
    y: 62,
    width: 83,
    label: "Red" ,
    onClick: function() {
        currentColor =color(255,0,0) ;
    }           
});
//button to draws with yellow color 
var colorButton3 = new Button({
    x: 270,
    y: 115,
    width: 85,
    label: "Yellow" ,
    onClick: function() {
        currentColor =color(255,255,0) ;
    }           
});
// button to draw with green color
var colorButton4 = new Button({
    x: 270,
    y: 168,
    width: 90,
    label: "Green" ,
    onClick: function() {
        currentColor = color(39, 207, 50) ;
    }           
});
var colorButton5 = new Button({
    x: 270,
    y: 224,
    width: 90,
    label: "Orange" ,
    onClick: function() {
        currentColor = color(237, 114, 26) ;
    }           
});
var colorButton6 = new Button({
    x: 270,
    y: 279,
    width: 90,
    label: "Purple" ,
    onClick: function() {
        currentColor = color(150, 65, 235) ;
    }           
});
var colorButton7 = new Button({
    x: -30,
    y: 270,
    width: 80,
    label: "Black" ,
    onClick: function() {
        currentColor = color(0, 0, 0) ;
    }           
});
var colorButton8 = new Button({
    x: 169,
    y: 272,
    width: 80,
    label: "White" ,
    onClick: function() {
        currentColor = color(255, 255, 255) ;
    } 
});//sets color to a random rgb value 
var colorButton9 = new Button({
    x:270,
    y:335,
    width: 90,
    label: "Random" ,
    onClick: function() {
        currentColor = randomColor ;
    } 
});// buton to go to next scene 
var nextButton = new Button ({
    x: 100,
    y: 330,
    width:122,
    label: "Next Secene",
    onClick: function() {
     currentScence = currentScence + 1;
     loop();
    }
});
//first trace game screen
var fristScence = function(){
   
   
    
    currentScence = 1;
    background(57, 176, 160);
    colorButton1.draw();
    colorButton2.draw();
    colorButton3.draw();
    colorButton4.draw();
    colorButton5.draw();
    colorButton6.draw();
    colorButton7.draw();
    colorButton8.draw();
    colorButton9.draw();
    nextButton.draw();
    fill(250, 250, 250);
    rect(0,0,286,265);
    
    //draws first character
     fill(252, 252, 252);
     stroke(0, 0, 0);
     character1(0,20,0.8);
     
    
    
};
//draw 2nd game scence
var secondScence = function(){
    


    currentScence = 2;
    background(224, 47, 224);
    colorButton1.draw();
    colorButton2.draw();
    colorButton3.draw();
    colorButton4.draw();
    colorButton5.draw();
    colorButton6.draw();
    colorButton7.draw();
    colorButton8.draw();
    colorButton9.draw();
    nextButton.draw();
    fill(255, 255, 255);
    rect(-1,-1,275,263);
    //draws flowers 
        var x =0;
     var y =0;
    var fheight=1;
//circle flower
//leaf
var flower = function(x,y,fheight){
arc(x + 118*fheight/1,y + 341*fheight/1,205*fheight/1,13*fheight/1,112,248);
//stem
rect(x + 80*fheight/1,y + 203*fheight/1,13*fheight/1,162*fheight/1);
//flower bud
ellipse(x + 87*fheight/1,y + 219*fheight/1,77*fheight/1,75*fheight/1);
//petals
arc(x + 50*fheight/1,y + 204*fheight/1,33*fheight/1,33*fheight/1,100,305);
arc(x + 72*fheight/1,y + 183*fheight/1,33*fheight/1,33*fheight/1,146,352);
arc(x + 105*fheight/1,y + 183*fheight/1,33*fheight/1,33*fheight/1,187,401);
arc(x + 126*fheight/1,y + 206*fheight/1,33*fheight/1,33*fheight/1,232,452);
arc(x + 125*fheight/1,y + 238*fheight/1,33*fheight/1,33*fheight/1,272,499);
arc(x + 110*fheight/1,y + 261*fheight/1,33*fheight/1,19*fheight/1,303,556);
arc(x + 53*fheight/1,y + 236*fheight/1,33*fheight/1,33*fheight/1,417,604);
arc(x + 68*fheight/1,y + 261*fheight/1,26*fheight/1,23*fheight/1,339,598);


//triangle flower
//stem
rect(x + 224*fheight/1,y + 193*fheight/1,13*fheight/1,171*fheight/1);
//flower
arc(x + 231*fheight/1,y + 119*fheight/1,65*fheight/1,152*fheight/1,-2,183);
arc(x + 231*fheight/1,y + 90*fheight/1,69*fheight/1,144*fheight/1,-2,183);
triangle(x + 210*fheight/1,y + 64*fheight/1,x + 226*fheight/1,y + 87*fheight/1,x + 196*fheight/1,y + 87*fheight/1);
triangle(x + 233*fheight/1,y + 64*fheight/1,x + 247*fheight/1,y + 87*fheight/1,x + 215*fheight/1,y + 87*fheight/1);
triangle(x + 256*fheight/1,y + 64*fheight/1,x + 266*fheight/1,y + 87*fheight/1,x + 237*fheight/1,y + 87*fheight/1);
//leaf
arc(x + 248*fheight/1,y + 265*fheight/1,107*fheight/1,12*fheight/1,-101,100);


//sun
ellipse(x + 30*fheight/1,y + 34*fheight/1,177*fheight/1,177*fheight/1);
};

stroke(8, 8, 8);
flower(28,7,0.7);
    
};
//draw 3rd game scence
var thridScence = function(){
    currentScence = 3;
    background(224, 47, 109);
    colorButton1.draw();
    colorButton2.draw();
    colorButton3.draw();
    colorButton4.draw();
    colorButton5.draw();
    colorButton6.draw();
    colorButton7.draw();
    colorButton8.draw();
    colorButton9.draw();
    nextButton.draw();
    fill(255, 255, 255);
    rect(1,5,280,257);
//draws baby character     
var x  = 0; 
var y = 0;
var bheight= 1;

var baby= function(x,y,bheight){

//head
ellipse(x + 189*bheight/1,y + 168*bheight/1,213*bheight/1,278*bheight/1);
//eyes
ellipse(x + 153*bheight/1,y + 106*bheight/1,35*bheight/1,23*bheight/1);
ellipse(x + 224*bheight/1,y + 106*bheight/1,35*bheight/1,23*bheight/1);
//pupils
ellipse(x + 153*bheight/1,y + 106*bheight/1,18*bheight/1,20*bheight/1);
ellipse(x + 224*bheight/1,y + 106*bheight/1,18*bheight/1,20*bheight/1);
fill(0, 0, 0);
ellipse(x + 224*bheight/1,y + 106*bheight/1,5*bheight/1,9*bheight/1);
ellipse(x + 153*bheight/1,y + 106*bheight/1,5*bheight/1,9*bheight/1);
noFill();
fill(255, 255, 255);

//smile
arc(x + 190*bheight/1,y + 193*bheight/1,131*bheight/1,97*bheight/1,-21,163);
line(x + 251*bheight/1,y + 175*bheight/1,x + 126*bheight/1,y + 207*bheight/1);

//bowtie
quad(x + 57*bheight/1,y + 32*bheight/1,x + 89*bheight/1,y + 97*bheight/1,x + 168*bheight/1,y + 4*bheight/1,x + 181*bheight/1,y + 75*bheight/1);

//teeth
line(x + 189*bheight/1,y + 191*bheight/1,x + 196*bheight/1,y + 212*bheight/1);
line(x + 172*bheight/1,y + 195*bheight/1,x + 179*bheight/1,y + 217*bheight/1);
line(x + 196*bheight/1,y + 212*bheight/1,x + 178*bheight/1,y + 217*bheight/1);

//nose
fill(255, 255, 255);
bezier(x + 195*bheight/1,y +  171*bheight/1, x + 349*bheight/1, y + 194*bheight/1, x + 458*bheight/1, y + 130*bheight/1, x + 196*bheight/1, y + 147*bheight/1);

//hair
noFill();
arc(x + 243*bheight/1,y +  31*bheight/1, 43*bheight/1, 35*bheight/1, -196, -25);
arc(x + 277*bheight/1,y +  23*bheight/1, 28*bheight/1, 32*bheight/1, -372, -181);
};

baby(0,20,0.7);


};
//draw 4th game scence
var fourthScence = function(){
    currentScence = 4;
    background(34, 105, 204);
    colorButton1.draw();
    colorButton2.draw();
    colorButton3.draw();
    colorButton4.draw();
    colorButton5.draw();
    colorButton6.draw();
    colorButton7.draw();
    colorButton8.draw();
    colorButton9.draw();
    nextButton.draw();
    fill(255, 255, 255);
    rect(0,0,285,257);
   //draws space scene 
    var x = 0;
var y = 0;
var heightS= 1;

var space = function(x, y , heightS){
    
    var star = function(x,y,heightS){
    
triangle(x + 100*heightS/1,y + 200*heightS/1,x + 200*heightS/1,y + 400*heightS/1,x + 300*heightS/1,y + 200*heightS/1);
triangle(x + 200*heightS/1,y + 145*heightS/1,x + 115*heightS/1,y + 341*heightS/1,x + 301*heightS/1,y + 340*heightS/1);

};
    
star(x + 48*heightS/1,y + 67*heightS/1,0.1*heightS/1);
star(x + 144*heightS/1,y + 145*heightS/1,0.1*heightS/1);
star(x + 37*heightS/1,y + 200*heightS/1,0.1*heightS/1);
star(x + 140*heightS/1,y + 21*heightS/1,0.1*heightS/1);
star(x + 294*heightS/1,y + 333*heightS/1,0.1*heightS/1);
star(x + 103*heightS/1,y + 293*heightS/1,0.1*heightS/1);
star(x + 222*heightS/1,y + 248*heightS/1,0.1*heightS/1);
star(x + 178*heightS/1,y + 323*heightS/1,0.1*heightS/1);


noFill();
//asterioid
arc(x + 466*heightS/1,y + 71*heightS/1,536*heightS/1,349*heightS/1,90,150);
arc(x + 472*heightS/1,y + 71*heightS/1,518*heightS/1,289*heightS/1,92,148);
ellipse(x + 232*heightS/1,y + 134*heightS/1,50*heightS/1,50*heightS/1);

fill(255, 255, 255);
arc(x + 213*heightS/1, y + 115*heightS/1, 20*heightS/1, 20*heightS/1, -27, 120);
arc(x + 257*heightS/1, y + 120*heightS/1, 20*heightS/1, 20*heightS/1, 91, 205);
ellipse(x + 233*heightS/1,y + 142*heightS/1,10*heightS/1,13*heightS/1);
line(x + 232*heightS/1,y + 160*heightS/1,x + 369*heightS/1,y + 291*heightS/1);
line(x + 255*heightS/1,y + 147*heightS/1,x + 373*heightS/1,y + 191*heightS/1);
noFill();

//moon
ellipse(x + 375*heightS/1,y + 67*heightS/1,209*heightS/1,200*heightS/1);

//rocket
rect(x + 95*heightS/1,y + 112*heightS/1,22*heightS/1,161*heightS/1);
triangle(x + 95*heightS/1,y + 113*heightS/1,x + 106*heightS/1,y + 47*heightS/1,x + 118*heightS/1,y + 113*heightS/1);
triangle(x + 143*heightS/1,y + 273*heightS/1,x + 118*heightS/1,y + 273*heightS/1,x + 118*heightS/1 ,y + 186*heightS/1);

triangle(x + 70*heightS/1,y + 273*heightS/1,x + 95*heightS/1,y + 185*heightS/1,x + 95*heightS/1,y + 273*heightS/1);
};

space(-31,-5,0.65);

};

//draws 5th game scence
var fifthScence = function(){
    currentScence = 5;
    background(45, 214, 82);
    colorButton1.draw();
    colorButton2.draw();
    colorButton3.draw();
    colorButton4.draw();
    colorButton5.draw();
    colorButton6.draw();
    colorButton7.draw();
    colorButton8.draw();
    colorButton9.draw();
    nextButton.draw();
    fill(255, 255, 255);
    rect(1,5,280,257);
    //draws character super winston
    var superWinston = function(faceX, faceY) {

//fill(133, 30, 189);
//face
ellipse(faceX, faceY ,138 ,146);
//fill(26, 23, 23);
//left eye
ellipse(faceX-18, faceY+-31 ,40 ,40);
//fill(255, 255, 255);
//left puplie
ellipse(faceX-14,faceY-30,25,25);
//fill(31, 28, 31);
//righteye
ellipse(faceX+36, faceY-30 ,40 ,40);
//fill(255, 255, 255);
// right puple 
ellipse(faceX+32,faceY-30,25,25);
//fill(255, 0, 0);
//mouth
arc(faceX+10, faceY+1, 75, 117, 360,537);
line(123,121,190,117);
};
    superWinston(142,117);
};

//end scene 
var endScence= function(){
    currentScence = 6;
    background(164, 206, 245);
    textSize(30);
    text('The End',133,136);
};//start button 
var startButton = new Button({
    x: 100,
    y: 268,
    width: 100,
    label: "    Start" ,
    onClick: function() {
      currentScence = 0;
        fristScence();       
    }
});//start screen
 var startScence = function(){
    currentScence = 0;
    background(64, 230, 55);
    textSize(30);
    text("Painting Program", 75,29);
    text( "by",175,61);
    text(" Andrew Marquez", 75,93);
    text(" & Steven Maloof",83,133);
    text("Click and Drag to Paint \n     on the Canvas",45,170);
    startButton.draw();
    drawBitmoji(-16,182,0.35);
    drawBitmoji2(317,243,103);
 
};

     
var draw= function() {
    if(currentScence ===0){
        startScence();
    }
   else if(currentScence === 1)
   {
}
   else if(currentScence === 2)
   {
      secondScence(); 
      noLoop();
   }
   else if(currentScence === 3)
   {  
       thridScence();
        noLoop();
   }
   else if(currentScence === 4)
   { 
       fourthScence();
        noLoop();
   }
   else if(currentScence === 5)
   { 
       fifthScence();
           noLoop();
    }
    else if (currentScence === 6){
        endScence();
              noLoop();
    }

   
};
//makes mouse drag color scene 
mouseDragged = function(){
       fill(currentColor);
       noStroke();
       ellipse(mouseX,mouseY,20,20);
};

// mouseClick function
mouseClicked = function() {
    startButton.handleMouseClick();
    colorButton1.handleMouseClick();
    colorButton2.handleMouseClick();
    colorButton3.handleMouseClick();
    colorButton4.handleMouseClick();
    colorButton5.handleMouseClick();
    colorButton6.handleMouseClick();
    colorButton7.handleMouseClick();
    colorButton8.handleMouseClick();
    colorButton9.handleMouseClick();
    nextButton.handleMouseClick();
};
