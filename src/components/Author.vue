<template>
    <div class="author_container">
        <div class="author">
            Created by Alex with <a class="hyperlink" href="https://vuejs.org/" rel="noopener noreferrer" target="_blank">Vue.js</a>
        </div>
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
