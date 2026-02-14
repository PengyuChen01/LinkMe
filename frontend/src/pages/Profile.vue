<template>
	<div class="page page-profile">
		<h2>个人资料</h2>

		<van-cell-group>
			<van-cell title="用户名" label="陈" />
			<van-cell title="邮箱" label="chen@example.com" />
		</van-cell-group>

		<div style="margin-top:1rem">
			<van-button block type="danger" @click="logout">退出登录</van-button>
		</div>
	</div>
</template>

<script setup lang="ts">
import { showToast } from 'vant';

const logout = () => {
	showToast('已退出登录');
};
</script>

<style scoped>
.page { padding: 1.25rem; }
.page-profile h2 { margin: 0 0 1rem; }
</style>
