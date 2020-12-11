# Event-delegation-changing-color-button-
adding one addEventListener to the parent instead of adding addEventListener individually to the children
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Event3-skill-learning</title> 
    <style>
      div {
          display: inline-block;
          width: 250px;
          height:30px;
          padding: 40px;
          background-color:powderblue;
          border-radius: 10px;
        } 
        div button {
          border-radius: 8px;
          font-size: 16px;  

        }
    </style>   
  </head>
  <body>
    <div id="button-bar">
      <button class="pink">pink</button>
      <button class="gray">gray</button>
      <button class="green">green</button>
      <button class="black">black</button>    
    </div>

    <script>
        const div = document.querySelector('#button-bar');
        const btn = document.querySelector('button');

        div.addEventListener('click',function(e){
          if(e.target && e.target.matches('button.pink')){
            document.body.style.backgroundColor = 'pink';
          }else if(e.target && e.target.matches('button.gray')){
            document.body.style.backgroundColor = 'gray';  
          }else if(e.target && e.target.matches('button.green')){
            document.body.style.backgroundColor ='green';  
          }else if(e.target && e.target.matches('button.black')){
            document.body.style.backgroundColor ='black';   
          }
        });
          
    </script>    
  </body>    
</html>
