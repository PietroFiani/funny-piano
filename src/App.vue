<template>
  <div id="app" class="body w-100% h-100%">
    <div class="app-container flex flex-col items-center">
      <span class="title mt-16"> <img src="@/assets/title.svg" alt=""></span>
      <v-piano></v-piano>
    </div>
    
  </div>
</template>

<script>
import VPiano from '@/components/VPiano'
export default {
  name: 'App',
  components: {
    VPiano
  }
}
</script>

<style lang="postcss">
.body {
  height:100vh; 
  background:linear-gradient(135deg, #FF9D6C 0%, #BB4E75 100%);
}
.app-container{
  width: 100%;
  height: 100%;
  
}

</style>