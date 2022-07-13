<template>
  <nav class="h-100">
    <aside class="d-flex flex-column align-items-center justify-content-center h-100 py-3">
      <div class="d-flex flex-column justify-content-center h-100 text-center">
        <ul class="progressbar">
        <li  :class="{'active fw-bold':$route.name == 'index' }">
        <router-link v-gsap.fromTo="[{ opacity: 0, x: 350 },{ opacity: 1, x: 0, duration: 1 }]" class="text-dark text-uppercase px-2" to="/">
          Home
        </router-link>
        </li>
        <li  :class="{'active fw-bold':$route.name == 'about' }">
        <router-link v-gsap.fromTo="[{ opacity: 0, x: 350 },{ opacity: 1, x: 0, duration: 2 }]" class="text-dark text-uppercase px-2" to="/about">
          about me
        </router-link>
        </li>
        <!-- <li  >
        <router-link v-gsap.fromTo="[{ opacity: 0, x: 350 },{ opacity: 1, x: 0, duration: 3 }]" class="text-dark text-uppercase px-2" to="about">
          درباره من
        </router-link>
        </li>
        <li  >
        <router-link v-gsap.fromTo="[{ opacity: 0, x: 350 },{ opacity: 1, x: 0, duration: 4 }]" class="text-dark text-uppercase px-2" to="about">
          درباره من
        </router-link>
        </li> -->
        </ul>
      </div>
      <!-- <div class="d-flex flex-column justify-content-end h-100 text-center">
        <social type="instagram"/>
        <social type="linkedin"/>
        <social type="facebook"/>
      </div> -->
    </aside>
  </nav>
</template>
<script>
export default {
  name:'navbar',
  data(){
    return{
    }
  }
}
</script>
<style>
.nuxt-logo {
  height: 180px;
}
.progressbar {
counter-reset: none;
display: flex;
    flex-direction: column;
}
.progressbar li{
      display: flex;
    flex-direction: row-reverse;
    align-items: center;
    width: auto;
list-style-type: none;
position:relative;
text-align: center;

}
.progressbar li:before {
/* CSS for creating steper block before the li item*/
content:"";
/* counter-increment: step; */
height: 1rem;
    width: 1rem;
    border: 2px solid #ddd;
    display: block;
    text-align: center;
    margin: 10px 0px;
    border-radius: 50%;
    background-color: white;
}
.progressbar li:after {
/* CSS for creating horizontal line*/
      content: '';
    position: absolute;
    width: 34%;
    height: 2px;
    background-color: #ddd;
    top: 2px;
    left: -10%;
    z-index: -1;
    transform: rotate(90deg);

}
.progressbar li:first-child:after {
content:none;
}
.progressbar li.active {
color:#000;
}
.progressbar li.active:before {
border-color:#000;
}
/* .progressbar li.active + li:after{
background-color:#000;
} */
</style>
