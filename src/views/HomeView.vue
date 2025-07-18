<script setup>
  import { ref } from 'vue'
  const theme = ref('light')
  import logo from '@/assets/logoCSUCC/logo-csu-cc.png'

  function onClick () {
    theme.value = theme.value === 'light' ? 'dark' : 'light'
  }
</script>

<template>

  <v-responsive class="" max-height="3000">
    <v-app :theme="theme">
      <v-app-bar class="px-3">
        <v-spacer></v-spacer>

        <v-btn
          :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          text=""
          slim
          @click="onClick"
        ></v-btn>
      </v-app-bar>

      <v-main>
        <v-container>
          <v-row>
            <v-col cols="12" class="d-flex flex-column align-center justify-center">
              <v-img :src="logo" height="200" width="190" class="mt-10"></v-img>
              <h1 class="text-h2 text-align mt-16 mb-10 font-weigth-bold" >WELCOME BACK STUDENTS!</h1>
              <v-btn class="mt5 front-weight-bold"
              size="x-large"
              color="blue"
              elevation="10"
              to="/login">
              <v-icon>mdi-page-last</v-icon>
              Login
              </v-btn>


            </v-col>
          </v-row>

        </v-container>
      </v-main>
    </v-app>
  </v-responsive>
</template>

<style scoped>
</style>
