<template>
    <div class="images">
        <div class="iron-man">
            <img :src="getImageUrl(ironManPath)" alt="">
        </div>
        <div class="moon">
            <img :src="getImageUrl(moonPath)" alt="">
        </div>
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

<style scoped lang="scss">
$width: 61%;

.images {
    display: flex;
    width: 100%;
    height: auto;
}

.iron-man {
    width: 30%;
    padding-left: 2%;
}

.moon {
    position: absolute;
    top: 20%;
    width: $width;
    left: 49%;
}

img {
    width: 90%;
    height: auto;
}

</style>