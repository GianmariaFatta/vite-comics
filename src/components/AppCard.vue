<script>
export default {
    name: 'card',
    props: {
        comic: Object
    }
}

</script>

<template>
    <div class="comic-card">
        <div class="card">
            <img :src="comic.thumb" :alt="comic.series">
        </div>
        <h6>{{ comic.series }}</h6>
    </div>
</template>


<style scoped>
.card {
    height: 177px;
    overflow: hidden;
    cursor: pointer;
}

.comic-card {
    display: flex;
    flex-wrap: wrap;
    width: calc(100% / 6);
    height: 220px;
    padding: 25px;
}
</style>