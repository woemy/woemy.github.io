<template>
  <div class="home fs">
    <img id="woemy-face" src="@/assets/pfp.svg" alt="woemy face" />
    <div id="link-wrapper" class="fs">
      <link-item link="https://youtube.com/@woemymeow">youtube</link-item>
      <link-item link="https://www.instagram.com/woemymeow/">instagram</link-item>
      <link-item link="https://x.com/woemymeow">twitter</link-item>
      <link-item link="https://www.twitch.tv/woemymeow">twitch</link-item>
      <link-item link="https://www.tiktok.com/@woemymeow">tiktok</link-item>
      <link-item link="https://github.com/woemy">github</link-item>
    </div>
  </div>
</template>

<script>
import LinkItem from '@/components/LinkItem.vue'

export default {
  name: 'HomeView',
  components: {
    LinkItem
  }
}
</script>

<style scoped>

.home {
  background-color: var(--main-color);
  display: flex;
  justify-content: center;
  align-items: center;
}

@keyframes face-move {
  0%, 35% {
    margin-top: 0px;
    width: 50vh;
  }
  100% {
    margin-top: -80vh;
    width: 30vh;
  }
}

@keyframes link-fade {
  0%, 40% {
    opacity: 0;
    transform: scale(.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

#woemy-face {
  animation: face-move 1.5s ease;
  animation-fill-mode: forwards;
}

#link-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  animation: link-fade 1.5s ease;
  animation-fill-mode: forwards;
}

/** mobile stylings */

@media screen and (max-device-width: 1000px) {


}
</style>