<template>
    <div>
        <div class="inputbox_container">
            <input class="inputbox" :value="currentEquation">
        </div>

        <div class="calcbutton_container">
            <div class="calcbutton operator" @click="clear()">C</div>
            <div class="calcbutton operator" @click="append('(')">(</div>
            <div class="calcbutton operator" @click="append(')')">)</div>
            <div class="calcbutton operator" @click="append('/')">/</div>

            <div class="calcbutton" @click="append('7')">7</div>
            <div class="calcbutton" @click="append('8')">8</div>
            <div class="calcbutton" @click="append('9')">9</div>
            <div class="calcbutton operator" @click="append('*')">*</div>

            <div class="calcbutton" @click="append('4')">4</div>
            <div class="calcbutton" @click="append('5')">5</div>
            <div class="calcbutton" @click="append('6')">6</div>
            <div class="calcbutton operator" @click="append('-')">-</div>

            <div class="calcbutton" @click="append('1')">1</div>
            <div class="calcbutton" @click="append('2')">2</div>
            <div class="calcbutton" @click="append('3')">3</div>
            <div class="calcbutton operator" @click="append('+')">+</div>

            <div class="calcbutton" @click="append('0')">0</div>
            <div class="calcbutton" @click="append(',')">,</div>
            <div class="calcbutton" @click="append('.')">.</div>
            <div class="calcbutton operator" @click="calculate()">=</div>
        </div>
    </div>
</template>

<script lang="ts">
    export default {
        name: 'ButtonsAndInput',
        data() {
            return {
                currentEquation: '',
                errorTimeout: null
            }
        },
        methods: {
            clear (): void {
                this.currentEquation = '';
                clearTimeout(this.errorTimeout);
            },

            append (letterToAppend: string = ''): void {
                this.currentEquation += letterToAppend;
                clearTimeout(this.errorTimeout);
            },

            calculate (): void {
                try {
                    const calculatedAnswer: number = eval(this.currentEquation);
                    this.currentEquation = calculatedAnswer;
                } catch (error) {
                    this.currentEquation = 'ERROR';
                    this.errorTimeout = setTimeout(() => {
                        this.currentEquation = '';
                        this.errorTimeout = null;
                    }, 1350);
                }
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit LESS to this component only -->
<style scoped lang="less">
    @import '../styles/Buttons.less';
    @import '../styles/InputBox.less';
</style>
