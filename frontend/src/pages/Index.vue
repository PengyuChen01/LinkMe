<template>
	<div class="page page-index">
		<h1>欢迎来到 LinkMe</h1>
		<p>连接团队与人才，快速开始你的项目。</p>
		<van-button type="primary" block @click="onClick">开始使用</van-button>
	</div>
</template>

<script setup lang="ts">
import { showToast } from 'vant';

const onClick = () => {
	showToast({ type: 'success', message: '欢迎来到 LinkMe' });
};
</script>

<style scoped>
.page { padding: 1.25rem; }
.page-index h1 { margin: 0 0 0.5rem; }
.page-index p { color: rgba(255,255,255,0.8); margin-bottom: 1rem; }
</style>
