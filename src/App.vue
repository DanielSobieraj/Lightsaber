<template>
    <v-container fluid fill-height class="container">
        <v-row>
            <v-col cols="12" style="display: flex; justify-content: center">
                <video  autoplay width="100%" height="720px" :src="video"></video>
            </v-col>
            <v-col cols="12" class="flex-md-column" style="display: flex; justify-content: space-around; flex-wrap: wrap">
                <v-btn
                        @click="changeShow"
                >
                    Show
                </v-btn>
                <v-btn
                        @click="changeOff"
                        dark
                >
                    Turn off
                </v-btn>
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
                <v-btn @click="changePurple"
                       color=rgb(128,0,128)
                       dark>
                    {{ purple }}
                </v-btn>
                <v-btn @click="changeRed"
                       color=rgb(255,0,0)
                       dark>
                    {{ red }}
                </v-btn>
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
    import show from '../src/assets/show.mp4'

    import yellow from '../src/assets/yellow.mp4'
    import yellow_disassemble from '../src/assets/yellow_disassemble.mp4'

    import green from '../src/assets/green.mp4'
    import green_disassemble from '../src/assets/green_disassemble.mp4'

    import blue from '../src/assets/blue.mp4'
    import blue_disassemble from '../src/assets/blue_disassemble.mp4'

    import purple from '../src/assets/purple.mp4'
    import purple_disassemble from '../src/assets/purple_disassemble.mp4'

    import red from '../src/assets/red.mp4'
    import red_disassemble from '../src/assets/red_disassemble.mp4'

    export default {
        name: 'App',
        data() {
            return {
                video: null,
                yellow: "Yellow",
                green: "Green",
                blue: "Blue",
                purple: "Purple",
                red: "Red",
                disassemble: "Disassemble"
            }
        },
        methods: {
            changeShow() {
                this.video = show
            },
            changeOff() {
                this.video = ""
            },
            changeYellow() {
                if (this.yellow == this.disassemble) {
                    this.yellow = "yellow";
                    this.video = yellow_disassemble;
                } else {
                    this.yellow = this.disassemble;
                    this.video = yellow;
                }
            },
            changeGreen() {
                if (this.green == this.disassemble) {
                    this.green = "green";
                    this.video = green_disassemble;
                } else {
                    this.green = this.disassemble;
                    this.video = green;
                }
            },
            changeBlue() {
                if (this.blue == this.disassemble) {
                    this.blue = "blue";
                    this.video = blue_disassemble;
                } else {
                    this.blue = this.disassemble;
                    this.video = blue;
                }
            },
            changePurple() {
                if (this.purple == this.disassemble) {
                    this.purple = "purple";
                    this.video = purple_disassemble;
                } else {
                    this.purple = this.disassemble;
                    this.video = purple;
                }
            },
            changeRed() {
                if (this.red == this.disassemble) {
                    this.red = "red";
                    this.video = red_disassemble;
                } else {
                    this.red = this.disassemble;
                    this.video = red;
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
    font-family: STARWARS,serif !important;
}

</style>
