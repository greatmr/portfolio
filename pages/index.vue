<template>
  <b-row class="h-100">
    <b-col lg="3" class="d-flex flex-column justify-content-around">
      <div v-for="(item , index) in descriptions" :key="index" v-gsap.fromTo="[{ opacity: 0, x: 350 },{ opacity: 1, x: 0, duration: index+1 }]" class="d-flex flex-column">
        <span class="text-muted text-center text-uppercase mb-3">{{item.label}}</span>
        <h2 class="h2 text-center font-weight-bolder">{{item.content}}</h2>
      </div>
    </b-col>
    <b-col lg="6" class="justify-content-center text-center">
      <h1 class="h1 text-uppercase text-muted" v-gsap.fromTo="[{ opacity: 0, y: -350 },{ opacity: 1, y: 0, duration: 2 }]">
        i'm mohammadreza
      </h1>
      <b-img src="@/assets/images/me2.jpg" width="350" fluid alt="My picture" class="pic-border rounded-pill p-4 filter-grey" v-gsap.fromTo="[{ opacity: 0, y: -350 },{ opacity: 1, y: 0, duration: 1 }]">
      </b-img>
      <h1 class="h1 text-uppercase text-muted" v-gsap.fromTo="[{ opacity: 0, y: 350 },{ opacity: 1, y: 0, duration: 2 }]">
        frontend developer
      </h1>
    </b-col>
    <b-col lg="3" class="d-flex flex-column justify-content-around">
      <div v-for="item in 3" :key="item" v-gsap.fromTo="[{ opacity: 0, x: -350 },{ opacity: 1, x: 0, duration: item+1 }]" class="d-flex flex-column">
        <span class="text-muted text-uppercase mb-3">biography</span>
        <p>Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet </p>
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: 'IndexPage',
 
  data() {
    return {
      descriptions:[
        {
          label:'years of experience',
          content:'8'
        },
        {
          label:'statisfaction clients',
          content:'100%'
        },
        {
          label:'clients on worldwide',
          content:'+ 80'
        },
        {
          label:'projects done',
          content:'675'
        },
      ]
    }
  },
  methods: {

  },
  mounted() {
this.$gsap.to('.title', { x: 100, ease: 'myEase' })
      this.$gsap.to('.text', { y: 100, ease: 'ease.2' })
  }
}
</script>
<style>
.filter-grey{
  filter: grayscale(30%);
}
.pic-border{
  position: relative;
  border: 1px solid #ddd;
}
</style>