<template>
    <div class="author_container">
        <span class="author">Created by Alex</span>
    </div>
</template>

<script lang="ts">
    import { Vue } from 'vue-class-component';

    export default class Author extends Vue {}
</script>

<!-- Add "scoped" attribute to limit LESS to this component only -->
<style scoped lang="less">
    @import '../styles/Author.less';
</style>
