<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>Signupp</h1>
        <v-form>
          <v-text-field label="email" type="email"></v-text-field>
          <v-autocomplete label="which browsers do you use?" :items="browsers"></v-autocomplete>
          <v-file-input label="select your image"></v-file-input>
          <v-text-field label="pick birthdate" v-model="birthdate" readonly></v-text-field>
          <v-date-picker v-model="birthdate"></v-date-picker>
          <v-checkbox label="agree terms and conditions"></v-checkbox>
          <v-btn type="submit" color="primary">Submit</v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    birthdate: "",
    browsers: ["chrome", "firefox", "opera", "brave", "edge"],
  }),
};
</script>

<style>
</style>