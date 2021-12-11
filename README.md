# Drawing-app

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
