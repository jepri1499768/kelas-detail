<template>
    <ion-page>  
    <ion-header>
    <ion-toolbar color="success"> 
        <ion-title>detail kelas </ion-title>
        </ion-toolbar>
        </ion-header>
        <ion-content>
            <ion-list>
                <ion-item> 
                    <ion-label> pertemuan 1 </ion-label> 
                    <ion-badge color="success" slot="end"> Hadir </ion-badge>
                    </ion-item> 
                 <ion-item> 
                    <ion-label> pertemuan 2 </ion-label> 
                    <ion-badge color="success" slot="end"> Hadir </ion-badge>
                    </ion-item> 
                 <ion-item> 
                    <ion-label> pertemuan 3 </ion-label> 
                    <ion-badge color="success" slot="end"> Hadir </ion-badge>
                    </ion-item> 
                 <ion-item> 
                    <ion-label> pertemuan 4 </ion-label> 
                    <ion-badge color="success" slot="end"> Hadir </ion-badge>
                    </ion-item> 
                 <ion-item> 
                    <ion-label> pertemuan 5 </ion-label> 
                    <ion-badge color="success" slot="end"> Hadir </ion-badge>
                    </ion-item> 

                    </ion-list> 
                    </ion-content>
        </ion-page>
</template>

<script>
import  { 
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonList,
        IonItem,
        IonLabel,
        IonBadge
} from '@ionic/vue' 
import { defineComponent } from 'vue'
    export default defineComponent({
        components: {
        IonHeader,
        IonToolbar,
        IonTitle,
        IonContent,
        IonList,
        IonItem,
        IonLabel,
        IonBadge
        }
    })
</script>

<style lang="scss" scoped>

</style>