<template>
        <section>
          <h1 class="ResumeH1">Resume</h1>
          <div class="resCont" style="display:inline-block;">
              <div class="justify-content-center mx-2">
              <div class="row my-5 resRow" v-for="person in resume">
                <div class="col-md-6 my-1" data-aos="fade-up" data-aos-duration="1200" style="text-align: left;">
                          <h6 class="my-4 text-primary" style=" margin-bottom: 20px;">📅  {{ person.period }}</h6>
                    <a :href="person.link" class="personLink text-white"><h2>{{ person.name }}</h2></a>
                    <div class="desc">{{ person.description}}</div>
                  </div>
                  <div class="col-md-6 imgCol my-1" data-aos="fade-up" data-aos-duration="1200">
                    <img :src="person.image" alt="">
                  </div>
          </div>
          </div>
          </div>
          <h1 class="skillsH1">Skills</h1>
          <div class="container-lg" style="display:inline-block;">
              <div class="row justify-content-center mx-2">
              <div class="col-md-3 mx-2 my-2 skillsCol" data-aos="fade" data-aos-duration="1200" v-for="pic in skills">
                        <img :src="pic.image" alt="">
          </div>
          </div>
          </div>
        </section>
</template>

<script>
    export default {
        name: 'Resume',
        data(){
              return{
                  resume:[
                      {
                          name: 'Life Choices Coding Academy',
                          period: ' September 2022 – Present',
                          description: "I am currently learning coding and web development at 'Life Choices Coding Academy' to become a fullstack web developer and learning things that would have taken me ages to learn at rosebank such as HTML, CSS and Bootstrap. Learning at Life Choices has dramatically changed my work ethic for the better.",
                          image: "https://i.postimg.cc/Y0rMDgkr/Logo.png",
                          link: "https://lifechoices.co.za/"
                      },
                      {
                          name: 'Rosebank College',
                          period: 'January 2022 - August 2022',
                          description: "Studied bachelor's Degree in I.T. at Rosebank College but left due to the fact that I wasn't learning much and when i heard back from life choices i made my decision to leave.",
                          image: "https://i.postimg.cc/XYQ8QQnm/rc-logo.png",
                          link: "https://www.rosebankcollege.co.za/"
                      },
                      {
                          name: 'Muizenberg High School',
                          period: 'January 2015 - December 2019',
                          description: "I matriculated at Muizenberg High School in 2019 with a bachelor's pass. My subjects were Pure Mathematics, Physical Sciences, Business Studies, Music, English, Afrikaans and Life Orientation.",
                          image: "https://i.postimg.cc/CLJkg59f/1940005-1389649074636868-537002596-n.png",
                          link: "https://muizenberghigh.org/"
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

<style scoped>

.resCont{
  width: 100%;
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

.resRow{
  justify-content: center !important;
  align-items: center !important;
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

.personLink{
  text-decoration: none;
}

.personLink h2:hover{
  color: rgb(0, 76, 255);
  transition: 0.5s;
}

@media screen and (width < 1000px) {

  .introH1{
    font-size: 3rem !important;
  }

  .meImg{
    max-height: 615px;
  }
}

@media screen and (width < 768px) {
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
.skillsCol img{
    margin-top: 5% !important;
}
}
</style>