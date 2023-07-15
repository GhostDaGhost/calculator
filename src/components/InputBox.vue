<template>
    <div class="inputbox_container">
        <input class="inputbox" :value="currentEquation">
    </div>
</template>

<script lang="ts">
    export default {
        name: 'InputBox',
        data() {
            return {
                currentEquation: '0'
            }
        },
        methods: {
            modifyEquation (letterToAppend: string = '1'): void {
                this.currentEquation += letterToAppend;
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit LESS to this component only -->
<style scoped lang="less">
    @import '../styles/InputBox.less';
</style>
