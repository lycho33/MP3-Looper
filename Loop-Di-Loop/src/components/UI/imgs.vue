<template>
    <div>
        <h3>Images</h3>
        <img :src="getImageUrl(ironManPath)" alt="" class="">
        <img :src="getImageUrl(moonPath)" alt="">
    </div>
</template>

<script>

export default {
    data() {
        return {
            ironManPath: 'ironMan.jpg',
            moonPath: 'fullMoon.jpg'
        }
    },
    methods: {
        getURL() {
            return this.ironManPath;
        }
    },
    setup() {
        const getImageUrl = (name) => {
                return new URL(`../../assets/images/${name}`, import.meta.url).href
            }
        return { getImageUrl }
    }
}
</script>

<style scoped>
h3 {
    color: white;
}
</style>