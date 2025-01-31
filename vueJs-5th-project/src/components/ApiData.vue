<script>
export default {
    data() {
        return {
            isLoading: true,
            userData: null,
            error: null,
        }
    },
    methods: {
        fetchData() {
            setTimeout(() => {
                // this.userData = ["name", "Antor"],
                this.error = "Something went wrong",
                this.isLoading = false
            },2500)
        },
    },
    mounted() {
        this.fetchData()
    } ,
}
</script>

<template>
    <div class="loadingTime" v-if="isLoading">
        Data is Loading.....
    </div>
    <div class="loadingTime" v-else-if="userData">
        {{ userData }}
    </div>
    <div class="loadingTime" v-else>Error! {{ error }}</div>
</template>

<style scoped>
.loadingTime {
    color: red;
    align-items: center;
    font-size: 32px;
    justify-content: center;
    display: flex;
    margin-top: 50px;
}
</style>