<template>
  <a :href="link" id="link-item">
    <slot />
  </a>
</template>

<script>
export default {
  name: 'LinkItem',
  props: ['link', 'icon']
}
</script>

<style scoped>
#link-item {
  background-color: rgba(0, 0, 0, .05);
  width: 30rem;
  height: 4rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 2rem;
  transition: all .2s linear;
  cursor: pointer;
  font-size: 2rem;
  color: black;
  margin: .5rem;
  position: relative;
}

#link-item:hover {
  background-color: rgba(0, 0, 0, .1);
}

/** mobile stylings */

@media screen and (max-device-width: 1000px) {
  #link-item {
    width: 90vw;
  }
}
</style>