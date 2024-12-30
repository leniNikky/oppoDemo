<script setup>
import Header from './Header.vue'
import SubHeader from './SubHeader.vue'
import Kv from './Kv.vue'
import Picture from './Picture.vue'
import Footer from './Footer.vue'
import {TweenMax} from 'gsap'
import { ref, getCurrentInstance, reactive, onMounted, onUnmounted } from 'vue'
defineProps({
    msg: {
        type: String,
        required: true,
    },
})

function  animateElement() {
        TweenMax.to(proxy.refs.animatedElement, 1, { x: 200 });
        console.log(proxy.refs.animatedElement)
    }

const isFixed = ref(false);
const offset = 53; // 设置固定位置的滚动条位置
const isFixed1 = ref(false);
const offset1 = 492; // 设置固定位置的滚动条位置
const opacity = ref(0);
 
onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});
 
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
 
function handleScroll() {
  isFixed.value = window.scrollY >= offset;
  isFixed1.value = window.scrollY >= offset1;
  console.log(window.screenY)
  if (window.scrollY > 520 && window.scrollY < 1049) {
    console.log('hhh')
    opacity.value = (window.scrollY - 520) / 621
    console.log(opacity.value)
  }
}
</script>

<template>
  <div class="main">
    <Header></Header>
    <sub-header  :class="{ fixed: isFixed }"></sub-header>
    <div style="width:100%;height:47px;" v-if="isFixed"></div>
    <kv></kv>
    <Picture  :class="{ fixed1: isFixed1 }"></Picture>
    <div style="width:100%;height:621px;z-index:1;background:rgb(0,0,0)" :style="{'opacity': opacity}" v-if="isFixed1"></div>
    <Footer></Footer>
    <!-- <h1 class="green">{{ msg }}</h1>
    <div>
        <button @click="animateElement">Animate</button>
    <div ref="animatedElement">I will move!</div>
  </div> -->
  </div>
</template>

<style lang="less" scoped>
.main {
  position: relative;
  .fixed {
    position: fixed;
    width: 100%;
    top: 0;
    // left: 8px;
    z-index: 1000; /* 确保元素在顶部 */
  }
   .fixed1 {
    position: fixed;
    top: 47px;
    right: 0;
    left: 0;
    z-index: -1; /* 确保元素在顶部 */
  }
    .section2 {
      width: 100%;
      height: 561px;
      background: #000;
    }
}
</style>