<script setup lang="ts">
import { onMounted } from 'vue'
import { load } from './sponsors'
// NOTE: hide the home video
// https://github.com/vuejs-translations/docs-zh-cn/issues/177

onMounted(async () => {
  await load()
})
</script>

<template>
  <section id="hero">
    <h1 class="tagline">
      <img src="/public/logo.png" alt="" srcset="">
    </h1>
    <p class="description">
      一款高效、轻量、免费开源的跨平台图形引擎，也是实时 3D 内容创作平台。它不仅能完美胜任 2D、3D 的游戏开发工作，同时在汽车、XR、元宇宙、教育等领域也都能提供完善的解决方案。
    </p>
    <p class="actions">
      <!-- NOTE: hide the home video -->
      <a class="get-started" href="https://docs.cocos.com/creator/manual/zh/">
        快速上手
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" width="10" height="10" viewBox="0 0 24 24">
          <path d="M13.025 1l-2.847 2.828 6.176 6.176h-16.354v3.992h16.354l-6.176 6.176 2.847 2.828 10.975-11z" />
        </svg>
      </a>
      <!-- <a class="setup" href="/guide/quick-start.html">安装</a> -->
    </p>
  </section>

  <section id="highlights" class="vt-box-container">
    <div class="vt-box">
      <h2><strong>一体化编辑器</strong></h2>
      <ul>
        <li>为美术策划深度参与设计的编辑器</li>
        <li>强大的插件系统，自由拓展</li>
        <li>从未如此丝滑的动画编辑器</li>
        <li>易上手方便调试的 TypeScript 脚本语言</li>
      </ul>
    </div>
    <div class="vt-box">
      <h2><strong>完善的框架</strong></h2>
      <ul>
        <li>基于 Command Buffer 提交渲染数据</li>
        <li>次世代引擎底层架构，面向未来的渲染 API 设计，支持 Vulkan、Metal、WebGL 等渲染后端</li>
      </ul>
    </div>
    <div class="vt-box">
      <h2><strong>2D 与 3D</strong></h2>
      <ul>
        <li>同样优秀的 2D 与 3D 制作支持，满足多样需求</li>
        <li>完美适配 Spine、DragonBones、TiledMap、Box2D 和 Texture Packer 等 2D 开发中间件</li>
      </ul>
    </div>
    <div class="vt-box">
      <h2><strong>开源</strong></h2>
      <ul>
        <li>底层框架开源，社区共创无限可能</li>
        <li>可定制、可嵌入、包体小、易上手</li>
      </ul>
    </div>
    <div class="vt-box">
      <h2><strong>超高的性能</strong></h2>
      <ul>
        <li>高性能 HDR 渲染</li>
        <li>超高效的 GPU Driven 骨骼动面</li>
        <li>自动合图和自动合批为 2D 游戏保驾护航</li>
      </ul>
    </div>
    <div class="vt-box">
      <h2><strong>跨平台支持</strong></h2>
      <p>
      <ul>
        <li>
          深度支持各大主流平台，快速发布到 Web、iOS、Android、HarmonyOS、Windows、Mac, 以及各个小游戏平台
        </li>
      </ul>
      </p>
    </div>
  </section>
</template>

<style scoped>
section {
  padding: 42px 32px;
}

#hero {
  /* padding: 96px 32px; */
  text-align: center;
}

.tagline {
  font-size: 76px;
  line-height: 1.25;
  font-weight: 900;
  letter-spacing: -1.5px;
  max-width: 960px;
  margin: 0px auto;
}

.tagline img {
  text-align: center;
  margin: auto;
  height: 200px;
}

