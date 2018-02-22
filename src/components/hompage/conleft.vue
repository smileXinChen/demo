<template>
    <div class="con-left">
        <Layout :style="{minHeight: '100vh'}">
            <Sider collapsible :collapsed-width="78" v-model="isCollapsed">
                <Tabs>
                    <TabPane label=" 标签1" icon="social-apple">标签一</TabPane>
                    <TabPane label="Windows" icon="social-windows">标签二的内容</TabPane>
                    <TabPane label="Linux" icon="social-tux">标签三的内容</TabPane>
                </Tabs>
                <Menu active-name="1-2" theme="dark" width="auto" :class="menuitemClasses">
                    <menu-item name="1-1">
                        <Icon type="ios-navigate"></Icon>
                        <span>内容1</span>
                    </menu-item>
                    <menu-item name="1-2">
                        <Icon type="search"></Icon>
                        <span>内容2</span>
                    </menu-item>
                    <menu-item name="1-3">
                        <Icon type="settings"></Icon>
                        <span>内容3</span>
                    </menu-item>
                </Menu>
            </Sider>
            <Layout>
                <Content :style="{padding: '0 16px 16px'}">
                    <Breadcrumb :style="{margin: '16px 0'}">
                        <BreadcrumbItem>Home</BreadcrumbItem>
                        <BreadcrumbItem>Components</BreadcrumbItem>
                        <BreadcrumbItem>Layout</BreadcrumbItem>
                    </Breadcrumb>
                    <Card>
                        <div style="height: 600px">Content</div>
                    </Card>
                </Content>
            </Layout>
        </Layout>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                isCollapsed: false
            };
        },
        computed: {
            menuitemClasses: function () {
                return [
                    'menu-item',
                    this.isCollapsed ? 'collapsed-menu' : ''
                ]
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .con-left{
        height: 100%;
        width: 100%;
    }
    .menu-item span{
        display: inline-block;
        overflow: hidden;
        width: 69px;
        text-overflow: ellipsis;
        white-space: nowrap;
        vertical-align: bottom;
        transition: width .2s ease .2s;
    }
    .menu-item i{
        transform: translateX(0px);
        transition: font-size .2s ease, transform .2s ease;
        vertical-align: middle;
        font-size: 16px;
    }
    .collapsed-menu span{
        width: 0px;
        transition: width .2s ease;
    }
    .collapsed-menu i{
        transform: translateX(5px);
        transition: font-size .2s ease .2s, transform .2s ease .2s;
        vertical-align: middle;
        font-size: 22px;
    }
</style>
