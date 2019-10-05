<template>
    <v-navigation-drawer color="grey lighten-5" floating right clipped app permanent>
      <v-container>
        <v-card>
          <v-card-title>
            <v-spacer></v-spacer>
            <v-icon>more_horiz</v-icon>
          </v-card-title>
          <v-divider></v-divider>
          <v-list-item>
            <!-- <v-list-item-content> -->
              <v-text-field height="50px" solo flat placeholder="Buscar" append-icon="search"></v-text-field>
            <!-- </v-list-item-content> -->
          </v-list-item>
          <v-divider></v-divider>
          <v-list-item>
            <v-list-item-content>
              <div class="questrial caption font-weight-bold blue--text">Amigos</div>
            </v-list-item-content>
            <v-list-item-action>
              <div class="questrial caption font-weight-bold grey--text" >Agregar</div>
            </v-list-item-action>
          </v-list-item>
          <template v-for="item in friends">
            <ChatUser :user="item"/>
          </template>
           <v-divider></v-divider>
          <v-list-item>
            <v-list-item-content>
              <div class="questrial caption font-weight-bold blue--text">Colegas</div>
            </v-list-item-content>
            <v-list-item-action>
              <div class="questrial caption font-weight-bold grey--text" >Agregar</div>
            </v-list-item-action>
          </v-list-item>
          <template v-for="item in colleagues">
            <ChatUser :user="item"/>
          </template>
           <v-divider></v-divider>
          <v-list-item>
            <v-list-item-content>
              <div class="questrial caption font-weight-bold blue--text">CLUBS</div>
            </v-list-item-content>
            <v-list-item-action>
              <div class="questrial caption font-weight-bold grey--text" >Agregar</div>
            </v-list-item-action>
          </v-list-item>
          <template v-for="item in clubs">
            <ChatUser :user="item"/>
          </template>

          
        </v-card>
      </v-container>
    </v-navigation-drawer>
</template>

<script>
import ChatUser from '../components/ChatUser/ChatUser'
export default {
  components: {
    ChatUser
  },
  data(){
    return {
      friends: [
        { name: 'Angel Sofia Sanchez', avatar: require('../assets/avatars/1.png'), online: true },
        { name: 'Juan Sebastian Sanchez', avatar: require('../assets/avatars/20.jpeg'), online: true },
        { name: 'Ana Maria Lugo Ramirez', avatar: require('../assets/avatars/17.jpg'), online: false },
        { name: 'Alejandro Nuñez', avatar: require('../assets/avatars/18.jpeg'), online: true },
        { name: 'Roberto Cerquera', avatar: require('../assets/avatars/19.jpeg'), online: false },
      ],
      colleagues: [
        { name: 'Carlos Zambrano', avatar: require('../assets/avatars/6.png'), online: false },
        { name: 'Ligia Farid Lugo', avatar: require('../assets/avatars/7.png'), online: false },
        { name: 'Cachi Ramirez', avatar: require('../assets/avatars/8.png'), online: true },
        { name: 'Claudia Trujillo', avatar: require('../assets/avatars/9.png'), online: false },
        { name: 'David Felipe Sanchez', avatar: require('../assets/avatars/10.png'), online: true },
      ],
      clubs: [
        { name: 'Cindy', avatar: require('../assets/avatars/11.png'), online: true },
        { name: 'Carmen Vargas', avatar: require('../assets/avatars/12.png'), online: false },
        { name: 'Alejandra Losada', avatar: require('../assets/avatars/13.png'), online: true },
        { name: 'Valentina Rojas', avatar: require('../assets/avatars/14.png'), online: true },
        
      ]
    }
  }
}
</script>

<style>

</style>
