<template>
    <div class="start">
        <h3>Найди меня<br> в магазине</h3>
        <span>
            Просто отсканируй код!
        </span>
        <div class="start-ellips-1"></div>
        <div style="text-align: center;">
            <img src="aks-2.png" class="start-aks-2"/>
        </div>
        
        <div class="button-row">
            <Button label="Камера" @click="$emit('change', 'camera')"/>
            <Button label="Поиграть" outline href="https://app.fabble.io/prototype/cc07eb"/>
        </div>
    </div>
</template>

<script>
import Button from './Button';
export default {
    components: {
        Button,
    }
}
</script>

<style scoped>
.start{
    color: white;
}
.start-ellips-1{
    width: 812px;
    height: 812px;
    background: #02903A;
    position: absolute;
    z-index: -10;
    top: -500px;
    left: -200px;
    border-radius: 50%;
}
.start-aks-2{
    margin: 0 auto;
    height: 400px;
    pointer-events: none;
}
</style>