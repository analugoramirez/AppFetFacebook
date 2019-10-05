<template>
    <v-card rounded outlined>
        <div>
            <v-list-item>
                <v-list-item-avatar>
                    <img :src="avatar3" alt="John">
                </v-list-item-avatar>
                <v-list-item-content class="mt-2">
                    <v-list-item-title class="subtitle questrial">Ana Maria Lugo</v-list-item-title>
                    <v-list-item-subtitle class="questrial caption blue--text">Colega</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                    <v-icon @click="">more_horiz</v-icon>
                </v-list-item-action>
            </v-list-item>
        </div>
        <!-- <v-container grid-list-xs fluid style="padding:10px"> -->
            <v-layout wrap>
                <v-flex v-for="n in 2" :key="n" xs6>
                    <v-card  flat tile>
                        <v-img
                        :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                        :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                        aspect-ratio="1"
                        class="grey lighten-2"
                        >
                        <template v-slot:placeholder>
                            <v-layout
                            fill-height
                            align-center
                            justify-center
                            ma-0
                            >
                            <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                            </v-layout>
                        </template>
                        </v-img>
                    </v-card>
                </v-flex>
                
            </v-layout>
        <!-- </v-container> -->
        <v-card-text>
            <div class="questrial body1 mb-4">{{lorem}}</div>
            <v-divider></v-divider>
            <v-layout class="py-4">
                
               <v-menu attach open-on-hover top offset-y min-width="200px">
                    <template v-slot:activator="{ on }">
                <v-flex v-on="on">
                    <v-layout>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/heavy-black-heart_2764.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/smiling-face-with-open-mouth-and-smiling-eyes_1f604.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/heavy-black-heart_2764.png">
                            </v-img>
                        </v-avatar>
                        <div class="questrial ml-3"> +15</div>
                    </v-layout>
                </v-flex>
                    </template>
                <Emojis/>
               </v-menu>
                <v-flex class="text-right">
                    <v-layout wrap justify-end>
                        <div class="questrial mr-3 font-weight-bold ">
                        2 Comments 
                        <v-icon v-if="false" @click="" small>keyboard_arrow_down</v-icon>
                        <v-icon  @click="" small>keyboard_arrow_up</v-icon> 
                    </div> 
                    <div class="questrial ml-2 font-weight-bold mr-2">
                        Share
                    </div>
                </v-layout>
                </v-flex>
            </v-layout>
            <v-divider></v-divider>
            
        </v-card-text>
         <v-list-item style="align-items:normal">
                <v-list-item-avatar>
                    <img :src="avatar1" alt="John">
                </v-list-item-avatar>
                <v-list-item-content >
                    <div class="questrial font-weight-bold" style="font-size: 14px">Juan Sanchez</div>
                    <v-list-item-subtitle class="questrial body1 grey--text text--darken-1 my-2">Ana.. ya llego me espera en cafetería</v-list-item-subtitle>
                    <v-layout>
                    <v-flex xs4>
                        <v-layout row >
                            <div class="questrial caption indigo--text font-weight-bold ml-1 mr-3">Me gusta</div>
                            <div class="questrial caption indigo--text font-weight-bold mr-3">Respuesta</div>
                            <div class="questrial caption indigo--text font-weight-bold mr-3">Traducir</div>
                            <div class="questrial grey--text caption font-weight-bold ml-3">5 minutos</div>
                        </v-layout>
                        
                    </v-flex>
                    
                </v-layout>
                </v-list-item-content>
                
            </v-list-item>
            <v-list-item>
                <v-list-item-avatar>
                    <img :src="avatar2" alt="John">
                </v-list-item-avatar>
                <v-list-item-content>
                    <div class="questrial font-weight-bold" style="font-size: 14px">Alejandro Nuñez</div>
                    <v-list-item-subtitle class="questrial body1 font-weight-medium grey--text text--darken-1 my-2">Ana Hizo el trabajo del profesor Zambrano_??'</v-list-item-subtitle>
                    <v-layout>
                    <v-flex xs4>
                        <v-layout row>
                            <!-- <v-flex xs12> -->
                            <div class="questrial caption indigo--text font-weight-bold ml-1 mr-3">Me gusta</div>
                            <div class="questrial caption indigo--text font-weight-bold mr-3">Respuesta</div>
                            <div class="questrial caption indigo--text font-weight-bold mr-3">Traducir</div>
                            <div class="questrial grey--text caption font-weight-bold ml-3">18 minutos</div>
                            <!-- </v-flex> -->
                            
                        </v-layout>
                    </v-flex>
                </v-layout>
                </v-list-item-content>
                
            </v-list-item>
            <div class="px-4">
                <v-text-field class="questrial" height="45px" background-color="grey lighten-3" append-icon="photo_camera sentiment_satisfied" placeholder="Write a comment..." rounded></v-text-field>
            </div>
    </v-card>
</template>

<script>
import Emojis from '../Emoji/Emojis'
export default {
    components: {
        Emojis
    },
    data(){
        return{
            avatar1: require('../../assets/avatars/18.jpeg'),
            avatar2: require('../../assets/avatars/20.jpeg'),
            avatar3: require('../../assets/avatars/17.jpg'),

            lorem: `Un rato agradable en una universidad FET`,
        }
    }
}
</script>

<style>

</style>
