<template>
    <v-container fluid fill-height class="container">
        <v-row>
            <v-col cols="12">
                <video autoplay width="100%" height="720" :src="video"></video>
            </v-col>
            <v-col cols="12" style="display: flex; justify-content: space-around">
                <v-btn @click="changeVideo">Disassemble</v-btn>
                <v-btn
                        @click="changeYellow"
                        color=rgb(255,255,0)
                >
                    {{ yellow }}
                </v-btn>
                <v-btn @click="changeGreen"
                       color=rgb(0,255,0)>
                    {{ green }}
                </v-btn>
                <v-btn @click="changeBlue"
                       color=rgb(0,0,255)
                       dark>
                    {{ blue }}
                </v-btn>
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
    import stock from '../src/assets/stock.mp4'
    import disassemble from '../src/assets/disassemble.mp4'
    import yellow from '../src/assets/yellow.mp4'
    import yellow_disassemble from '../src/assets/yellow_disassemble.mp4'
    import green from '../src/assets/green.mp4'
    import green_disassemble from '../src/assets/green_disassemble.mp4'
    import blue from '../src/assets/blue.mp4'
    import blue_disassemble from '../src/assets/blue_disassemble.mp4'

    export default {
        name: 'App',
        data() {
            return {
                video: stock,
                yellow: "Yellow",
                green: "Green",
                blue: "Blue"
            }
        },
        methods: {
            changeVideo() {
                this.video = disassemble;
            },
            changeYellow() {
                if (this.yellow == "disassemble") {
                    this.yellow = "yellow";
                    this.video = yellow_disassemble;
                } else {
                    this.yellow = "disassemble";
                    this.video = yellow;
                }
            },
            changeGreen() {
                if (this.green == "disassemble") {
                    this.green = "green";
                    this.video = green_disassemble;
                } else {
                    this.green = "disassemble";
                    this.video = green;
                }
            },
            changeBlue() {
                if (this.blue == "disassemble") {
                    this.blue = "blue";
                    this.video = blue_disassemble;
                } else {
                    this.blue = "disassemble";
                    this.video = blue;
                }
            }
        }
    }
</script>
<style>
.container {
    background-image: url("../src/assets/background.jpg");
    background-position: center;
    background-size: cover;
    height: 100vh !important;
}

</style>
