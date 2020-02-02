<template>
  <div class="search-engine-input">
    <el-row :span="24">
      <el-col :span="23">
        <el-autocomplete v-model="state"
                         :fetch-suggestions="querySearchAsync"
                         placeholder="请输入内容"
                         @select="handleSelect"></el-autocomplete>
      </el-col>
      <el-col :span="1">
        <el-button type="primary"
                   icon="el-icon-search">搜索</el-button>
      </el-col>
    </el-row>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'search-engine-input',
  data(): iData {
    return {
      items: [],
      state: '',
      timeout: 0
    }
  },
  methods: {
    loadAll() {
      return [{ value: '教父' }, { value: '肖申克的救赎' }]
    },
    querySearchAsync(queryString: String, cb: any) {
      let items = this.items
      let results:Array<any> = queryString
        ? items.filter(this.createStateFilter(queryString))
        : items

      cb(results)
      //console.log(results)
      return
    },
    createStateFilter(queryString: String): any {
      return (state: any) => {
        return state.value.toLowerCase().indexOf(queryString.toLowerCase) === 0
      }
    },
    handleSelect(item: String) {
      console.log(item)
    }
  },
  mounted() {
    this.items = this.loadAll()
  }
})
interface iData {
  items: any
  state: any
  timeout: number
}
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
