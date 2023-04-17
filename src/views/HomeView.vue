<template>
  <div v-if="skills">
    <div class="body">
      <Navbar />
      <div class="container">
        <section class="introSec">
          <div class="row introduction">
            <div class="col-md-6 intro">
              <h1 class="introH1">Abdul Wahhaab Abrahams</h1>
              <h3 class="my-1">Web Developer</h3>
              <a href="#about" class="btn btn-lg btn-light my-4 px-5" style="border-radius: 0px;">Learn About Me</a>
            </div>
            <div class="col-md-6 ImgCol my-5">
              <img class="meImg" src="https://i.postimg.cc/sX56rV4K/Screenshot-2023-04-17-143529.png" alt="">
            </div>
          </div>
        </section>
        <div class="space" id="about"></div>
        <section class="aboutSec">
          <h1 class="AboutH1">About Me</h1>
          <div class="row aboutrow">
            <div class="col-md-6" style="text-align: left;">
              <p>Hi! I am Abdul Wahhaab Abrahams, but you can call me Wahhaab. I'm an aspiring fullstack Web Developer that
                enjoys helping out wherever I can and sharing the knowledge that i've gained as well as take in new
                information and learn more. I'm a bit of a perfectionist at times and try to recreate things exactly as I
                envisioned it, but i see that as a strength and not a weakness.<br/>
                When I am not in front of the computer coding, I spend my time playing basketball🏀 working out at the
                gym🏋️‍♂️playing games with my friends🎮and spending time with my family👪.</p>
            </div>
            <div class="col-md-6 deats">
              <p class="things">
                Full name: Abdul Wahhaab Abrahams<br/>
                Date of birth: 12 May 2002<br/>
                Location: Cape Town<br/>
                Cell Phone number: 083 400 4653<br/>
                Email Address: abdulabrahams2002@gmail.com
              </p>
            </div>
          </div>
        </section>
        <div class="space" id="resume"></div>
        <section>
          <h1 class="ResumeH1">Resume</h1>
          <div class="resCont" style="display:inline-block;">
              <div class="justify-content-center mx-2">
              <div class="row my-5 resRow" v-for="person in resume">
                <div class="col-md-6" style="text-align: left;">
                          <h6 class="my-4 text-primary" style=" margin-bottom: 20px;">📅  {{ person.period }}</h6>
                    <h2>{{ person.name }}</h2>
                    <div class="desc">{{ person.description}}</div>
                  </div>
                  <div class="col-md-6 imgCol">
                    <img :src="person.image" alt="">
                  </div>
          </div>
          </div>
          </div>
          <h1 class="skillsH1">Skills</h1>
          <div class="container-lg" style="display:inline-block;">
              <div class="row justify-content-center mx-2">
              <div class="col-md-3 mx-2 my-2 skillsCol" v-for="pic in skills">
                        <img :src="pic.image" alt="">
          </div>
          </div>
          </div>
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
  </div>

  <div v-else>
    <Spinner/>
  </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'
