<template>

<div>
  <div class="curved-background">

      <div class="curved-background__curved xl:max-xl:overflow-hidden">
          <navbar />
          <div class="dad">
            <div class="son_1">
              <h2  data-aos="fade-right" data-aos-offset="300" data-aos-easing="ease-in-sine" data-aos-duration="800" class=" mb-6 text-5xl text-purple-600 font-extrabold dark:text-white max-lg:text-4xl max-lg:mb-2">Scholar <span class=" underline decoration-pink-500">Flow</span></h2>
              <h2  class=" subtext mt-8 mb-6 text-4xl text-white font-extrabold dark:text-white">Vous êtes des <span class=" underline decoration-purple-500">milliers</span> à nous faire confiance</h2>
              <p  class=" subtext tracking-wide mb-4 text-base font-normal text-gray-600 dark:text-gray-400">Nous analysons et suivont les performances de plus de <span class="font-semibold underline decoration-indigo-500">10 000</span> élèves à travers tout le Cameroun, tous issues d'etablissements divers mais avec <span class="underline decoration-pink-500">des performances toutes aussi exemplaires.</span></p>
              <button  type="button" class=" download_1 shadow-xl mt-6 font-medium text-black bg-white hover:bg-blue-700 hover:text-white focus:ring-4 focus:ring-blue-300 font-semi rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800 transition duration-300 ease-in-out hover:-translate-y-1 hover:scale-110">Telecharger l'application mobile <i class="ml-2 fa-solid fa-mobile-button"></i></button>
            </div>
            <div class="son_2 max-lg:hidden" >
              <img data-aos="zoom-in-right" data-aos-duration="3000"   id="avatarButton" type="button" data-dropdown-toggle="userDropdown" data-dropdown-placement="bottom-start" class="ml-6 mt-4 w-96 h-96 rounded-full cursor-pointer max-lg:hidden" src="../assets/photo_4.webp" alt="User dropdown" >
              <div data-aos="zoom-in-right" data-aos-duration="2000" class="son_2_1">
                <img id="avatarButton" type="button" data-dropdown-toggle="userDropdown" data-dropdown-placement="bottom-start" class="ml-4 mt-4 w-48 h-48 rounded-full cursor-pointer max-lg:hidden " src="../assets/photo_3.webp" alt="User dropdown">
                <img id="avatarButton" type="button" data-dropdown-toggle="userDropdown" data-dropdown-placement="bottom-start" class="ml-4 mt-4 w-24 h-24 rounded-full cursor-pointer max-lg:hidden " src="../assets/photo_2.webp" alt="User dropdown">
                <img id="avatarButton" type="button" data-dropdown-toggle="userDropdown" data-dropdown-placement="bottom-start" class="son_2_1_1 ml-1 w-48 h-48 rounded-full cursor-pointer max-xl:hidden " src="../assets/photo_5.webp" alt="User dropdown">
              </div>
            </div>
          </div> 
      <div class="searchBar">
        
      <searchBar  />        
      </div> 

      </div>
  </div>


  <footer_ data-aos="zoom-in" data-aos-duration="1000"/>

</div>

</template>

<script setup>
import navbar from '../components/navbar.vue';
import searchBar from '../components/searchBar.vue';
import footer_ from '../components/footer_.vue';
import Caroussel from '../components/Caroussel.vue';



</script>

<style scoped>
.curved-background{
  position: relative;
  width: 100%;
  height: auto;
  z-index: 0;
}
.curved-background__curved {
    /* Background color */
    background-color: #F8C822;

    position: relative;

    /* You can use gradient background color such as */
    /* background: linear-gradient(rgba(0, 0, 0, 0.2) 0%, rgba(0, 0, 0, 0.1) 100%); */

    /* Curved corners */
    border-bottom-left-radius: 50% 10%;
    border-bottom-right-radius: 50% 10%;

    /* Size */
    height: 95vh;
    width: 100%;

}

h1{
  z-index: 1;
  height: 200px;
}

.searchBar{
  position: absolute;
  margin-top: 83vh;
  width: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.dad{
  position: absolute;
  width: auto;
  height: 65vh;
  z-index: 100;
  margin-top: 30px;
  padding-left: 3vw;
  display: grid;
  grid-template-columns: 40% 55%;
  grid-template-rows: 100%;
  grid-template-areas: 
  "son_1 son_2";
  grid-gap: 5px;
}

.son_1{
  grid-area: son_1;
  display: flex;
  flex-direction: column;
  padding-top: 50px;
  align-items: flex-start;
}
.son_2{
  grid-area: son_2;
  position: relative;
}

.son_2_1{
  position: absolute;
  margin-top: -400px;
  margin-left: 400px;
}

.son_2_1_1{
  margin-top: -75opx;
  margin-left: 150px;
}

.son_2_1_2{
  margin-top: -700px;
  margin-left: 250px;
}

.body_content{
  background-color: red;
  width: 100vh;
  height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;

  left: 50%;
  transform: translate(-50%, -50%);
}


@media only screen and (max-width: 1024px) {
    .dad{
    position: absolute;
    width: auto;
    height: auto;
    z-index: 100;
    margin-top: 30px;
    padding-left: 3vw;
    padding-right: 3vw;
    display: grid;
    grid-template-columns: 100%;
    grid-template-rows: 100%;
    grid-template-areas: 
    "son_1";
    grid-gap: 5px;
  }

  .son_1{
  grid-area: son_1;
  display: flex;
  flex-direction: column;
  padding-top: 60px;
  align-items: center;
}

.subtext{
  padding-left: 2vw;
  padding-right: 3vw;
  text-align: center;
}

}

@media only screen and (max-width: 425px) {
  .download_1{
    margin-top: 1rem;
  }

  .searchBar{
  position: absolute;
  margin-top: 87vh;
  width: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
}
}
</style>