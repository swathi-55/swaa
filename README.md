# swaa
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>WEBSITE</title>
  <!-- Latest compiled and minified CSS -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css"
    integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

  <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
    integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
    crossorigin="anonymous"></script>
    <link href="https://fonts.googleapis.com/css?family=Yatra+One&display=swap" rel="stylesheet">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"
    integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1"
    crossorigin="anonymous"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"
    integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM"
    crossorigin="anonymous"></script>


</head>
<style>
    body{
      background: url(pup.jpg) no-repeat center fixed; 
  background-size: cover;
    }
    * {
   
    margin: 0;
    padding: 0;
  }

  .navbar-brand{
    font-family: Yatra One, cursive;
    font-size:32px;
} 
a.active{
font-size: 17px;
color:#cecbdc;
}

nav{
    font-size: 14px;
    font-weight: 400px;
    line-height: 22.4px;
   
    }
    
a{  
    color: rgb(249, 242, 242)
    }
a:hover{
    color: #9f90e3;
    }
#addPet, #login{
    margin-right:10px 
}
.hvr-grow {
    display: inline-block;
    vertical-align: middle;
    transform: translateZ(0);
    box-shadow: 0 0 1px rgba(0, 0, 0, 0);
    backface-visibility: hidden;
    -moz-osx-font-smoothing: grayscale;
    transition-duration: 0.3s;
    transition-property: transform;
    }
    
.hvr-grow:hover,
.hvr-grow:focus,
.hvr-grow:active {
    transform: scale(1.1);
    }

#dogBreed:hover, #catBreed:hover{
background-color: lightgray;
}

footer{
    background-color: #231942;
    font-size:15px;
    position: relative;
    bottom: 0%;
    width: 100%;
    height: 50px;
    color: white;
    padding: 10px
}
*{
    box-sizing: border-box;
    color: white
  }
  
 .bg{
    background-image: linear-gradient( 
      rgba(0, 0, 0, 0.3),
      rgba(0, 0, 0, 0.3)
    ),
    
     
  }
  sup{
    color: red
  }
  .form-container{
    margin: 60px auto 20px auto;
    padding: 20px;
    width: 400px; 
    background: rgba(0, 0, 0, 0.5);
    border-radius: 10px;    
  }
  #btn{
      color:white;
      background-color: #231942;
      border-radius: 5px
  }
  
p{
   text-align: center;
   margin-top: 10px
}
@media screen and (max-width: 500px){
    .form-container{
        width: 100%
    }
} 
img{
  border-radius: 50%;
}
.hero-text {
  text-align: right;
  position:absolute;
  top: 30%;
 right: 50%;
 
  color: white;
  float: right;
}
li{
  text-align: top-left;
  color: floralwhite;
  font-size: 30px;
}
 
