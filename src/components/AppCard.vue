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
        <img :src="comic.thumb" :alt="comic.series">
    </div>
</template>


<style scoped>
.row {
    width: 100%;
    height: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

}

.card {

    height: 10px;
    padding: 20px;
}
</style>