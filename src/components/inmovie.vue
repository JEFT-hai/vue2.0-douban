<template>
    <div @mouseover="on" @mouseout="off">
        <router-link :to="{ name: 'details', params: { id: data.id }}"><div class="img"><img :src="data.images.large" alt=""></div></router-link>
            <div class="title" :class="{'inmovie-o':btn}">
                <router-link :to="{ path: 'details', params: { id: data.id }}"><h3>{{data.title}}</h3></router-link>
                <h4>{{data.original_title}}</h4>
                <span class="nums">评分:{{data.rating.average}}</span>
                <span class="year">上映时间:{{data.year}}</span>
            </div>
    </div>
</template>
<style lang="less">
.inmovie-o {
    bottom: 0px !important;
}
</style>
<script>
export default {
    props:{
      data: {
        type: Object
      }
    },
    data(){
        return {
            btn:false
        }
    },
    methods :{
        on () {
            this.btn = true;
        },
        off () {
            this.btn = false;
        }
    }
}
</script> 