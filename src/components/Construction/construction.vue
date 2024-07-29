<template>
  <div class="container">
    <div>
      <span class="const-page-text">
        <h2 style="padding-top: 100px; font-size: 46px; color: var(--gray-900, #1E212C);">
          We are Createx Construction Bureau
        </h2>
        <p style="padding-top: 20px; font-size: 18px; color: var(--gray-700, #808080);">
          We are rightfully considered to be the best construction company in the USA.
        </p>
      </span>
    </div>

    <div class="const-video container">
      <video ref="video" src="../../assets/placeholder-video1.mp4"></video>
      <img class="play-img" @click="togglePlay"
        :src="isPlaying ? '../../assets/icons/pause.svg' : '../../assets/icons/play.svg'" alt="play">
      <img class="mute-img" @click="toggleMute"
        :src="isMuted ? '../../assets/icons/unmute.svg' : '../../assets/icons/mute.svg'" alt="mute">
    </div>

    <div class="const-part2">
      <span style="display: flex; flex-direction: column; align-items: center;">
        <h2>Our core values</h2>
        <p>Our mission is to set the highest standards for construction sphere.</p>
      </span>
    </div>

    <div style="display: flex; justify-content: space-between; padding-top: 60px;">
      <div class="core-values">
        <span style="display: flex; align-items: center; flex-direction: column;">
          <img src="../../assets/icons/like-finger.svg" alt="like">
          <h3>Quality</h3>
          <p class="const-pp">Culpa nostrud commodo ea consequat aliquip reprehenderit. Veniam velit nostrud aliquip sunt.</p>
        </span>
      </div>

      <span style="width: 1px; height: 188px; background-color: #808080;"></span>

      <div class="core-values">
        <span style="display: flex; align-items: center; flex-direction: column;">
          <img src="../../assets/icons/like-finger.svg" alt="like">
          <h3>Safety</h3>
          <p class="const-pp">Anim reprehenderit sint voluptate exercitation adipisicing laborum adipisicing. Minim empor est ea.</p>
        </span>
      </div>

      <span style="width: 1px; height: 188px; background-color: #808080;"></span>

      <div class="core-values">
        <span style="display: flex; align-items: center; flex-direction: column;">
          <img src="../../assets/icons/like-finger.svg" alt="like">
          <h3>Comfort</h3>
          <p class="const-pp">Sit veniam aute dolore adipisicing nulla sit culpa. Minim mollit voluptate ullamco proident ea ad.</p>
        </span>
      </div>
    </div>
  </div>

        
    
</template>

<script>
export default {
  name: 'Construction',
  data() {
    return {
      isPlaying: false,
      isMuted: false
    };
  },
  methods: {
    togglePlay() {
      const video = this.$refs.video;
      if (video.paused) {
        video.play();
        this.isPlaying = true;
      } else {
        video.pause();
        this.isPlaying = false;
      }
    },
    toggleMute() {
      const video = this.$refs.video;
      video.muted = !video.muted;
      this.isMuted = video.muted;
    }
  }
};
</script>

<style scoped>
.message {
  width: 414px !important;
}
.const-pp{
  padding-top: 8px;
}

.core-values>span>h3 {
  padding-top: 24px;
  padding-bottom: 8px;
  display: flex;
  width: 285px;
  height: 30px;
  flex-direction: column;
  justify-content: center;
  color: var(--gray-900, #1E212C);
  text-align: center;
  font-family: Ubuntu;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: 150%;
  /* 30px */
}

.core-values>span>p {
  width: 285px;
  color: var(--gray-700, #808080);
  text-align: center;
  /* base/regular */
  font-family: Ubuntu;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 160%;
  /* 25.6px */
}

.const-part2>span>p {
  width: 810px;
  color: var(--gray-700, #808080);
  text-align: center;
  font-family: Ubuntu;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
}

.const-part2 {
  color: var(--gray-900, #1E212C);
  text-align: center;
  padding-top: 150px;
  /* h2 */
  font-family: Ubuntu;
  font-size: 46px;
  font-style: normal;
  font-weight: 700;
  line-height: 130%;
  /* 59.8px */
}

.const-video>.play-img {
  position: absolute;
  top: 70%;
  cursor: pointer;
}

.mute-img {
  position: absolute;
  width: 30px;
  height: 30px;
  bottom: -22%;
  left: 11%;
  padding: 3px;
  border-radius: 50%;
  cursor: pointer;
}

.const-video {
  position: relative;
  /* padding-left: 3%; */
  width: 1230px;
  height: 500px;
  border-radius: 4px;
  display: flex;
  justify-content: center;
  /* align-items: center; */
}

.const-video>video {
  width: 1000px;
  height: 700px;
}

.const-page-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>