<template>
    <ion-page>
        <ion-header>
            <ion-toolbar color="success">
                <ion-title>Login</ion-title>
            </ion-toolbar>
        </ion-header>

        <ion-content>
            <ion-item>
                <ion-label position="floating">Email</ion-label>
                <ion-input v-model="email"></ion-input>
            </ion-item>
            <ion-item>
                <ion-label position="floating">Password</ion-label>
                <ion-input type="password" v-model="password"></ion-input>   
            </ion-item>
            <ion-button expand="block" color="danger" @click="login">Login</ion-button>
        </ion-content>

        <ion-footer></ion-footer>
    </ion-page>
</template>

<script>
import {
    IonPage,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonFooter,
    IonItem,
    IonLabel,
    IonInput,
    IonButton
} from '@ionic/vue'
import { defineComponent } from 'vue'
import axios from 'axios';
export default defineComponent({
    data(){
        return {
            email: '',
            password: ''
        }
    },
    components: {
        IonPage,
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonFooter,
        IonItem,
        IonLabel,
        IonInput,
        IonButton
    },
    methods: {
        login(){
            // perintah ngecek user password
            // jika user password valid
            // this.$router.push("/kelas")
            // jika tidak valid
            // tetap di halaman login
           axios.post("http://3.234.139.56/api/login",{
                "email": this.email,
                "password": this.password
            })
            .then(response => {
                if(response.data.is_login){
                    localStorage.setItem("user_id",response.data.user_id)
                    this.$router.push("/kelas")
                }
            });
        }
    }
})
</script>

<style scoped>
</style>