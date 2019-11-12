<template lang="html">
    <section :class="[panelClass,cname]">
        <h4>-{title}-</h4>
        <div></div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            panelClass:'panel',//默认的class名
        }
    },
    props:{
        cname:{
            type:String,
            default:''
        },
        title:{
            type:String,
            default:''
        },

    }
    
}
</script>

<style lang="scss">
//引入公共的panel样式
import "../../element.scss";
.panel{
    @include panel;//引入后的应用
}
</style>
