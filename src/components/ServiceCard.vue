<template>
    <div class="card-container rounded py-2">
        <div class="card-content">
            <div class="d-flex justify-space-between">
                <v-list-item>
                    <span class="font-weight-bold text-white">{{title}}</span>
                </v-list-item>
                <v-list-item>
                    <v-icon :icon="icon" color="red-darken-1"></v-icon>
                </v-list-item>
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'ServiceCard',
    props: {
        title: String,
        icon: String
    }
}
</script>

<style>
.card-container{
    width: 300px;
    height: 150px;
    background-color: rgb(197, 202, 233, 0.6);
}

</style>