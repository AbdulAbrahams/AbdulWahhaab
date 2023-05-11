<template>
            <div class="contactsec container-lg" id="Contact">
          <h1 class="contact mb-5" style="color: White;">Contact Me</h1>
          <form action="https://formspree.io/f/xzbwjdvo" method="POST" class="form" style="padding-bottom: 7%;">
              <div class="row justify-content-center">
                <div class="col-5">
                  <input type="text" class="form-control" name="name" placeholder="First name" aria-label="First name" required>
                </div>
                <div class="col-5">
                  <input type="text" class="form-control" name="lastname" placeholder="Last name" aria-label="Last name" required>
                </div>
              </div>
              <div class="row justify-content-center">
                <div class="col-10 mb-3">
                  <label for="exampleInputEmail1" class="form-label"></label>
                  <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" name="email" placeholder="Your Email" required>
                  <div id="emailHelp" class="form-text"></div>
                </div>
            
                <div class="col-10 mb-3">
                  <label for="exampleFormControlTextarea1" class="form-label"></label>
                  <textarea class="form-control" id="exampleFormControlTextarea1" rows="5" name="message" placeholder="Enter Message Here" required></textarea>
                </div>
              </div>
              
              <button type="submit" class="btn subButton" name="submit">Submit</button>
            </form>
    
            <div class="deats justify-content-around">
              <text class="my-3" ><i class="fa fa-phone"></i> +27 83 400 4653</text>
            <text class="my-3"><i class="fa fa-envelope"></i> abdulabrahams2002@gmail.com</text>
            </div>
            
        </div>
                      
    </template>
    
    <script>
    export default{
      name: 'Contact',
      
        methods: {
          scrollTop() {
            document.body.scrollTop = document.documentElement.scrollTop = 0;
          }
        }
      }
    </script>
    
    <style scoped>

    form input{
      border-radius: 0px;
    }

    form textarea{
      border-radius: 0px;
    }
    
    .contactsec{
      min-height: 100vh;
    }
    .form-control{
        border: 2px solid rgb(255, 255, 255);
        background: rgb(0, 0, 0);
        color: rgb(255, 255, 255);
    }
    .subButton{
        font-size: 18px;
        width: 40%;
        border: 2px solid rgb(255, 255, 255);
        color: rgb(255, 255, 255);
        border-radius: 0px;
    }
    .subButton:hover{
      border: 2px solid rgb(255, 255, 255);
      background-color: rgb(255, 255, 255);
      color: rgb(0, 0, 0);
      border-radius: 0px;
    }
    .contact{
        text-align: left;
        mix-blend-mode: difference;
        font-size: clamp(3.4rem, 5vw, 6.5rem);
    }
    .deats{
      display: flex;
    }

    @media screen and (width <600px){
        .contact{
            margin-top: 20%;
        }
        .contact form{
          margin-top: 10%;
        }
        .deats{
          flex-direction: column;
        }
    }
    </style>