</style>
<body>
  <div class="hero-image">
    <div class="hero-text">
      <h1 style="font-size:50px">“LOVE BETWEEN PETS AND THIER PEOPLE IS SOMETHING  FELT”</h1>
      
     
    </div>
  </div>
  <nav class="navbar navbar-expand-lg navbar-expand-sm fixed-top">
   <a class="navbar-brand" href="/">Pet Adaptation</a>
   <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
     aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
     <span class="navbar-toggler-icon" ><i class="fa fa-caret-down text-light" style="font-size:25px;" aria-hidden="true"></i></span>
   </button>
   <div class="collapse navbar-collapse" id="navbarSupportedContent">
     <ul class="navbar-nav ml-auto">
       <li class="nav-items mr-1">
         <a class="nav-link {{#isActive title 'Dogs'}} active {{/isActive}}" href="/alldogs">Dogs</a>
       </li>
       <li class="nav-item mr-1">
         <a class="nav-link {{#isActive title 'Cats'}} active {{/isActive}}" href="/allcats">Cats</a>
       </li>
       
     
       
       <li class="nav-item dropdown mr-1">
         <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" data-toggle="dropdown"
           aria-haspopup="true" aria-expanded="false">
           Breeds
         </a>
         <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
           <a class="dropdown-item" id="dogBreed" href="/dogs">Dog Breeds</a>
           <a class="dropdown-item" id="catBreed" href="/cats">Cat Breeds</a>
         </div>
       </li>
       
       </ul>
       <ul class="navbar-nav ml-auto">
       <li class="nav-item">
         <a id="addPet" class="btn btn-outline-light hvr-grow" {{#isActive title 'Add Pets'}} active {{/isActive}} href="/pets/addpet/">Add Pets</a>
       </li>
       <li class="nav-item">
         <a href="/login{{#if loggedin}}/logout{{/if}}" id="login" class="btn btn-outline-light hvr-grow">
           
         </a>
       </li>
        <li class="nav-item">
       <a href="/login/logout" id="logout" class="btn btn-outline-light hvr-grow">Logout </a>
     </li> 
      
       <li class="nav-item">
         <button type="button" id="signup" class="btn btn-outline-light hvr-grow" href="/signup">Login</button>
       </li>
       
     </ul>
   </div>
 </nav>
 <div class="container-fluid bg">
      
    <div class="row justify-content-center">
        <div class="col-xs-12 col-sm-6 col-md-3">
            <form class="form-container" action="/signup" method="POST">
                
                <hr/>
                <br><h4 class="text-center"> Signup</h4>
                <div class="alert alert-warning" role="alert">
Username or email already exist
</div>
                
              <div class="form-group">
                
                <label for="firstname">Firstname <sup>*</sup></label>
                <input type="text" class="form-control" name="firstname" id="firstname"  placeholder="Firstname" required>
                <span class="error_form" id="fname_error_message"></span>
              </div>
              <div class="form-group">
                <label for="lastname">Lastname <sup>*</sup></label>
                <input type="text" class="form-control" name="lastname" id="lastname"  placeholder="lastname" required>
                <span class="error_form" id="lname_error_message"></span>
              </div>
              <div class="form-group">
                <label for="email">Email <sup>*</sup></label>
                <input type="email" class="form-control" name="email" id="email"  placeholder="Email" required>
                <span class="error_form" id="email_error_message"></span>
              </div>
              <div class="form-group">
                <label for="username">Username <sup>*</sup></label>
                <input type="text" class="form-control" id="username" name="username" placeholder="Username" required>
                <span class="error_form" id="uname_error_message"></span>
              </div>
              <div class="form-group">
                <label for="password">Password <sup>*</sup></label>
                <input type="password" class="form-control" id="password" name="password" placeholder="Password" required>
                <span class="error_form" id="password_error_message"></span>
                </div>
                <button type="submit" id="btn"class=" btn form-control">Submit</button>
                <p id="signup-link">Already have an account? <a style="color:white; text-decoration:underline" id="signupLink" href="/login">Login</a> here</p>
              </form>
              
        </div>
    </div>
</div>

            
        </div>
    </div>
</div>

</div>
</footer>
<h1 style="color: aliceblue;" >BENIFITS OF ADOPTING A PET</h1>
<pre >
  <li >You Are Saving a Life</li>
  <li>Teaches Empathy & Awareness</li>
  <li>Unconditional love</li>
  <img src="sold.webp" alt="" style="position: left;">
</pre>
<pre>
  <li>You Are a Hero</li>
  <li>Improved Cardiovascular Health</li>
  <li>Lower Rates of Depression</li>
  <img src="girl.webp" alt="">
</pre>
<div class="footer-elem">
  <p>
      <span class="follow-us">You can follow us on</span>
      <a href="#"><ion-icon name="logo-instagram"></ion-icon></a>
      <a href="#"><ion-icon name="logo-twitter"></ion-icon></a>
      <a href="#"><ion-icon name="logo-facebook"></ion-icon></a>
  </p>
</div>

<div class="copyright">
  <p>&copy; 2023 WebPage. All rights reserved.</p>
</div>
<script src="https://unpkg.com/ionicons@5.4.0/dist/ionicons.js"></script>


  <script src="https://code.jquery.com/jquery-3.4.1.min.js"
    integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"
    integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q"
    crossorigin="anonymous"></script>

  
  <script src='https://kit.fontawesome.com/a076d05399.js'></script>
  <link href='https://fonts.googleapis.com/css?family=Cookie' rel='stylesheet'>
  <script src='{{script}}'></script>
    <script>
      
var express=require("express");
var router=express.Router();
router.get("/",function(req,res){
    res.render("signup",{
        layout: false,
        title: 'Signup',
        script: '/signupPage.js'
    });
});
router.post('/', function(req, res){
  var db = req.app.locals.db;
  var md5 = req.app.locals.md5;
  var newUser = {
    firstname: req.body.firstname,
    lastname: req.body.lastname,
    email: req.body.email,
    username: req.body.username,
    password: md5(req.body.password),
    petAdded:[],
    petLiked:[],
    requestedPet:[]
  };
  db.collection('userInfo').find({}).toArray(function(error,result){
    var flag = false;
    if(error) throw error
    for(var i=0; i<result.length; i++){
      if(req.body.username == result[i].username || req.body.email == result[i].email){
        flag = true
        res.render("signup",{
          layout: false,
          title: 'Signup',
          script: '/signupPage.js',
          msg: 'Username or email already exists'
      });
      }
    }
    if(! flag){
      db.collection('userInfo').insertOne(newUser, function(err, result){
        if (err) throw err;
        console.log(result);
        res.redirect('/login');
      });
    }
  })
});
module.exports=router; 
    </script>
</body>
</html>
