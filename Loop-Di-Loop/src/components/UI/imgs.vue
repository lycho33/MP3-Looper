<template>
    <div class="images">
        <div class="iron-man">
            <img :src="getImageUrl(ironManPath)" alt="">
        </div>
        <div class="moon-container">
            <div class="moon">
                <img :src="getImageUrl(moonPath)" alt="">
                <Playlist />
            </div>
            <UrlInput />
        </div>
    </div>
</template>

<script>
import Playlist from '../models/Playlist.vue'
import UrlInput from '../models/UrlInput.vue'

export default {
    components: {
        Playlist,
        UrlInput,
    },
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
$width: 100%;

.images {
    display: flex;
    width: 100%;
    height: auto;
}

.iron-man {
    width: 30%;
    padding-left: 2%;
}

.moon-container {
    position: absolute;
    left: 50%;
    top: 30%;
}

.moon {
    display: flex;
    position: relative;
    width: $width;
    left: 7%;
}

.moon img {
    z-index: 1;
}

img {
    width: 90%;
    height: auto;
}

</style>