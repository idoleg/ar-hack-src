<template>
    <a :class="{'button': !outline, 'button-outline': outline}" @click="$emit('click')" :href="href" target="_blank">
        {{label}}
    </a>
</template>

<script>

export default {
    props: {
        label: String,
        href: String,
        outline: Boolean,
    }
}
</script>

<style scoped>
.button {
    background: #EB261D;
    border-radius: 50px;
    color: white;
    display: block;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 40px;
    height: 40px;
    text-align: center;
    width: 100%;
    cursor: pointer;
    text-decoration: none;
}
.button-outline {
    border: 1px solid #02903A;
    box-sizing: border-box;
    border-radius: 50px;
    color: #02903A;
    display: block;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 40px;
    height: 40px;
    text-align: center;
    width: 100%;
    cursor: pointer;
    text-decoration: none;
}
</style>