<template>
  <main>
    <b-row>
    <b-col lg="10">
      <Nuxt/>
    </b-col>
        <b-col class="side-height" lg="2">
            <navbar v-once />
        </b-col>
  </b-row>
  </main>
</template>

<script>
export default {

}
</script>

<style>
.side-height{
    height: 100vh;
}
</style>