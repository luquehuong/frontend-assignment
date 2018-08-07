<template>
 <div class="html-content container max-w-full">
      <div class="header-background">
        <div class="navigation flex justify-between mb-4 px-4 pb-1 flex-wrap">
            <div class="w-1/3">
                <p class="paragraph">START BOOTSTRAP</p>
            </div>
             <nav class=" flex justify-end w-2/3 flex-wrap">
            <p class="mx-10 paragraph">ABOUT</p>
            <p class="mx-10 paragraph">SERVICES</p>
            <p class="mx-10 paragraph">PORTFOLIO</p>
            <p class="mx-10 paragraph">CONTACT</p>
             </nav>
        </div>
        <div class="container mx-auto w-5/6">

            <h1 class="paragraph text-center my-10">YOUR FAVORITE SOURCE OF <br> FREE BOOTSTRAP THEMES</h1>
            <p class="paragraph text-center my-10">Start Bootstrap can help you build better websites using the Bootstrap CSS framework! Just download <br> your template and start going, no strings attached!</p>
            <button class="btn mx-auto">FIND OUT MORE</button>

        </div>


      </div>
      <!--  -->
      <div class="container max-w-full content-intro">
           <div class="container mx-auto py-5 w-5/6">
               <h2 class="paragraph text-center">We're got what we need!</h2>
               <p class="paragraph text-center my-10">Start Bootstrap has everything you need to get your new website up and running in no time! <br> All of the templates and themes on Start Bootstrap are open source, free to download, and <br> easy to use. No strings attached!</p>
               <button class="btn mx-auto my-10">GET STARTED!</button>
           </div>
      </div>
      <!--  -->
      <div class="containter max-w-full content-service">
               <div class="container mx-auto w-5/6">
                      <h2 class="text-center my-10">At Your Servive</h2>
                      <div class=" flex flex-wrap">
                           <div class="w-full md:w-1/2 lg:w-1/4  text-center">
                                     <i class="fas fa-gem"></i>
                                     <h3>Sturdy Templates</h3>
                                    <p>Our templates are updated regularly so they don't break.</p>
                           </div>
                            <div class="w-full md:w-1/2 lg:w-1/4 text-center">
                               <i class="fas fa-plane"></i>
                              <h3>Ready so Ship</h3>
                              <p>Our templates are updated regularly so they don't break.</p>
                           </div>
                            <div class="w-full md:w-1/2 lg:w-1/4 text-center">
                                 <i class="fas fa-envelope"></i>
                                  <h3>Sturdy Templates</h3>
                                 <p>Our templates are updated regularly so they don't break.</p>
                           </div>
                            <div class="w-full md:w-1/2 lg:w-1/4 text-center">
                                <i class="fas fa-heart"></i>
                                  <h3>Made with Love</h3>
                                 <p>Our templates are updated regularly so they don't break.</p>
                           </div>

                      </div>
               </div>

      </div>
      <div class="container max-w-full content-image flex flex-wrap">
           <div class="w-full md:w-1/3 lg:w-1/3">
                <img src="https://i.imgur.com/dn1QSBo.jpg">
           </div>
             <div class="w-full md:w-1/3 lg:w-1/3">
             <img src="https://i.imgur.com/dn1QSBo.jpg">
           </div>
             <div class="w-full md:w-1/3 lg:w-1/3">
            <img src="https://i.imgur.com/dn1QSBo.jpg">
           </div>
             <div class="w-full md:w-1/3 lg:w-1/3">
             <img src="https://i.imgur.com/dn1QSBo.jpg">
           </div>
             <div class="w-full md:w-1/3 lg:w-1/3">
               <img src="https://i.imgur.com/dn1QSBo.jpg">
           </div>
             <div class="w-full md:w-1/3 lg:w-1/3">
               <img src="https://i.imgur.com/dn1QSBo.jpg">
           </div>
      </div>
      <!--  -->
      <div class="container max-w-full content-download">
        <div class="w-5/6 mx-auto">
             <h2 class="text-center">Free Download at Start Bootstrap!</h2>
             <button class="btn mx-auto my-10">DOWNLOAD NOW!</button>
        </div>

      </div>
      <!--  -->
     <div class="containter max-w-full footer">
       <div class="container w-3/5 mx-auto">
            <h2 class="text-center">Let's Get In Touch</h2>
            <p class="text-center">Ready to start your next project with us? That's great! Give us a call or send us an email and <br> we will get back to you as soon as possible!</p>
           <div class="flex flex-wrap py-10">
               <div class="w-full md:w-1/2 text-center">

                            <i class="fas fa-phone"></i>
                            <p>123-456-789</p>

               </div>
               <div class="w-full md:w-1/2 text-center">
                     <i class="fas fa-envelope"></i>
                     <p>hiepdangnguyendai@gmail.com</p>
               </div>
           </div>
       </div>


     </div>





</div>





</template>

<script>
import AppLogo from "~/components/AppLogo.vue";

export default {
  components: {
    AppLogo
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Open+Sans");
* {
  font-family: "Open Sans", sans-serif;
  text-decoration: none;
}
.container {
  /* min-height: 100vh; */
  /* margin-top: 15%; */

}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.header {
  display: flex;
}
.row-content-service {
  display: flex;
}
#logo {
  display: flex;
  /* margin-left: auto; */
}
.navigation > p {
  margin-left: 10px;
  /* color: rgba(255, 255, 255, 0.7); */
}
.navigation {
}

.header {
  background-image: url("https://i.imgur.com/FXI0gmp.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: auto;
  padding-top: 2%;
  padding-bottom: 20%;
}
.paragraph {
  color: rgba(255, 255, 255, 0.7);
}
.contents {
  background-color: #f05f40;
  width: 100%;
  height: auto;
  padding-bottom: 10%;
  padding-top: 5%;
}
.download-service {
  background-color: black;
  width: 100%;
  margin-top: -7%;
  height: auto;
  padding-bottom: 10%;
  padding-top: 5%;
}
.title-header {
  margin-top: 10%;
}
.container {
  /* width: 1200px; */
}
.header-background {
  background-image: url("https://i.imgur.com/FXI0gmp.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: auto;
  padding-top: 2%;
  padding-bottom: 20%;
}
.content-intro {
   background-color: #f05f40;
}
</style>

