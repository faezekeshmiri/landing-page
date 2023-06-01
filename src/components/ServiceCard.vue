<template>
    <div class="card-container rounded py-2 px-2">
        <div class="card-content">
            <div class="d-flex justify-space-between">
                <v-list-item>
                    <span class="font-weight-bold text-white">{{title}}</span>
                </v-list-item>
                <v-list-item>
                    <v-icon :icon="icon" color="red-darken-1"></v-icon>
                </v-list-item>
            </div>
            <div class="text-body-2 text-grey-lighten-2 px-4 text-left w-75">{{description}}</div>
        </div>
        <div class="card-link mx-4 my-4 text-subtitle-2 text-white">{{link}}</div>
    </div>
</template>

<script>
export default{
    name: 'ServiceCard',
    props: {
        title: String,
        icon: String,
        description: String,
        link: String
    }
}
</script>

<style>
.card-container{
    width: 320px;
    height: 150px;
    background-color: rgb(197, 202, 233, 0.6);
    position: relative;
}
.card-link{
    position: absolute;
    bottom: 0;
    border-bottom: 2px solid #E53935;
}
</style>