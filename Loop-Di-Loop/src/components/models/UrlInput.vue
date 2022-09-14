<template>
    <div class="input-forms">
        <input type="text" placeholder="Enter YouTube URL">
        <select name="playlistNames" id="playlistNames">
            <option value="">Select Playlist</option>
        </select>
        <button>Add</button>
    </div>  
</template>

<script>
export default {
    
}
</script>

<style scoped>
* {
    font-family: 'Italiana', serif;;
}
.input-forms {
    display: flex;
    justify-content: center;
}

button {
    background: rgba(219, 75, 75, 0.83);
    border-radius: 5px;
    color: white;
}
</style>