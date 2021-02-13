<template>
<div class="row justify-content-center">
    <div class="col-lg-2">
        <div class="media text-left">
            <div class="form-check">
                <input class="form-check-input" type="checkbox" value="" id="" @click="toggleTugas(tugasSaya)">
                <label class="form-check-label item-tugas" v-bind:class="{'item-tugas-selesai':tugasSaya.isDone}" for="">
                       {{tugasSaya.namaTugas}}
                </label>
            </div>
        </div>
    </div>
    
    <div class="col-lg-2">
        <div class="media text-left">
            <p class="item-tugas" v-bind:class="{'item-tugas-selesai':tugasSaya.isDone}"> {{tugasSaya.kategori}}
            </p>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "ItemTodo",
    props: ["tugasSaya"]
}
</script>

<style scoped>

</style>