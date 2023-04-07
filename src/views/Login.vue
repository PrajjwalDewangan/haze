<template>
    <body class="login">
        <v-parallax dark src="@/assets/loginBack.png" class="login">
            <div class="center" height="100%">
                <v-row>
                    <v-col cols="10" offset="1" sm="6" offset-sm="3" md="4" offset-md="4">
                        <v-img src="@/assets/HAZE.svg"></v-img>
                        <br>
                        <v-img src="@/assets/Tag.svg"></v-img>
                        <br>
                        <!-- <v-avatar color="primary" size="87"><v-img src="@/assets/logo.jpg"></v-img></v-avatar> -->
                        <!-- <v-text-field label="Username" v-model="username" outlined></v-text-field> -->
                        <!-- <v-text-field label="Password" v-model="password" type="password" outlined></v-text-field> -->
                    </v-col>
                </v-row>
                <v-row>
                    <v-col cols="2" offset="4">
                        <v-select :items="items" class="cdrop" label="Country Code" outlined></v-select>
                    </v-col>
                    <v-col cols="2">
                        <v-text-field class="phonebox" label="Phone Number" v-model="username" outlined
                            color="white"></v-text-field>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col>
                        <p class="confirmation">By continuing, I agree to <u>Terms of Use</u> & <u>Privacy Policy</u></p>
                        <v-btn class="ma-2" outlined color="#b9bbc1" elevation="0" @click="authenticate()">Continue</v-btn>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col cols="12" sm="6" align="right">
                        <v-img src="@/assets/Google.svg" max-height="300px" max-width="50px"></v-img>
                    </v-col>
                    <v-col cols="12" sm="6">
                        <v-img src="@/assets/Apple.svg" max-height="330px" max-width="50px"></v-img>
                    </v-col>
                </v-row>
            </div>
        </v-parallax>
    </body>
</template>

<script>
export default {
    data() {
        return {
            username: "",
            password: "",
            items: []
        }
    },
    methods: {
        authenticate() {
            alert("Login Clicked")
        }
    },
}
</script>

<style lang="scss" scoped>
@import url(@/assets/styles.css);
</style>