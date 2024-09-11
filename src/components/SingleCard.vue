<script>
export default {
    props:{
        card: Object
    }   
}
</script>


<template>
    <div class="col-2 py-5 my-bg text-center ">
        <div class="card">
            <img :src="card.thumb" class="card-img-top" :alt="card.series">
            <div class="card-body">
                <p class="card-text">{{ card.type.toUpperCase() }}</p>
            </div>
        </div>  
    </div>
</template>

<style lang="scss" scoped>
.card{
    border:none;
    text-align:start;
    img{
        height:250px;
        object-fit:cover;
    }
    .card-body{
        background-color:#1C1C1C;
        color:white;
        padding-left:0;
    }
}
</style>