Project-2
=========
mkdir ~/Project-2


cd ~/Project-2



git init


touch README


git add README

git commit -m 'first commit'

git remote add origin https://github.com/username/Project-2.git

git push origin master

<!DOCTYPE HTML>
<html>
   <!-- Project 2 by Marcus Rocha
        Introduction to Programming
        Project 2 - My First Game 9/25/2013-->
    <head>
      <title>The Lone Wanderer</title>
      <style>
        body {background-color:black}
        h1 {font-weight:bold; color:red}
      </style>
      <script type="text/JavaScript">
      var score = 0;
      var visitNorth = false;
      var visitSouth = false;  
      var visitEast = false;
      var visitWest = false;
       
       function btn_directions_click(btnNum) {
            if (btnNum === 1) {
               var msg = "You have traveled North to a deserted and destroyed town.";
               updateText(msg);
               if (!visitNorth) {
                  score = score + 5;
                  visitNorth = true;
               }   
            } else {
               if (btnNum === 2) {
                 var msg = "You have traveled South to what seems to be a broken down bridge, there is no way across.";
                 updateText(msg);                  
                 if (!visitSouth) {
                    score = score + 5;
                    visitSouth = true;
                 }   
               } else {
                  if (btnNum === 3) {
                    var msg = "You have traveled East to an abandoned house. You search the house but find nothing of use.";
                    updateText(msg);
                    if (!visitEast) {
                        score = score + 5
                        visitEast = true;
                    }
                  } else {     
                    if (btnNum === 4) {
                      var msg = "You have traveled West to an empty airstrip. You start running towards an abandoned plane hoping to find keys, but you suddenly blackout.";
                      updateText(msg);
                      if (!visitWest) {
                          score = score + 5;
                          visitWest = true;
                      }   
                      
                    } else {
                    alert("What have you done... noooo.");
                      }               
                    }            
                 }  
              }
         
         scoreText();  
       } 
        
        
          
          function updateText(msg){
           var ta = document.getElementById("Project2");
           ta.value = msg + "\n" + ta.value;
          }
            function scoreText(){
            var scoreElement = document.getElementById("Score");
            scoreElement.value = score;
          }
            
      </script>
  </head>
  <body>
      <h1>The Lone Wanderer</h1> 
      <br>
      <textarea id="Project2" rows="8" cols="40">You have woken up in the middle of a barren wasteland, there seems to be a sign pointing north towards a town name.      
      </textarea>
      
      
      <br>
      <input type="button"
             value="North"
             onclick="btn_directions_click(1);">

      <input type="button"
             value="South"
             onclick="btn_directions_click(2);">
             
      <input type="button"
             value="East"
             onclick="btn_directions_click(3);">
      
      <input type="button"
             value="West"
             onclick="btn_directions_click(4);">
      <br>
      <br>
      <h1>Score</h1>
      <textarea id="Score"rows="4" cols="32"> Your score is currently 0.
      </textarea>
      
      <p class="bottom">
      <a href= mailto:"marcus.rocha1@marist.edu">E-mail Link </a>
      
  </body>
</html>