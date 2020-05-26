<template>
  <div id="" :class="bgClass">

  </div>
</template>

<script>
    export default {
      name: "",
      data: () => ({
        active: false
      }),
      computed: {
          bgClass() {
              return this.active ? 'bg-theme-dark-gray' : 'bg-theme-light-gray'
          }
      }
    }
</script>
