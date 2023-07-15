<template>
    <div class="calcbutton_container">
        <div class="calcbutton_row">
            <button class="calcbutton operator" @click="calculate('C')">C</button>
            <button class="calcbutton operator" @click="calculate('(')">(</button>
            <button class="calcbutton operator" @click="calculate(')')">)</button>
            <button class="calcbutton operator" @click="calculate('/')">/</button>
        </div>

        <div class="calcbutton_row">
            <button class="calcbutton" @click="calculate('7')">7</button>
            <button class="calcbutton" @click="calculate('8')">8</button>
            <button class="calcbutton" @click="calculate('9')">9</button>
            <button class="calcbutton operator" @click="calculate('*')">*</button>
        </div>

        <div class="calcbutton_row">
            <button class="calcbutton" @click="calculate('4')">4</button>
            <button class="calcbutton" @click="calculate('5')">5</button>
            <button class="calcbutton" @click="calculate('6')">6</button>
            <button class="calcbutton operator" @click="calculate('-')">-</button>
        </div>

        <div class="calcbutton_row">
            <button class="calcbutton" @click="calculate('1')">1</button>
            <button class="calcbutton" @click="calculate('2')">2</button>
            <button class="calcbutton" @click="calculate('3')">3</button>
            <button class="calcbutton operator" @click="calculate('+')">+</button>
        </div>

        <div class="calcbutton_row">
            <button class="calcbutton" @click="calculate('0')">0</button>
            <button class="calcbutton" @click="calculate(',')">,</button>
            <button class="calcbutton" @click="calculate('.')">.</button>
            <button class="calcbutton operator" @click="calculate('=')">=</button>
        </div>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'CalculatorButtons',
        methods: {
            calculate (letterToAppend: string = '1'): void {
                this.$emit('modifyEquation', letterToAppend);
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit LESS to this component only -->
<style scoped lang="less">
    @import '../styles/Buttons.less';
</style>
