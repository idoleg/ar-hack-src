<template>
    <div class="sale">
        <h3>Скидка<br> от Аксика!</h3>
        <div class="sale-ellips-1"></div>
        <img class="sale-1" src="sale-1.png" />
        <p style="font-size: 20px;line-height: 24px;padding: 10px 0;">
            на любую пасту<br>
            SPLAT special
        </p>
        <p style="font-size: 14px;line-height: 14px;padding: 5px 0;">
            * не забудьте предьявить<br>
            на кассе карту лояльности
        </p>
        <p style="font-size: 14px;line-height: 14px;padding: 5px 0;">
            * скидка возвратится на карту лояльности<br>
            в виде бонусов в течении 5 дней
        </p>
        <div style="text-align: right;">
            <img src="aks-4.png" class="sale-aks-4"/>
        </div>
        
        <div class="button-sale">
            <Button label="О товаре" @click="$emit('change', 'item')"/>
        </div>
        <div style="margin-top: 100px;position:relative;">
            <p style="color: #02903A; font-size: 14px;line-height: 14px;">
                Второй Аксик удвоит скидку!
            </p>
            <div style="text-align: right;">
                <img src="aks-5.png" class="sale-aks-5"/>
            </div>
            <h3 style="color: #EB261D;line-height: 36px;font-size: 36px;">
                Скидка <br>
                от Аксика <br>
                на зубные щетки SPLAT
            </h3>
            <img class="sale-2" src="sale-2.png" />
            <div style="width:50%; padding-top:20px;">
                <Button label="Искать!" outline @click="$emit('change', 'camera')"/>
            </div>
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
.sale{
    color: white;
}
.sale-ellips-1{
    width: 812px;
    height: 812px;
    background: #02903A;
    position: absolute;
    z-index: -10;
    top: -350px;
    left: -200px;
    border-radius: 50%;
    z-index: -20;
}
.sale-aks-4{
    position: absolute;
    right: 0;
    top: 20px;
    height: 400px;
    pointer-events: none;
}
.sale-aks-5{
    position: absolute;
    right: -130px;
    top: -20px;
    pointer-events: none;

}
.button-sale{
    padding-top: 20px;
    width: 50%;
}
</style>