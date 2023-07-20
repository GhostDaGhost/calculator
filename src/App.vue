<template>
    <div class="outercontainer">
        <div class="innercontainer">
            <ButtonsAndInput/>
            <Author/>
        </div>
    </div>
</template>

<script lang="ts">
    import { Options, Vue } from 'vue-class-component';
    import Author from './components/Author.vue';
    import ButtonsAndInput from './components/ButtonsAndInput.vue';

    @Options({ components: { ButtonsAndInput, Author } })

    export default class App extends Vue {}
</script>

<style lang="less">
    @import 'styles/App.less';
</style>
