<template>
  <div class="accordion">
    <header>
      <h3>Title</h3>
      <button @click="toggleVisibility">{{ isVisible ? "-" : "+" }}</button>
    </header>
    <p class="content" :class="{ 'show-content': isVisible }">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias illum
      accusantium alias rerum numquam est mollitia quisquam aut repellendus,
      illo nam distinctio, quidem nisi repellat?
    </p>
  </div>
</template>

<script>
export default {
    data() {
        return {
            isVisible: false,
        }
    },
    methods: {
        toggleVisibility() {
            this.isVisible = !this.isVisible;
        }
    }
}
</script>

<style scoped>
.accordion {
  max-width: 500px;
  margin: 40px 0;
  border: 1px solid royalblue;
  background: skyblue;
  border-radius: 10px;
  overflow: hidden;
}

.accordion > header {
  background: royalblue;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  cursor: pointer;
}

.accordion > header h3 {
  color: aliceblue;
  margin: 0;
}

 .accordion > header button {
  color: aliceblue;
  background: royalblue;
  font-size: 32px;
  border: 2px solid aliceblue;
  border-radius: 5px;
  width: 60px;
  cursor: pointer;
}

.accordion .content {
  display: none;
  padding: 10px;
}
.accordion .show-content {
  display: block;
}

</style>
