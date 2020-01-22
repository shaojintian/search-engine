<template>
	<el-input
		v-model="input"
		placeholder="请输入内容"
		autofocus="true"
	></el-input>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
	name: 'searchEngineInput',
	data() {
		return {
			input: ''
		}
	}
})
</script>

<style>
.el-input {
	width: 50%;
	position: absolute;
	left: 30%;
	top: 50%;
	margin: -100px 0 0 -100px;
}
</style>