import Testimonials from '../components/Testimonials.vue'
import Projects from '../components/Projects.vue'
import Contact from '../components/Contact.vue'
import Footer from '../components/Footer.vue'
import Spinner from '../components/Spinner.vue'
export default {
  name: 'HomeView',
  components: { Navbar, Testimonials, Projects, Contact, Footer, Spinner },
      data(){
              return{
                  resume:[
                      {
                          name: 'Life Choices Coding Academy',
                          period: ' September 2022 – Present',
                          description: "I am currently learning coding and web development at 'Life Choices Coding Academy' to become a fullstack web developer and learning things that would have taken me ages to learn at rosebank such as HTML, CSS and Bootstrap. Learning at Life Choices has dramatically changed my work ethic for the better.",
                          image: "https://i.postimg.cc/Y0rMDgkr/Logo.png"
                      },
                      {
                          name: 'Rosebank College',
                          period: 'January 2022 - August 2022',
                          description: "Studied bachelor's Degree in I.T. at Rosebank College but left due to the fact that I wasn't learning much and when i heard back from life choices i made my decision to leave.",
                          image: "https://i.postimg.cc/XYQ8QQnm/rc-logo.png"
                      },
                      {
                          name: 'Muizenberg High School',
                          period: 'January 2015 - December 2019',
                          description: "I matriculated at Muizenberg High School in 2019 with a bachelor's pass. My subjects were pure Maths, Physics, Business Studies, Music, English, Afrikaans and Life Orientation.",
                          image: "https://i.postimg.cc/CLJkg59f/1940005-1389649074636868-537002596-n.png"
                      }
                  ],

                  skills:[
                    {
                        image: 'https://i.postimg.cc/76DKxRLK/pngegg-5.png'
                    },
                    {
                        image: 'https://i.postimg.cc/G2yjQ2YH/html-png.png'
                    },
                    {
                        image: 'https://i.postimg.cc/gcKhP8YG/bootstrap.png'
                    },
                    {
                        image: 'https://i.postimg.cc/152h991M/pngegg-7.png'
                    },
                    {
                        image: 'https://i.postimg.cc/QMSTTYb4/pngegg-6.png'
                    },
                    {
                        image: 'https://i.postimg.cc/CxMw1XgR/pngegg-2.png'
                    },
                    {
                        image: 'https://i.postimg.cc/Zn6MFbrJ/pngegg-1.png'
                    }
                  ]
              }
          }
      }
</script>

<style  scoped>

.space{
  height: 80px;
}
.body {
  overflow-x: hidden;
  position: absolute;
  width: 100%;
  background-image: linear-gradient(240deg, rgb(255, 255, 255) 26%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
}

.container{
  justify-content: space-between;
  color: white;
}

.introSec{
  min-height: 100vh;
}

.resCont{
  width: 100%;
}

.introH1{
  font-size: clamp(3.8rem, 5vw, 6.5rem);
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

.shadow{
  max-height: 745px;
  position: absolute;
  mix-blend-mode: difference;
}

.AboutH1{
  text-align: left;
  mix-blend-mode: difference;
  font-size: clamp(3.4rem, 5vw, 6.5rem);
}

.ResumeH1{
  text-align: left;
  mix-blend-mode: difference;
  font-size: clamp(3.4rem, 5vw, 6.5rem);
}

.skillsH1{
  text-align: left;
  mix-blend-mode: difference;
  font-size: clamp(3.4rem, 5vw, 6.5rem);
}

.aboutrow{
  font-size: 18px;
  mix-blend-mode: difference;
  justify-content: center !important;
  align-items: center !important;
}

.resRow{
  justify-content: center !important;
  align-items: center !important;
}

.deats{
  justify-content: center !important;
}
.details small{
  color: rgb(220, 220, 220);
}
.details h6{
  text-align: left;
  font-size: 13px;
}
.resRow img{
  max-width: 250px;
}
.desc{
  mix-blend-mode: difference;
  margin-top: 4%;
}

.skillsCol{
    height: 20vh;
    mix-blend-mode: luminosity;
}
.skillsCol img{
    margin-top: 5%;
    max-width: 100%;
    max-height: 80%;
}
.skillsCol:hover{
  mix-blend-mode: unset;
}
@media screen and (width < 768px) {
  .body{
    background-image: linear-gradient(240deg, rgb(255, 255, 255) 10%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
  }
  .ImgCol{
    display: none;
  }

  .introH1{
    margin-top: 30vh;
  font-size: clamp(3.4rem, 5vw, 5rem);
}
.skillsCol img{
    margin-top: 2% !important;
}
}
@media screen and (width < 425px) {
  .body{
    background-image: linear-gradient(240deg, rgb(255, 255, 255) 6.5%, rgb(0, 0, 0) 1%, rgb(0, 0, 0));
  }
.skillsCol img{
    margin-top: 5% !important;
}
}
</style>
