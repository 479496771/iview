<template>
    <div>
        <Logi v-if="callbackdata.send.length > 0" :listnub="logisticsData"></Logi>

    </div>
</template>

<script>
    import Logi from '@path/components/orderListBtn/Logistics.vue';
    export default {
        components:{
            Logi
        },
        data(){
            return{
                logisticsData:{
                    weid:''
                },
            };
        },
        props: {
            callbackdata: {
                type: Object,
                default: {}
            }
        },
        name: 'eighth',
        mounted(){
            this.logisticsData.weid = this.callbackdata.weid;
        }

    };
</script>

<style scoped>

</style>