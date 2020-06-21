<template>
    <div class="bonus">
        <h3>Ура!<br> Ты получишь<br> бонусы!</h3>
        <div class="bonus-ellips-1"></div>
        <img class="bonus-bonuses-1" src="bonuses-1.png" />
        <div style="text-align: right;">
            <img src="aks-3.png" class="bonus-aks-3"/>
        </div>
        
        <div class="button-row">
            <Button label="Получить!" outline  @click="$emit('change', 'sale')"/>
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
.bonus{
    color: white;
}
.bonus-ellips-1{
    width: 812px;
    height: 812px;
    background: #02903A;
    position: absolute;
    z-index: -10;
    top: -500px;
    left: -200px;
    border-radius: 50%;
    z-index: -20;
}
.bonus-aks-3{
    height: 400px;
    margin-right: -40px;
}
.bonus-bonuses-1 {
    position: absolute;
    height: 100vh;
    top: -30vh;
    right: -100px;
    z-index: -10;
    
}
</style>