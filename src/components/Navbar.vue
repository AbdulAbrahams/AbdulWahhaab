<template>
<div class="navigation fixed-top">
    <header class="container d-flex flex-wrap justify-content-center">
      <a href="/" class="d-flex align-items-center mx-5 mb-md-0 me-md-auto text-dark text-decoration-none">
        <span class="title fs-4 text-white">Wahhaab</span>
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
    <a class="navbar-brand" href="#">Wahhaab</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasNavbar" aria-controls="offcanvasNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasNavbar" aria-labelledby="offcanvasNavbarLabel">
      <div class="offcanvas-header">
        <h5 class="offcanvas-title text-white" id="offcanvasNavbarLabel">Wahhaab</h5>
        <button type="button" class="btn-close text-reset bg-white mx-4" data-bs-dismiss="offcanvas" aria-label="Close"></button>
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

.title{
  font-weight: 600;
}

.navigation{
  background: rgb(0, 0, 0);
  color: white;
}

.navigation.black{
  background: rgb(0, 0, 0);
}

.nav-link{
  color: white;
  mix-blend-mode: difference;
}
.navigation2{
  display: none;
}

.offcanvas{
  text-align: left;
  background: black;
  opacity: 90%;
}

@media screen and (width < 1000px) {
.navigation{
  display: none;
}

.navigation2{
  display: block;
}
}
</style>