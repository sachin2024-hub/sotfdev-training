<script setup>
import { ref } from 'vue'

const visible = ref(false)
</script>

<template>
  <v-app>
    <!-- Use v-main to wrap the entire page content and apply background -->
    <v-main
      class="d-flex align-center justify-center"
      style="
        background: url('/CSU-CC.jpg') no-repeat center center;
        background-size: cover;
        min-height: 100vh;
      "
    >
      <div>
        <!-- Logo image -->
        <v-img class="mx-auto my-6" max-width="228"></v-img>

        <!-- Login card -->
        <v-card class="mx-auto pa-12 pb-8" elevation="8" max-width="448" rounded="lg">
          <div class="text-subtitle-1 text-medium-emphasis">Account</div>

          <v-text-field
            density="compact"
            placeholder="Email address"
            prepend-inner-icon="mdi-email-outline"
            variant="outlined"
          ></v-text-field>

          <div
            class="text-subtitle-1 text-medium-emphasis d-flex align-center justify-space-between mt-4"
          >
            Password

            <a
              class="text-caption text-decoration-none text-blue"
              href="#"
              rel="noopener noreferrer"
              target="_blank"
            >
              Forgot login password?
            </a>
          </div>

          <v-text-field
            :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
            :type="visible ? 'text' : 'password'"
            density="compact"
            placeholder="Enter your password"
            prepend-inner-icon="mdi-lock-outline"
            variant="outlined"
            @click:append-inner="visible = !visible"
          ></v-text-field>

          <v-card class="mb-6 mt-4" color="surface-variant" variant="tonal">
            <v-card-text class="text-medium-emphasis text-caption"> </v-card-text>
          </v-card>

          <v-btn class="mb-4" color="blue" size="large" variant="tonal" block> Log In </v-btn>

          <v-card-text class="text-center">
            <a
              class="text-blue text-decoration-none"
              href="#"
              rel="noopener noreferrer"
              target="_blank"
            >
              Sign up now <v-icon icon="mdi-chevron-right"></v-icon>
            </a>
            <v-btn class="mt5" prepend-icon="" size="x-large" color="pink" elevation="10" to="/">
              balik sa pinaka una nga page
            </v-btn>
          </v-card-text>
        </v-card>
      </div>
    </v-main>
  </v-app>
</template>
