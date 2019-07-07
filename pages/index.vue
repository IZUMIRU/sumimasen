<template>
  <section class="container">
    <button class="sumimasen" @click="sumimasen">&#x1f37a;</button>
  </section>
</template>

<script>
export default {
  methods: {
    sumimasen() {
      const ssu = new SpeechSynthesisUtterance();
      ssu.text  = 'すみませーーーん';
      ssu.lang  = 'ja-JP';
      speechSynthesis.speak(ssu);
    },
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.sumimasen {
  text-decoration: none;
  color: #FFF;
  background-color: #FFF;
  width: 120px;
  height: 120px;
  line-height: 120px;
  border-radius: 50%;
  box-shadow: 0px 0px 0px 5px #f3a600;
  border: none;
  font-size: 60px;
}
</style>