html:not(.dark) .accent,
.dark .tagline {
  background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.description {
  max-width: 960px;
  line-height: 1.5;
  color: var(--vt-c-text-2);
  transition: color 0.5s;
  font-size: 22px;
  margin: 24px auto 40px;
}

.actions a {
  font-size: 16px;
  display: inline-block;
  background-color: var(--vt-c-bg-mute);
  padding: 8px 18px;
  font-weight: 500;
  border-radius: 8px;
  transition: background-color 0.5s, color 0.5s;
}

.actions .get-started {
  margin-right: 18px;
}

.actions .icon {
  display: inline;
  position: relative;
  top: -1px;
  margin-left: 2px;
  fill: currentColor;
  transition: transform 0.2s;
}

.actions .get-started:hover {
  transition-duration: 0.2s;
}

.actions .get-started:hover .icon {
  transform: translateX(2px);
}

.actions .get-started,
.actions .setup {
  color: var(--vt-c-text-code);
}

.actions .get-started:hover,
.actions .setup:hover {
  background-color: var(--vt-c-gray-light-4);
  transition-duration: 0.2s;
}

.dark .actions .get-started:hover,
.dark .actions .setup:hover {
  background-color: var(--vt-c-gray-dark-3);
}

/* NOTE: via #vuemastery-action in VueMasteryModal.vue */

.actions .get-started {
  font-size: 16px;
  display: inline-block;
  border-radius: 8px;
  transition: background-color 0.5s, color 0.5s;
  position: relative;
  font-weight: 600;
  background-color: var(--vt-c-green);
  color: #fff;
  margin-right: 18px;
  padding: 8px 1em;
}

.dark .actions .get-started {
  color: var(--vt-c-indigo);
}

.actions .get-started:hover {
  background-color: var(--vt-c-green-dark);
  transition-duration: 0.2s;
}

.dark .actions .get-started:hover {
  background-color: var(--vt-c-green-light);
}

/* end NOTE */

#special-sponsor {
  border-top: 1px solid var(--vt-c-divider-light);
  border-bottom: 1px solid var(--vt-c-divider-light);
  padding: 12px 24px;
}

#special-sponsor h3 {
  text-align: center;
  font-size: 13px;
  font-weight: 500;
  padding-bottom: 10px;
}

#special-sponsor-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

#special-sponsor .logo {
  display: flex;
  justify-content: center;
  padding: 0 20px;
}

.dark #special-sponsor img {
  filter: grayscale(1) invert(1);
}

#highlights {
  max-width: 1370px;
  margin: 0px auto;
  color: var(--vt-c-text-2);
}

#highlights h2 {
  font-weight: 600;
  font-size: 20px;
  letter-spacing: -0.4px;
  color: var(--vt-c-text-1);
  transition: color 0.5s;
  margin-bottom: 0.75em;
}

#highlights p {
  font-weight: 400;
  font-size: 15px;
}

#highlights .vt-box {
  background-color: transparent;
}

#sponsors {
  max-width: 900px;
  margin: 0px auto;
}

#sponsors h2 {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 1em;
}

#sponsors .sponsor-container {
  margin-bottom: 3em;
}

@media (max-width: 960px) {
  .tagline {
    font-size: 64px;
    letter-spacing: -0.5px;
  }

  .description {
    font-size: 18px;
    margin-bottom: 48px;
  }
}

@media (max-width: 768px) {
  .tagline {
    font-size: 48px;
    letter-spacing: -0.5px;
  }
}

@media (max-width: 576px) {
  #hero {
    padding: 56px 32px;
  }

  .description {
    font-size: 16px;
    margin: 18px 0 30px;
  }

  #special-sponsor {
    flex-direction: column;
    height: auto;
  }

  #special-sponsor img {
    height: 36px;
    margin: 8px 0;
  }

  #special-sponsor span {
    text-align: center !important;
  }

  #highlights h3 {
    margin-bottom: 0.6em;
  }

  #highlights .vt-box {
    padding: 20px 36px;
  }

  .actions a {
    margin: 18px 0;
  }
}

@media (max-width: 370px) {
  .tagline {
    font-size: 36px;
  }
}
</style>
