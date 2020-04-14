<template>
  <div class="hello">
    <el-table
        :data="tableData"
        style="width: 800px;margin:20px auto"
        :row-class-name="tabRowClassName">
        <el-table-column
        prop="id"
        label="序号"
        width="180">
        </el-table-column>
        <el-table-column
        prop="field"
        label="字段"
        width="180">
        </el-table-column>
        <el-table-column
        prop="descrip"
        label="描述">
        </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: 'interviewTest',
  data () {
    return {
       tableData: [{
          id: '1',
          field: 'typeName',
          descrip: '车名'
        },{
          id: '2',
          field: 'car.carload',
          descrip: '载重'
        },{
          id: '3',
          field: 'car.carLong*car.carWidth*car.carHeight',
          descrip: '载货体积'
        },{
          id: '4',
          field: 'startAddress',
          descrip: '始发地'
        },{
          id: '5',
          field: 'endAddress',
          descrip: '目的地'
        },{
          id: '6',
          field: 'hoursLength',
          descrip: '线路耗时'
        },{
          id: '7',
          field: 'distance',
          descrip: '线路距离'
        },{
          id: '8',
          field: 'price',
          descrip: '价格'
        },{
          id: '9',
          field: 'carTypeImage',
          descrip: '车辆图片链接'
        },{
          id: '10',
          field: 'usageCount',
          descrip: '使用次数'
        }]
    }
  },
  methods:{
    tabRowClassName({row,rowIndex}){
        let index = rowIndex + 1;
        if(index %2 == 0){
            return 'warning-row'
        }else{
            return 'success-row'
        }
    }
  }
}
</script>
<style>
.el-table .warning-row {
    background: rgb(255, 255, 255);
}

.el-table .success-row {
    background: #e1e6df;
}

</style>
