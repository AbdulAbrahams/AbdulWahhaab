<template>
<div class="navigation fixed-top">
    <header class="container d-flex flex-wrap justify-content-center">
      <a href="#" class="d-flex align-items-center mx-5 mb-md-0 me-md-auto text-dark text-decoration-none">
        <span class="title fs-4 text-white"><img class="logo" src="https://i.postimg.cc/JzKGzHsT/Screenshot-2024-05-09-120515.png" alt=""></span>
      </a>

      <ul class="navbar nav nav-pills mx-5">
        <li class="nav-item"><a href="#" class="nav-link">Home</a></li>
        <li class="nav-item"><a href="#about" class="nav-link">About</a></li>
        <li class="nav-item"><a href="#resume" class="nav-link">Resume</a></li>
        <li class="nav-item"><a href="#testimonials" class="nav-link">Testimonials</a></li>
        <li class="nav-item"><a href="#projects" class="nav-link">Projects</a></li>
        <li class="nav-item"><a href="#contact" class="nav-link">Contact</a></li>
      </ul>
    </header>
  </div>

  <nav class="navigation2 navbar navbar-dark bg-black fixed-top">
  <div class="container-fluid">
    <a class="navbar-brand" href="#"><img class="logo" src="https://i.postimg.cc/JzKGzHsT/Screenshot-2024-05-09-120515.png" alt=""></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
      <div class="offcanvas-header">
        <img class="logo offcanvas-title" id="offcanvasNavbarLabel" src="https://i.postimg.cc/G2CHvHrv/AW.png" alt="">
        <button type="button" class="btn-close py-2 px-2 text-reset bg-white mx-4" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body">
        <ul class="navbar-nav flex-grow-1 pe-3">
          <li class="nav-item">
            <a class="nav-link my-2" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link my-2" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link my-2" href="#resume">Resume</a>
          </li>
          <li class="nav-item">
            <a class="nav-link my-2" href="#testimonials">Testimonials</a>
          </li>
          <li class="nav-item">
            <a class="nav-link my-2" href="#projects">Projects</a>
          </li>
          <li class="nav-item">
            <a class="nav-link my-2" href="#contact">Contact</a>
          </li>
        </ul>
      </div>
      <div class="offcanvas-footer">
        <div class="footer-bar mx-3 my-3">
              <a href="https://www.youtube.com/@AbnormalAbdul12"><i class="fa fa-youtube-play"></i></a>
              <a href="https://www.instagram.com/abdul_abrahams_/"><i class="fa fa-instagram mx-2"></i></a> 
              <a href="https://www.linkedin.com/in/abdul-wahhaab-abrahams-506142222/"><i class="fa fa-linkedin"></i></a> 
              <a href="https://github.com/AbdulAbrahams"><i class="fa fa-github mx-2"></i></a>
        </div>
      </div>
    </div>
  </div>
</nav>
</template>

<script>
    export default {
        name: 'Navbar',
    }
</script>

<style  scoped>

.logo{
  background-color: white;
  width: 80px;
  height: 40px;
}

.title{
  font-weight: 600;
}

.navigation{
  background: black;
  color: white;
}

.navigation.black{
  background: rgb(0, 0, 0);
}
.nav-link {
  color: white;
}

.nav-link:hover{
  opacity: 80%;
}

.navbar-dark .navbar-nav .nav-link {
  font-size: 18px;
    color: rgba(255,255,255);
}

.navbar-dark .navbar-nav .nav-link:hover {
    color: rgba(255, 255, 255, 0.468);
}
.navigation2{
  display: none;
}

.offcanvas{
  text-align: left;
  background: black;
  opacity: 90%;
  max-width: 70vw;
}
.footer-bar a{
  font-size: 25px;
  margin: 3px;
}
.footer-bar a i{
    color: rgb(255, 255, 255) !important;
}
.footer-bar a i:hover{
    color: rgba(255, 255, 255, 0.721) !important;
}

@media screen and (width < 1000px) {
.navigation{
  display: none;
}

.navigation2{
  display: block;
}

.nav-link:hover{
  opacity: 80%;
}
}
</style>
