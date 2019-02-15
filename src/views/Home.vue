<template>
  <div class="home">
    <HelloWorld>
       <template v-slot:[slotForHeader]>Hello</template>
       <template v-slot:footer="{ nameInfo }">
         Data from child component {{nameInfo.lastName}}
       </template>
    </HelloWorld>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'home',
  data() {
    return {
      slotForHeader: 'header',
    };
  },
  components: {
    HelloWorld,
  },
};
</script>
