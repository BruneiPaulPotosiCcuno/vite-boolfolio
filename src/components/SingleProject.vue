<script>
export default {
    name: 'SingleProject',
    props: {
        projectDetails: Object
    }
}
</script>
<template>
    <div class="col">
        <div class="card my-3">
                <div class="card-body">
                    <div>
                        <strong>Tipo:{{ projectDetails.type_id }}</strong>
                    </div>
                    <h5 class="card-title">{{projectDetails.name}}</h5>
                    <p class="card-text">{{ projectDetails.summary }}</p>
                </div>
            </div>
    </div>
</template>
<style scoped lang = "scss">
</style>