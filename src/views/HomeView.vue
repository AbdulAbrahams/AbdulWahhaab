<template>
    <div class="body">
      <Navbar />
      <div class="container">
        <section class="introSec">
          <div class="row introduction">
            <div class="col-md-6 intro" data-aos="fade-left" data-aos-duration="2000">
              <h1 class="introH1">Abdul Wahhaab Abrahams</h1>
              <h3 class="my-1">Web Developer</h3>
              <a href="#about" class="learn btn btn-lg btn-light my-4 px-5" style="border-radius: 0px;">Learn About Me</a>
              <div class="footer-bar mx-4">
                <a href="https://www.youtube.com/@AbnormalAbdul12"><i class="fa fa-youtube-play"></i></a>
                <a href="https://www.instagram.com/abdul_abrahams_/"><i class="fa fa-instagram mx-4"></i></a> 
                <a href="https://www.linkedin.com/in/abdul-wahhaab-abrahams-506142222/"><i class="fa fa-linkedin"></i></a> 
                <a href="https://github.com/AbdulAbrahams"><i class="fa fa-github mx-4"></i></a>
              </div>
            </div>
            <div class="col-md-6 ImgCol my-5" data-aos="fade" data-aos-easing="linear" data-aos-duration="2000">
              <img class="meImg" src="https://i.postimg.cc/KjpBpkMW/Screenshot-2023-04-17-143529.png" alt="">
            </div>
          </div>
        </section>
        <div class="space" id="about"></div>
        <section>
          <About/>
        </section>
        <div class="space" id="resume"></div>
        <section>
          <Resume/>
        </section>
        <div class="space" id="testimonials"></div>
        <section>
          <Testimonials/>
        </section>
        <div class="space" id="projects"></div>
        <section>
          <Projects/>
        </section>
        <div class="space" id="contact"></div>
        <section>
          <Contact/>
        </section>
      </div>
      <Footer/>
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'
import About from '../components/About.vue'
import Resume from '../components/Resume.vue'
import Testimonials from '../components/Testimonials.vue'
import Projects from '../components/Projects.vue'
import Contact from '../components/Contact.vue'
import Footer from '../components/Footer.vue'
import Spinner from '../components/Spinner.vue'
export default {
  name: 'HomeView',
  components: { Navbar, About, Resume, Testimonials, Projects, Contact, Footer, Spinner }
      }
</script>

<style  scoped>

.learn:hover{
  background-color: black;
  color: white;
  transition: 0.5s;
}
.footer-bar a{
  font-size: 30px;
  margin: 3px;
}
.footer-bar a i{
    color: rgb(255, 255, 255) !important;
}
.footer-bar a i:hover{
    color: rgba(255, 255, 255, 0.721) !important;
}

.space{
  height: 80px;
}
.body {
  overflow-x: hidden;
  position: absolute;
  width: 100%;
  background-image: linear-gradient(240deg, rgb(255, 255, 255) 25.5%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
}

.container{
  justify-content: space-between;
  color: white;
}

section{
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.introSec{
  justify-content: center;
  align-items: center;
}

.resCont{
  width: 100%;
}

.introH1{
  font-size: clamp(3.6rem, 5vw, 6.5rem);
}

.intro {
  color: white;
  text-align: left;
  mix-blend-mode: difference;
}

.introduction{
  justify-content: center;
  align-items: center;
}

.meImg {
  max-height: 705px;
  float: right;
  mix-blend-mode: luminosity !important;
}
@media screen and (width < 1000px) {
  .body{
    background-image: linear-gradient(240deg, rgb(255, 255, 255) 12%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
  }

  .introH1{
    font-size: 3rem !important;
  }

  .meImg{
    max-height: 615px;
  }
}

@media screen and (width < 768px) {
  .body{
    background-image: linear-gradient(240deg, rgb(255, 255, 255) 8%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
  }
  .ImgCol{
    display: none;
  }
  .introH1{
    margin-top: 30vh;
  font-size: clamp(3.4rem, 5vw, 5rem);
}
}
@media screen and (width < 425px) {
  .body{
    background-image: linear-gradient(240deg, rgb(255, 255, 255) 6.5%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
  }
}
</style>
