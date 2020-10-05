<template>
  <ion-page>
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>Photo Gallery</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-fab vertical="bottom" horizontal="center" slot="fixed">
        <ion-fab-button color="danger" @click="takePhoto()">
          <ion-icon :icon="camera"></ion-icon>
        </ion-fab-button>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<script>
import { camera, trash, close } from "ionicons/icons";

import {
  // IonCol,
  IonContent,
  IonFab,
  IonFabButton,
  // IonGrid,
  IonHeader,
  IonIcon,
  // IonImg,
  IonPage,
  // IonRow,
  IonTitle,
  IonToolbar,
} from "@ionic/vue";

import { usePhotoGallery } from "@/composables/usePhotoGallery";

export default {
  name: "Tab2",
  components: {
    // IonCol,
    IonContent,
    IonFab,
    IonFabButton,
    // IonGrid,
    IonHeader,
    IonIcon,
    // IonImg,
    IonPage,
    // IonRow,
    IonTitle,
    IonToolbar,
  },
  setup() {
    const { takePhoto } = usePhotoGallery();

    return {
      camera,
      close,
      takePhoto,
      trash,
    };
  },
};
</script>