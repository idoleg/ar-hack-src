<template>
    <div class="enter">
        <h3>Привет,<br> я Аксик!</h3>
        <span>
            я помогу тебе покупать<br> лучшие товары - выгодно!
        </span>
        <div class="enter-ellips-1"></div>
        <img src="card.png"/>
        <img src="aks-1.png" class="enter-aks-1"/>
        
        <div class="button-column">
            <Button label="Камера" @click="$emit('change', 'camera')"/>
            <Button label="Далее" outline @click="$emit('change', 'start')"/>
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
.enter{
    color: white;
}
.enter-ellips-1{
    width: 812px;
    height: 812px;
    background: #02903A;
    position: absolute;
    z-index: -10;
    top: -400px;
    left: -200px;
    border-radius: 50%;
}
.enter-aks-1{
    position: absolute;
    right: 0px;
    top: 200px;
    pointer-events: none;
}
</style>