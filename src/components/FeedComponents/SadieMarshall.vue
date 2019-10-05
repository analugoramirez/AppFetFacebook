<template>
    <v-card rounded outlined>
        <div>
            <v-list-item>
                <v-list-item-avatar>
                    <img src="../../assets/avatars/19.jpeg" alt="John">
                </v-list-item-avatar>
                <v-list-item-content class="mt-2">
                    <v-list-item-title class="questrial subtitle">Roberto Cerquera</v-list-item-title>
                    <v-list-item-subtitle class="questrial caption indigo--text">Friends</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                    <v-icon @click="">more_horiz</v-icon>
                </v-list-item-action>
            </v-list-item>
        </div>
        <!-- <v-container grid-list-xs fluid style="padding:10px"> -->
            <v-layout wrap>
                <v-flex xs12>
                    <v-card flat tile>
                        
                        <v-img
                        >
                       <iframe width="660" height="315" src="https://www.youtube.com/embed/WRHVP711xnA" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                            <v-layout
                            fill-height
                            align-center
                            justify-center
                            ma-0
                            >
                                
                                    
                            </v-layout>
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
            <v-card-title>
                <div class="questrial font-weight-bold" style="font-size: 17px">La mejor canción del mundo segun DINO</div>
            </v-card-title>
            <v-card-text>
            <div class="questrial body1 mb-4">{{lorem}}</div>
            <v-divider></v-divider>
            <v-layout class="py-4">
            <v-menu open-on-hover top offset-y min-width="200px">
                    <template v-slot:activator="{ on }">
                <v-flex v-on="on">
                    <v-layout>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/smiling-face-with-sunglasses_1f60e.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/grinning-face_1f600.png">
                            </v-img>
                        </v-avatar>
                        <v-avatar size="20" class="ml-1">
                            <v-img
                                src="https://emojipedia-us.s3.dualstack.us-west-1.amazonaws.com/thumbs/160/facebook/65/runner_emoji-modifier-fitzpatrick-type-1-2_1f3c3-1f3fb_1f3fb.png">
                            </v-img>
                        </v-avatar>
                        <div class="questrial ml-3"> +98</div>
                    </v-layout>
                </v-flex>
                </template>
                <Emojis/>
            </v-menu>
                <v-flex class="text-right">
                    <v-layout wrap justify-end>
                        <div class="questrial mr-3 font-weight-bold ">
                        28 Comentarios
                        <v-icon  @click="" small>keyboard_arrow_down</v-icon>
                        <v-icon v-if="false" @click="" small>keyboard_arrow_up</v-icon> 
                    </div> 
                    <div class="questrial ml-2 font-weight-bold mr-2">
                        3 Compartido
                    </div>
                </v-layout>
                </v-flex>
            </v-layout>
            <v-divider></v-divider>
            
        </v-card-text>
         <div class="px-4">
                <v-text-field class="questrial" height="45px" append-icon="photo_camera sentiment_satisfied" background-color="grey lighten-3" placeholder="Escribir comentarios" rounded></v-text-field>
            </div>
        <!-- </v-container> -->
    </v-card>
</template>

<script>
import Emojis from '../Emoji/Emojis'
export default {
    components:{
        Emojis,
    },
    data(){
        return {
            lorem: `Coldplay es una banda británica de pop rock formada en Londres en 1996. El grupo está integrado por Chris Martin (voz, teclado, guitarra), Jon Buckland (guitarra principal), Guy Berryman (bajo eléctrico) y Will Champion (batería, coros y otros instrumentos). ... Coldplay ha vendido internacionalmente50 millones de copias`,
        }
    }
}
</script>

<style>
.v-menu__content{
    border-radius: 25px
}
</style>
