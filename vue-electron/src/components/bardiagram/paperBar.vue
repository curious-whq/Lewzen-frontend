<template>
    <div class="card">
        <div class="card-header">Paper Size</div>
        <div class="card-item">
            <el-select v-model="value" placeholder="请选择">
                <el-option
                        v-for="item in options"
                        :key="item.value"
                        :label="item.label"
                        :value="item.value">
                </el-option>
            </el-select>
        </div>
    </div>
</template>

<script>
    export default {
        name: "paperBar",
        data(){
            return{
                options: [{
                    value: '选项1',
                    label: 'A4(210mm*297mm)'
                }, {
                    value: '选项2',
                    label: 'A3(297mm*420mm)'
                }],
                value:'',
            }
        }
    }
</script>

<style scoped>
    .card{
        padding: 10px;
        border-bottom: #E1E1E1 solid 1px;
        text-align: left;
    }
    .card-header{
        font-weight: 600;
        font-size: 12px;
    }
    .card-item{
        padding-top: 7px;
        font-size: 10px;
    }
    .bottom-item{
        padding-bottom: 2px;
        font-size: 10px;
    }
    .el-checkbox__label{
        font-size:10px;
    }
    .clear{
        clear: both;
    }
    .card-left{
        float: left;
        /*background-color: #42b983;*/
        line-height: 30px;
        width: 70%;
        height: 30px;
    }
    .card-left-item{
        float: left;
        /*background-color: #42b983;*/
        line-height: 30px;
        width: 60%;
        height: 30px;
        font-size: 14px;
        color: gray;
        padding-left: 24px;
    }

    .card-left-left{
        float: left;
        /*background-color: #42b983;*/
        line-height: 30px;
        width: 30%;
        height: 30px;
    }
    .card-midden{
        float: left;
        /*background-color: #9a6e3a;*/
        line-height: 30px;
        width: 40%;
        height: 30px;
    }
    .card-right{
        float: right;
        align-items: center;
        /*background-color: #795da3;*/
        /*padding-left: 20px;*/
        width:30%;
        height: 30px;
    }
</style>