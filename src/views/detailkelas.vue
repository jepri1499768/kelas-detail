<template>
    <ion-page>
        <ion-header>
            <ion-toolbar color="success">
                <ion-buttons slot="start">
                    <ion-back-button></ion-back-button>
                </ion-buttons>
                <ion-title>Detail Kelas</ion-title>
            </ion-toolbar>
        </ion-header>

        <ion-content>
            <ion-list>
                <ion-item v-for="(item,id) in detailkelas" :key="id">
                    <ion-label>Pertemuan {{ item.pertemuan }}</ion-label>
                    <ion-badge color="success" 
                        slot="end">{{ item.status}}</ion-badge>
                </ion-item>
            </ion-list>
        </ion-content>
    </ion-page>
</template>

<script>
    import {
        IonHeader,
        IonToolbar,
        IonPage,
        IonTitle,
        IonContent,
        IonList,
        IonItem,
        IonLabel,
        IonBadge,
        IonButtons,
        IonBackButton
    } from '@ionic/vue'
    import { defineComponent } from 'vue'
    import axios from 'axios'
    export default defineComponent({
        data(){
            return {
                detailkelas: []
            }
        },
        components: {
            IonHeader,
            IonToolbar,
            IonPage,
            IonTitle,
            IonContent,
            IonList,
            IonItem,
            IonLabel,
            IonBadge,
            IonButtons,
            IonBackButton
        },
        mounted(){
            axios.post("http://3.234.139.56/api/detailkelas",{
                "user_id": localStorage.getItem("user_id"),
                "kelas_id": this.$route.params.id
            })
            .then(response => {
                this.detailkelas = response.data.data
            })
        }
    })
</script>

<style lang="scss" scoped>
</style>