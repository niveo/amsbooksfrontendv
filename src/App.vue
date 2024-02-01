<script setup lang="ts">
import { h } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import { HomeOutlined, MenuOutlined } from '@ant-design/icons-vue';
import { Layout, LayoutHeader, LayoutContent, Button } from 'ant-design-vue';


const visualizarPage = (link: string) => {

}

</script>

<template>
  <Layout class="layout">
    <LayoutHeader class="header">
      <Button type="dashed" ghost shape="circle" :icon="h(HomeOutlined)" @click="visualizarPage('')"></Button>
      <div class="fx-flex"></div>
      <Button type="dashed" ghost shape="circle" :icon="h(MenuOutlined)" @click="visualizarPage('')"></Button>
    </LayoutHeader>
    <LayoutContent class="content">
      <div class="inner-content">
        <RouterView />
      </div>
    </LayoutContent>
  </Layout>
</template>

<style scoped>
.layout {
  min-height: 100vh;
}

.header {
  position: fixed;
  width: 100%;
  z-index: 1;
  align-items: center;
  box-sizing: border-box;
  flex-direction: row;
  display: flex;
  gap: 8px;
}

.content {
  padding: 0 50px;
  margin-top: 64px;
}

.inner-content {
  padding: 24px;
  min-height: 380px;
}
</style>
