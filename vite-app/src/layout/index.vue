<template>
    <div class="layout">
        <Menu title="我想穿一条裤子"></Menu>
        <div class="layout-right">
            <Header></Header>
            <Content></Content>
        </div>
    </div>
</template>

<script setup lang="ts">
import Menu from './Menu/index.vue';
import Header from './Header/index.vue';
import Content from './Content/index.vue';
</script>
<style lang="less" scoped>
.layout {
    display: flex;
    height: 100%;
    overflow: hidden;

    &--right {
        flex: 1;
    }
}
</style>