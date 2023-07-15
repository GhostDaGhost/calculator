<template>
    <div class="outercontainer">
        <div class="innercontainer">
            <InputBox/>
            <CalculatorButtons/>
            <Author/>
        </div>
    </div>
</template>

<script lang="ts">
    import { Options, Vue } from 'vue-class-component';

    import CalculatorButtons from './components/CalculatorButtons.vue';
    import InputBox from './components/InputBox.vue';
    import Author from './components/Author.vue';

    @Options({ components: { InputBox, CalculatorButtons, Author } })

    export default class App extends Vue {}
</script>

<style lang="less">
    @import 'styles/App.less';
</style>
