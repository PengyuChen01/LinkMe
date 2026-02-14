
<template>
 <van-nav-bar
  title="标题"
  left-text="返回"
  right-text="按钮"
  left-arrow
  @click-left="onClickLeft"
  @click-right="onClickRight"
/>

</template>

<script setup lang="ts">

    const onClickLeft = () => alert('返回');
    const onClickRight = () => alert('按钮');
</script>