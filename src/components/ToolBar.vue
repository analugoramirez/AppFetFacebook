<template>
    <v-app-bar dense clipped-left clipped-right color="green darken-2" dark app>
      <v-toolbar-title  class="headline text-uppercase">
         <img src="../assets/avatars/LogoFET.png" height="50" width="200" alt="avatar">
      </v-toolbar-title>
      <v-toolbar-items>
        <v-btn text class="questrial text-none font-weight-bold">Inicio</v-btn>
        <v-btn text class="questrial text-none font-weight-bold">Buscar amigos</v-btn>
      </v-toolbar-items>
      <v-spacer></v-spacer>
        <v-text-field  append-icon="search" class="mt-8 questrial" label="Buscar" rounded solo light></v-text-field>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn icon><v-icon color="black lighten-4">supervisor_account</v-icon></v-btn>
        <v-btn icon><v-icon color="black lighten-4">fa-comments</v-icon></v-btn>
        <v-btn icon><v-icon color="black lighten-4">notifications</v-icon></v-btn>
        <v-btn icon><v-icon color="black lighten-4">help</v-icon></v-btn>
        
        <v-avatar class="mt-2" :size="30">
          <img src="../assets/avatars/16.jpeg" alt="avatar">
        </v-avatar>
      </v-toolbar-items>
    </v-app-bar>
</template>

<script>
export default {

}
</script>

<style>
.v-text-field.v-text-field--solo .v-input__control{
  min-height: 22px
}
.v-text-field.v-text-field--solo .v-input__append-inner, .v-text-field.v-text-field--solo .v-input__prepend-inner{
  margin-bottom: 5px
}
</style>
