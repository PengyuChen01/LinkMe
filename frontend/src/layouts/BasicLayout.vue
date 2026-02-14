
<template>
 <van-nav-bar
  title="标题"
  right-text="按钮"
  left-arrow
  @click-left="onClickLeft"
  @click-right="onClickRight"
>
  <template #right>
    <van-icon name="search" size="18" />
  </template>
</van-nav-bar>
<div id="content">
    <template v-if="active === 'index'">
        <Index />
    </template>
    <template v-else-if="active === 'team'">
        <Team />
    </template>
    <template v-else-if="active === 'profile'">
        <Profile />
    </template>
</div>

<van-tabbar v-model="active" @change="onChange">
  <van-tabbar-item icon="home-o" name="index">主页</van-tabbar-item>
  <van-tabbar-item icon="search" name="team">队伍页</van-tabbar-item>
  <van-tabbar-item icon="friends-o" name="profile">个人</van-tabbar-item>
</van-tabbar>


</template>

<script setup lang="ts">
import { showToast } from 'vant';
import { ref } from 'vue';
import Index from '../pages/Index.vue';
import Team from '../pages/Team.vue';
import Profile from '../pages/Profile.vue';
    const onClickLeft = () => alert('返回');
    const onClickRight = () => alert('按钮');
    const active = ref("index");
    const onChange = (index: string) => showToast(`标签 ${index}`);
</script>