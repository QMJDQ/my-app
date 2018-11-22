<template>
  <div class="home">
      <HelloWorld :msg="cc" @msg="jj"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
    data: function() {
        return {
            cc: 111
        };
    },
    components: {
        HelloWorld
    },
    methods: {
      jj (val) {
          alert(val)
      }
    }
}
</script>
