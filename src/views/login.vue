<template>
<ion-page>
    <ion-header>
        <ion-toolbar color="success">
            <ion-title> login </ion-title>
        </ion-toolbar>
    </ion-header>
    <ion-content>
        <ion-item>
            <ion-label position="floating"> email </ion-label>
            <ion-input> </ion-input>
        </ion-item>
    <ion-item>
                <ion-label position="floating"> password </ion-label>
                <ion-input type="password"> </ion-input>
                </ion-item>
     <ion-button expand="block"> login </ion-button>
            </ion-content>
    <ion-footer> </ion-footer>
</ion-page>

</template>

<script>
import {
    IonPage,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonLabel,
    IonItem,
    IonInput,
    IonButton,
    IonFooter
} from '@ionic/vue'
import { defineComponent } from 'vue'

export default defineComponent ({
        components: {
            IonPage,
            IonHeader,
            IonToolbar,
            IonTitle,
            IonContent,
            IonLabel,
            IonItem,
            IonInput,
            IonButton,
            IonFooter
        }
    }
)
</script>

<style scoped> </style>