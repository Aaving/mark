<template>
  <div class="todo-header">
    <input v-model='head' @keyup.enter='add' type="number" placeholder="请输入头" /><br/><br>
    <input v-model='tail' @keyup.enter='add' type="number" placeholder="请输入尾" /><br/><br>
    <input v-model.number='group' @keyup.enter='add' type="number" placeholder="请输入组数" />
  </div>
</template>

<script>
import {nanoid} from 'nanoid'
  export default {
    data(){
      return{
        head:'',
        tail:'',
        group:''
      }
    },
    methods: {
      //添加todo
      add(){

        // 校验数据
        if(!this.num)return alert("输入不能为空")
        // 调用父组件函数传数据，这里this->Top组件
        this.receive({
          id:nanoid(),
          name:this.name,
          done:false
        } )

        // 清空输入
        this.name = ''
      }
    },
    props:['receive']
  };
</script>

<style>

/*header*/
.todo-header input {
  width: 562px;
  height: 28px;
  font-size: 14px;
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 4px 7px;
}

.todo-header input:focus {
  outline: none;
  border-color: rgba(82, 168, 236, 0.8);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 8px rgba(82, 168, 236, 0.6);
}

</style>
