<template>
    <div>
        <h3>Images</h3>
        <img :src="getImageUrl(ironManPath)" alt="" class="">
    </div>
</template>

<script>
// import {ironMan} from '@../../assets/images/ironMan.jpg'

export default {
    data() {
        return {
            ironManPath: 'ironMan.jpg',
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