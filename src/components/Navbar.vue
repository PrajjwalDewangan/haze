<template>
    <div>
        <v-app-bar color="#f0e8eb" dark>
            <v-row>
                <v-col cols="12" sm="4">
                    <v-app-bar-nav-icon @click="drawer = true" style="color: black;"></v-app-bar-nav-icon>
                </v-col>
                <v-col cols="12" sm="4">
                    <v-toolbar-title @click="$router.push('/')">HAZE</v-toolbar-title>
                </v-col>
                
                <v-col cols="12" sm="4" align="right">
                    
                    <v-btn icon style="color: black;">
                        <v-icon>mdi-magnify</v-icon>
                    </v-btn>

                    <v-btn icon style="color: black;" @click="$router.push('/wishlist')">
                        <v-icon>mdi-heart</v-icon>
                    </v-btn>

                    <v-btn icon style="color: black;" @click="$router.push('/cart')">
                        <v-icon>mdi-shopping-outline</v-icon>
                    </v-btn>

                    <v-btn icon style="color: black;" @click="$router.push('/profile')">
                        <v-icon>mdi-account-circle-outline</v-icon>
                    </v-btn>
                </v-col>
            </v-row>
        </v-app-bar>
        <v-navigation-drawer v-model="drawer" absolute temporary>
            <v-list nav dense>
                <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
                    <v-list-item @click="$router.push('/')">
                        <v-list-item-icon>
                            <v-icon>mdi-home</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>Home</v-list-item-title>
                    </v-list-item>

                    <v-list-item @click="$router.push('/shop')">
                        <v-list-item-icon>
                            <v-icon>mdi-diamond-stone</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>Shop Jewellery</v-list-item-title>
                    </v-list-item>

                    <v-list-item @click="$router.push('/collections')">
                        <v-list-item-icon>
                            <v-icon>mdi-rhombus-split</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>Collections</v-list-item-title>
                    </v-list-item>

                    <v-list-item @click="$router.push('/gifting')">
                        <v-list-item-icon>
                            <v-icon>mdi-gift</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>Gifting</v-list-item-title>
                    </v-list-item>

                    <v-list-item @click="$router.push('/about')">
                        <v-list-item-icon>
                            <v-icon>mdi-information-outline</v-icon>
                        </v-list-item-icon>
                        <v-list-item-title>About Us</v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>

<script>
export default {
    data: () => ({
        drawer: false,
        group: null,
    }),
}
</script>

<style lang="scss" scoped>
@import url(@/assets/styles.css);
</style>