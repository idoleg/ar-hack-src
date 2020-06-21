<template>
    <div class="item">
        <div style="color: white;">
            <h3>Информация о продукте</h3>
            <p style="line-height: 24px;font-size: 14px;">
                75 ml
            </p>
            <p style="line-height: 24px;font-size: 20px;">
                Зубная паста <br>
                SPLAT special
            </p>
        </div>
        
        <div style="padding-top:20px;margin-left:-40px;text-align: center;">
            <img src="item.png" class="item-1"/>
        </div>
        <div class="item-ellips-1"></div>
        
        <div style="position:relative;">
            <h3 style="font-weight: 600;font-size: 20px;line-height: 24px;">
                Интересный<br>
                факт от Аксика
            </h3>
            <div style="max-width: 200px;font-size: 12px;line-height:12px;color: #474B5F;">
                <p>Эмаль здоровых зубов полупрозрачна, ее цвет приближен к истинному цвету слоновой кости.<p>
                <br>
                <p>Очень часто поверхность зуба становится матовой и мутной.</p>
                <br>
                <p>Это происходит из-за адгезии пигменти-
                рованного зубного налета, резкого механического воздействия, демине-
                рализации эмали и образования меловых пятен.</p>
                <br>
                <p>Такой зуб нуждается
                в профессиональном лечении и дальнейшей профилактике</p>
            </div>
            <div style="text-align: right;">
                <img src="aks-6.png" class="item-aks-6"/>
            </div>
        </div>
        <div class="button-row">
            <Button label="Спросить у Аксика" outline href="https://app.fabble.io/prototype/cc07eb"/>
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
.item{
}
.item-ellips-1{
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
.item-aks-6{
    position: absolute;
    top:0px;
    right: -120px;
    height: 300px;
}
.bonus-bonuses-1 {
    position: absolute;
    height: 100vh;
    top: -30vh;
    right: -100px;
    z-index: -10;
    
}
</style>