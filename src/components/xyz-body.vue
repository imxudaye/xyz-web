<template>
    <div>
        <el-checkbox-group v-model="checkedCities" @change="handleCheckedCitiesChange">
            <el-checkbox v-for="artType in artTypes" :label="artType" :key="artType"></el-checkbox>
        </el-checkbox-group>
        <el-button @click="drawer = true" type="primary" style="margin-left: 16px;">
            点我打开
        </el-button>
        <div id="ds">
        <el-drawer id="drawer"
                title="我是标题"  :show-close="false"
                :visible.sync="drawer"
                :direction="direction">
            <login></login>
        </el-drawer>
        </div>
    </div>
</template>

<script>
    import Login from "./login";
    const cityOptions = ['上海', '北京', '广州', '深圳'];
    export default {
        name: "xyz-body",
        components: {Login},
        data() {
            return {
                checkedCities:[],
                artTypes: cityOptions,
                isIndeterminate: true,
                drawer: false,
                direction: 'ltr',
            }

        },
        methods: {
            handleCheckedCitiesChange(value){
                let checkedCount = value.length;
                this.isIndeterminate = checkedCount > 0 && checkedCount < this.artTypes.length;
                if(!this.checkedCities.find(value)){
                    this.checkedCities.push(value);
                }
                alert(this.checkedCities)
            },
        }
    }
</script>

<style scoped>
#drawer{
    text-align: center;
    line-height: 160px;
    border-radius: 4px;
    font-size: small;
    box-shadow: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04);
}
    #ds{
        background-color: #333333;
    }

</style>