<script setup lang="ts">
import { Icon } from '@iconify/vue';
import ProjectCard from './common/ProjectCard.vue'

const projects = [
  {
    title: 'Mini Terminal',
    description: 'A mini terminal with simple commands by Vue3',
    link: 'https://term.mphy.me',
    logo: 'twemoji:laptop',
    tags: ['vue', 'tailwindcss']
  },
  {
    title: 'React 60s View',
    description: '基于 React + Deno 的每日 60 秒读懂世界在线应用',
    link: 'https://60s-view.netlify.app',
    logo: 'twemoji:world-map',
    tags: ['react', 'deno']
  },
  {
    title: '100 React Apps',
    description: 'Try to finish 100 apps with React',
    link: 'https://100a.netlify.app',
    logo: 'twemoji:rocket',
    tags: ['react', 'unocss']
  },
  {
    title: 'Can You Google',
    description: 'A toy app to tell you how to google',
    link: 'https://google.mphy.me',
    logo: 'twemoji:thinking-face',
    tags: ['vue', 'scss']
  },
  {
    title: 'My Personal Site',
    description: 'A personal site built by vue3',
    link: 'https://github.com/Hacker-C/mphy.me',
    logo: 'twemoji:man-technologist-medium-skin-tone',
    tags: ['vue', 'unocss']
  },
  {
    title: 'WZRY Nodejs Spider',
    description: '使用 Nodejs 爬取王者荣耀英雄技能信息',
    link: 'http://wzry.mphy.top',
    logo: 'twemoji:spider-web',
    tags: ['nodejs']
  }
]

</script>

<template>
  <div class="mt-5">
    <div class="flex">
      <h2 class="font-[Cute] mt-5 title-color text-3xl">Projects</h2>
      <span class="flex-1"></span>
      <a href="https://github.com/Hacker-C" target="_blank" class="decoration-none text-gray-7">
        <Icon icon="akar-icons:arrow-up-right" width="30" class="mt-5"/>
      </a>
    </div>
    <div>
      <ProjectCard
        v-for="item of projects"
        :title="item.title"
        :description="item.description"
        :link="item.link"
        :logo="item.logo"
        :tags="item.tags"
      />
    </div>
  </div>

</template>