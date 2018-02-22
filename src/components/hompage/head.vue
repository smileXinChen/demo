<template>
    <div id="menu-head">
        <Row class="head">
            <Header :style="{position: 'fixed', width: '100%'}">
                <Menu mode="horizontal" theme="dark" active-name="1">
                        <div class="layout-logo">UI框架练习</div>
                        <div class="layout-nav">
                            <Menu mode="horizontal" :theme="theme1" active-name="1">
                                <menu-item name="1">
                                    <Icon type="ios-paper"></Icon>
                                    内容管理
                                </menu-item>
                                <menu-item name="2">
                                    <Icon type="ios-people"></Icon>
                                    用户管理
                                </menu-item>
                                <menu-item name="3">
                                    <Icon type="settings"></Icon>
                                    综合设置
                                </menu-item>
                                <menu-item name="4">
                                    <Icon type="settings"></Icon>
                                    综合设置
                                </menu-item>
                            </Menu>
                        </div>
                        <div><i-input v-model="value4" icon="ios-search" placeholder="搜索框" style="width: 200px"></i-input></div>
                        <div>22222222</div>
                </Menu>
            </Header>
        </Row>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                theme1: 'light',
                value4: ''
            }
        },
        methods: {
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#menu-head{
  height:60px;
  line-height:60px;
  box-sizing:border-box;
  border-bottom:1px solid #d0d3d8;
  box-shadow: 0 5px 0 0 #d0d3d8;
  background-color:#F4F6FC;
}
.head_title{
  border-right:1px solid #000;
}
.head_con{
  border-right:1px solid #000;
  margin:0 auto;
}
.ivu-dropdown-rel a{
  color:#495060;
}
.ivu-menu-light.ivu-menu-horizontal .ivu-menu-item-active, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-item:hover, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-submenu-active, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-submenu:hover,.ivu-menu-light.ivu-menu-horizontal .ivu-menu-item:hover, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-submenu-active, .ivu-menu-light.ivu-menu-horizontal .ivu-menu-submenu:hover{
  color:#fc923f;
  border-bottom:2px solid #fc923f;
}
.ivu-menu-light{
  background-color:transparent;
}
.ivu-col-span-12{
  display: inline-block;
  vertical-align: top;
  text-align: center;
}
.layout-logo{
    width: 150px;
    height: 60px;
    border-radius: 3px;
    float: left;
    color:#495060;
}
.layout-nav{
    width: 520px;
    margin: 0 auto;
    margin-left:60px;
}
#menu-head .ivu-layout-header,#menu-head .ivu-menu-dark{
    background-color:transparent;
}
.ivu-menu-dark.ivu-menu-horizontal .ivu-menu-item, .ivu-menu-dark.ivu-menu-horizontal .ivu-menu-submenu{
    color:#666666;
}
.ivu-menu-horizontal .ivu-menu-item, .ivu-menu-horizontal .ivu-menu-submenu{
    padding:0 10px;
}
</style>
