<template>
        <section class="aboutSec">
          <h1 class="AboutH1 my-5">About Me</h1>
          <div class="row aboutrow">
            <div class="col-md-6 mt-5" data-aos="fade-right" data-aos-duration="1500" style="text-align: left;">
              <p>Hi! I am Abdul Wahhaab Abrahams, but you can call me Wahhaab. I am a QA Analyst/Automation Engineer that
                enjoys helping others and sharing the knowledge that i've gained. I'm a bit of a perfectionist at times, but i see that as a strength and not a weakness.<br/>
                When I am not in front of the computer, I spend my time playing basketball🏀 working out at the
                gym🏋️‍♂️playing games with my friends🎮and spending time with my family👪.</p>
            </div>
            <div class="col-md-6 mt-5 deats" data-aos="fade-left" data-aos-duration="1500">
              <p class="things">
                Full name: Abdul Wahhaab Abrahams<br/>
                Email Address: abdulabrahams2002@gmail.com<br/>
                Date of birth: 12 May 2002<br/>
                Location: Ottery, Cape Town      
              </p>
            </div>
          </div>
        </section>
</template>

<script>
    export default {
        name: 'About'
    }
</script>

<style scoped>

.AboutH1{
  text-align: left;
  color: white;
  mix-blend-mode: difference;
  font-size: clamp(3.4rem, 5vw, 6.5rem);
}

.aboutrow{
  font-size: 18px;
  color: white;
  mix-blend-mode: difference;
  justify-content: center !important;
  align-items: center !important;
}

</style>
