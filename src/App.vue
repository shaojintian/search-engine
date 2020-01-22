<template>
	<div class="search-engine">
		<logo />
		<search-engine-input />
	</div>
</template>

<script lang="ts">
import Vue from 'vue'
import searchEngineInput from './components/search-engine-input.vue'
import logo from './components/logo.vue'
export default Vue.extend({
	components: { searchEngineInput, logo }
})
</script>

<style></style>
