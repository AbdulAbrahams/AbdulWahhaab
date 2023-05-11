<template>
        <section class="aboutSec">
          <h1 class="AboutH1 my-5">About Me</h1>
          <div class="row aboutrow">
            <div class="col-md-6 mt-5" data-aos="fade-right" data-aos-duration="1500" style="text-align: left;">
              <p>Hi! I am Abdul Wahhaab Abrahams, but you can call me Wahhaab. I'm an aspiring fullstack Web Developer that
                enjoys helping out wherever I can and sharing the knowledge that i've gained as well as take in new
                information and learn more. I'm a bit of a perfectionist at times and try to recreate things exactly as I
                envisioned it, but i see that as a strength and not a weakness.<br/>
                When I am not in front of the computer coding, I spend my time playing basketball🏀 working out at the
                gym🏋️‍♂️playing games with my friends🎮and spending time with my family👪.</p>
            </div>
            <div class="col-md-6 mt-5 deats" data-aos="fade-left" data-aos-duration="1500">
              <p class="things">
                Full name: Abdul Wahhaab Abrahams<br/>
                Date of birth: 12 May 2002<br/>
                Location: Strandfontein, Cape Town<br/>
                Cell Phone number: 083 400 4653<br/>
                Email Address: abdulabrahams2002@gmail.com
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