<template>
    <div class="item-wrap">
        <div class="item">
            <img :src="url" :alt="desc">
            <p>{{ desc }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Category',
    data() {
        return {}
    },
    props: ["url", "desc"]

}
</script>

<style>
.category-wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

.category > p {
    font-family: "Hilti Roman",Arial,Verdana,sans-serif;
    font-size: 18px;
    margin-bottom: 20px;
}

.category > h2 {
    font-size: 26px;
    padding-bottom: 3px;
}

.category-wrap > * {
    flex-basis: calc(1/4*100% - 10px);
    margin-bottom: 10px;
}

.item-wrap {
    text-align: center;
    border: 1px solid #d1d1d1;
    border-radius: 3px;
}


.item {
    height: 200px;
    padding: 10px;
}

.item img {
    max-height: 150px;
}
</style>