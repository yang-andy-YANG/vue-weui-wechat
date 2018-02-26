<template>
    <section class="login">
        <a href="javascript:;" class="weui-btn weui-btn_primary" @click.prevent="onClick">页面主操作 Normal</a>
        <a href="javascript:;" class="weui-btn weui-btn_disabled weui-btn_primary">页面主操作 Disabled</a>
        <a href="javascript:;" class="weui-btn weui-btn_default">页面次要操作 Normal</a>
        <a href="javascript:;" class="weui-btn weui-btn_disabled weui-btn_default">页面次要操作 Disabled</a>
        <a href="javascript:;" class="weui-btn weui-btn_warn">警告类操作 Normal</a>
        <a href="javascript:;" class="weui-btn weui-btn_disabled weui-btn_warn">警告类操作 Disabled</a>

        <div class="button-sp-area">
            <a href="javascript:;" class="weui-btn weui-btn_plain-default">按钮</a>
            <a href="javascript:;" class="weui-btn weui-btn_plain-default weui-btn_plain-disabled">按钮</a>
            <a href="javascript:;" class="weui-btn weui-btn_plain-primary">按钮</a>
            <a href="javascript:;" class="weui-btn weui-btn_plain-primary weui-btn_plain-disabled">按钮</a>
            <a href="javascript:;" class="weui-btn weui-btn_mini weui-btn_primary">按钮</a>
            <a href="javascript:;" class="weui-btn weui-btn_mini weui-btn_default">按钮</a>
            <a href="javascript:;" class="weui-btn weui-btn_mini weui-btn_warn">按钮</a>
        </div>
    </section>
</template>

<script>

    import {mapState,mapActions} from 'vuex'
    import weui from 'weui.js';

    export default {
        name: 'login',
        data() {
            return {
                userName:'',
                password:'',
                errorMsg: ''
            }
        },

        computed: mapState(['userInfo']),

        mounted() {
            
        },

        methods: {
            ...mapActions(['getUserInfo']),
            onClick(){
                weui.alert('alert');
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
    @import '~@/style/link';
    @import '~@/style/mixin';
    @import '~@/style/flex.less';

    .login {
        .link.link-block {
            color: #000;
        }
    }
</style>
