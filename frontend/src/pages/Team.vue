<template>
	<div class="page page-team">
		<h2>团队</h2>

		<van-cell-group>
			<van-cell title="团队 A" label="5 位成员" is-link @click="open('团队 A')" />
			<van-cell title="团队 B" label="3 位成员" is-link @click="open('团队 B')" />
			<van-cell title="设计组" label="2 位成员" is-link @click="open('设计组')" />
		</van-cell-group>
	</div>
</template>

<script setup lang="ts">
import { showToast } from 'vant';

const open = (name: string) => {
	showToast(`${name} 已选择`);
};
</script>

<style scoped>
.page { padding: 1.25rem; }
.page-team h2 { margin: 0 0 1rem; }
</style>
