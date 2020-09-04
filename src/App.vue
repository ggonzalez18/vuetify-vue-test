<template>
  <v-app>
    <v-app-bar app color="dark" dark>
      <v-toolbar-title>Edutecno</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text>Home</v-btn>
      <v-btn text>Login</v-btn>
    </v-app-bar>
    <v-card width="420px" class="mx-auto my-auto">
      <v-card-title><h1 class="mx-auto">Login</h1></v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field label="userName" prepend-icon="mdi-account-circle"/>
          <v-text-field
          @click:append="showPassword = !showPassword"
          label="password"
          :type="showPassword ? 'text' : 'password'"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"/>
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-btn color="success">Register</v-btn>
        <v-spacer></v-spacer>
        <v-btn color="info">Login</v-btn>
      </v-card-actions>
    </v-card>
  </v-app>

</template>

<script>


export default {
  name: 'App',
  components: {
  },
  data: () => ({
    showPassword: false
  }),
};
</script>
