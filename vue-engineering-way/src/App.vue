
<script setup>
import { ref } from 'vue';

const goodsList = ref([
		{ id: 101, name: 'biangbiang面', price: 13 },
		{ id: 102, name: '葫芦头', price: 20 },
		{ id: 103, name: '冰峰', price: 2 },
		{ id: 104, name: '肉夹馍', price: 11 },
		{ id: 105, name: '羊肉泡馍', price: 18 }
	])

    const del = (i) => {
      if (window.confirm("确认删除吗？")) {
        goodsList.value.splice(i,1)
      }
    }
</script>

<template>
<table border="1" cellspacing="0" cellpadding="0">
  <caption>
    <h3>橱窗</h3>
  </caption>
  <thead>
    <tr>
      <th>商品名称</th>
      <th>商品价值</th>
      <th>操作</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(item, index) in goodsList">
      <th>{{ item.name }}</th>
      <th>{{ item.price }}</th>
      <th>
        <button @click="del(index)">删除</button>
      </th>
    </tr>
  </tbody>
  <tfoot v-if="goodsList.length === 0">
			<tr>
				<td colspan="3">暂无数据啦</td>
			</tr>
		</tfoot>
</table>
</template>


<style lang="scss">
table{
  width: 500px;
  margin: 150px auto;
  text-align: center;
  font-family: 'Courier New', Courier, monospace;

		tr {
			height: 40px;
		}

		tfoot {
			height: 100px;
		}
}

</style>