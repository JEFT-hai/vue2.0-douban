<template>
    <div class="main">
        <headers></headers>
        <div class="content">
            <router-view></router-view>
        </div>
        <footers></footers>
    </div>
</template>
<script>
    import headers from "./view/header";
    import footers from "./view/footer";

    export default {
        components :{
            headers,
            footers
        }
    }
</script>
<style>
</style>