<template>
  <div class="home">
    <link rel="stylesheet" href="./magic.css" />
    <h1 class="magictime">{{ timerCount }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timerCount: 30,
    };
  },

  watch: {
    timerCount: {
      handler(value) {
        if (value > 0) {
          setTimeout(() => {
            this.timerCount--;
          }, 1000);
        }
      },
      immediate: true,
    },
  },
};
</script>
