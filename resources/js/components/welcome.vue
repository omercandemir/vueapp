<template>
    <div class="marmara">
        Hoşgeldin <b> {{ isim }} </b> <br>
        Yeteneklerin: <b v-for="(skill, i) in skills" :key="i">{{ skill }}, </b> <br>
        Yaşınız <b> {{ yas }} </b>, 
        <span v-if="yas<18"> siteye kayıt olabilmek için 18 yaşından büyük olmalısınız.</span>
        <span v-if="yas>=18"> siteye kayıt olabilirsiniz.</span><br><br>
        <div class="text-center">

            <button @click="ageInfo" class="btn btn-success">Yaşım Alert</button><br><br>

            <button v-on:click="counter +=1" class="btn btn-primary">Tıkla</button><br>
            <p><b>{{ counter }}</b></p><br> <!-- Data Counter -->

            <button @click="yasArttir" class="btn btn-danger">Yaşı Arttır</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isim: 'Ömer',
            yas: 17,
            skills : ['php', 'laravel', 'vue'],
            counter: 0,
        }
    },
    methods: {
        ageInfo(){
            alert(this.yas)
        },
        yasArttir(){
            this.yas = this.yas+1
        },

    },
}
</script>

<style>
.marmara {
    margin-left: 15px;
    margin-top: 10px;
}
</style>