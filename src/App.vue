<template>
  <div id="app">
    <div>
      <span>姓名:</span>
      <input type="text" />
    </div>
    <div>
      <span>年龄:</span>
      <input type="number" />
    </div>
    <div>
      <span>性别:</span>
      <select >
        <option value="男">男</option>
        <option value="女">女</option>
      </select>
    </div>
    <div>
      <button >添加/修改</button>
    </div>
    <div>
      <table
        border="1"
        cellpadding="10"
        cellspacing="0"
      >
        <tr>
          <th>序号</th>
          <th>姓名</th>
          <th>年龄</th>
          <th>性别</th>
          <th>操作</th>
        </tr>
        <tr v-for="item in arr" :key="item.id">
          <th>{{item.id}}</th>
          <th>{{item.name}}</th>
          <th>{{item.age}}</th>
          <th>{{item.sex}}</th>
          <td>
            <button >删除</button>
            <button >编辑</button>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      arr:[{id:1,name:'chaochao',age:18,sex:'男'},
      {id:2,name:'qianqian',age:18,sex:'女'},
      {id:3,name:'lulu',age:18,sex:'男'},
      {id:4,name:'nannan',age:18,sex:'男'},
      {id:5,name:'wenwen',age:18,sex:'男'},
      ]
    }
  }
}
</script>
