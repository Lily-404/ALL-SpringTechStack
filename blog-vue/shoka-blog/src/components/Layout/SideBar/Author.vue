<template>
  <div>
    <!-- 作者信息 -->
    <div class="author-container">
      <!-- 作者头像 -->
      <img class="author-avatar" :src="user.avatar" />
      <!-- <img class="author-avatar" :src="blog.blogInfo.siteConfig.authorAvatar" /> -->
      <!-- 作者名称 -->
      <!-- <p class="author-name">{{ blog.blogInfo.siteConfig.siteAuthor }}</p> -->
      <p class="author-name">{{ 'laotutou007' }}</p>
      <!-- 网站简介 -->
      <div class="site-desc">{{ blog.blogInfo.siteConfig.siteIntro }}</div>
    </div>
    <!-- 博客信息 -->
    <blog-info></blog-info>
    <!-- 社交 -->
    <social-list></social-list>
  </div>
</template>

<script setup lang="ts">
import { useBlogStore } from "@/store";
import { useUserStore } from "@/store";
const blog = useBlogStore();
const user = useUserStore();

</script>

<style scoped></style>
