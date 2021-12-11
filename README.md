# Drawing-app
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

};//start button 
var startButton = new Button({
    x: 97,
    y: 300,
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
    text("painting program", 75,100);
    text( "by",175,133);
    text("Andrew Marquez", 75,162);
    text("Steven Maloof",83,197);
    startButton.draw();
 
};

     
var draw= function() {
    if(currentScence ===0){
        startScence();
    }

    else if (currentScence === 3){
        endScence();
    }
     if (mouseIsPressed)
    {
       fill(currentColor);
       noStroke()
       ellipse(mouseX,mouseY,20,20);
    }
   
}; 
