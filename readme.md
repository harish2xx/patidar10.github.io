,<!DOCTYPE html>
<html>
<head>
    <!-- <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Page Title</title>
    <meta name="viewport" content="width=device-width, initial-scale=1"> -->
    <link rel="stylesheet" type="text/css" media="screen" href="main1.css" />
         
    <style>
             body{
     background-image:url(https://images.wallpaperscraft.com/image/tropics_palm_trees_ocean_vacation_shore_96771_3840x2400.jpg);
     background-size: 1900px;
     background-repeat: no-repeat;
     font-family:sans-serif;}
     .login{
             width:350px;
             height:400px;
             transform:translate(650px,160px);
             border:none;
             background:rgba(0,0,0,.5);
             color:#fff;
             padding:80px 40px;
             margin: 20px;

           
            }
    .myform2{
              height:100px;
              width:100px;
              transform: translate(100px,-430px);
    }
    .myform{
        widows: 200px;
        height:200px;
        
        transform:translate(8px,60px);
    }
    .form{

        font-size:20px;
        color:black;

    }
    
    
    h1{
        color:#efed40;
        transform:translate(4px,30px);
        padding:0 0 20px;
    }
    .login input{
        width:100%;
        margin-bottom:20px;
        
    }
    .login input[type="text"],
    .login input[type="password"]
     {
         border:none;
         border-bottom:1px solid #fff;
         background:transparent;
         outline:none;
         height:40px;
         color:#efed40;
        font-size:20px;
     }
     ::placeholder{
         color:rgba(255,255,255,.5);
     }
    .form3
     {
         border:none;
         outline:none;
         height:50px;
         color:#fff;
         font-size:16px ;
         width:350px;
         background:#ff267e;
         border-radius:25px;

     }
     .form:hover{
                color:green;
                  }
    a{
       color:#efed40;
      font-size:20px;
       
     }
      a:hover{
              color:black;
           }
    </style>
</head>
<body>
<!--     
       <input type="text" name="hay" id="myform" placeholder="enter your name ">
          
         <button onclick="myvalidation()">click me </button>
 -->
 <div class="login">
      <h1>login here</h1>
    <form class="myform">
        <label  class="form1">username</label>
        <input class="form2" type="text" name="username" placeholder="HARISH "></br>
        
        <label class="form1">password</label>
        <input class="form6" type="password" name="password" placeholder="patidar"></br>
   
        <button class="form3"  type="submit" >login</button>
        <a href="#" >forget password</a>
    </form>
    <img class="myform2" src="https://www.iconfinder.com/icons/403019/download/png/512"/>

       
</div>  
    
</body>
</html>
