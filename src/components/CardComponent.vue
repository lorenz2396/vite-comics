<script>
export default {
    data(){
        return{

        }
    },
    props:{
        img: String,
        title: String,
    }
}
</script>

<template>

    <div class="card">

        <div class="img-container">
                <img :src="img" :alt="title">
        </div>

        <h3 class="card-title"> 
            {{ title }}
        </h3>

    </div>

</template>

<style lang="scss" scoped>
.card{
    max-width: calc((100% - 10px*6) / 6);
    display: flex;
    align-items: center;
    justify-content: flex-start;
    flex-direction: column;
    margin: 5px;
    flex-shrink: 1;
    flex-grow: 1;
    .img-container{
        width: 80%;

        img{
            display: block;
            width: 100%;
            aspect-ratio: 8 / 10;
        }
    }

    h3{
        width: 100%;
        text-align: center;
        text-overflow: ellipsis;
        overflow: hidden;
        color: white;
    }
}
</style>