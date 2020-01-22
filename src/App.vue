<template>
	<searchEngineInput />
</template>

<script lang="ts">
import Vue from 'vue'
import searchEngineInput from './components/search-engine-input.vue'
export default Vue.extend({
	components: { searchEngineInput }
})
</script>

<style>
.searchEngineInput{
    display: inline;
    vertical-align: middle;
}
</style>