<template>
    <div>
        <h3>Я расскажу тебе об Аксиках</h3>
        <video ref="video" autoplay="autoplay" class="aks-video" controls="controls" poster="video.jpeg">
            <source src="video.mp4" type='video/mp4;'>
        </video>
        <div class="button-row">
            <Button label="Камера" @click="$emit('change', 'camera')"/>
            <Button label="Далее" @click="$emit('change', 'enter')" outline/>
        </div>
    </div>
</template>

<script>
import Button from './Button';
export default {
    components: {
        Button,
    },
    mounted() {
        this.$refs['video'].play()
    }
}
</script>

<style scoped>
.aks-video {
    margin: 0 -40px;
    width: calc(100% + 80px);
}
</style>