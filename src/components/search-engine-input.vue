<template>
	<div class="search-engine-input">
		<el-row :span="24">
			<el-col :span="23">
				<el-input
					v-model="input"
					placeholder="请输入内容"
					autofocus="true"
				></el-input>
			</el-col>
			<el-col :span="1">
				<el-button type="primary" icon="el-icon-search">搜索</el-button>
			</el-col>
		</el-row>
	</div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
	name: 'search-engine-input',
	data() {
		return {
			input: ''
		}
	}
})
</script>

<style>
.search-engine-input {
	width: 50%;
	position: absolute;
	left: 30%;
	top: 50%;
	margin: -100px 0 0 -100px;
}
</style>
