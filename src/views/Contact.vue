<template>
  <v-main>
    <v-img src="../assets/images/img14.jpg">
      <v-row align="end" class="lightbox white--text pa-2 fill-height">
        <v-col>
          <v-container>
            <div class="headline">Contact Us</div>
          </v-container>
        </v-col>
      </v-row>
    </v-img>
    <div class="block">
      <v-container>
        <v-form ref="form" v-model="valid" :lazy-validation="lazy">
          <v-text-field v-model="name" :counter="10" :rules="nameRules" label="Name" required></v-text-field>
          <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
          <v-textarea v-model="text" :counter="10" :rules="textRules" label="Write a something..." required></v-textarea>

          <v-checkbox v-model="checkbox" :rules="[v => !!v || 'You must agree to continue!']" label="Do you agree?" required></v-checkbox>
          <v-btn depressed :disabled="!valid" color="success" class="mr-4" @click="submit">Submit</v-btn>
          <v-btn depressed color="error" class="mr-4" @click="reset">Reset Form</v-btn>
        </v-form>
      </v-container>
    </div>

    <div>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1630.214032698006!2d129.08079615826688!3d35.19580498694515!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x35689368848d06e9%3A0x51a63d7aa8c2fc4a!2z67K97IKwReuplO2DgO2PtOumrOyKpA!5e0!3m2!1sko!2skr!4v1611471412836!5m2!1sko!2skr"
        width="100%"
        height="450"
        frameborder="0"
        style="border:0;"
        allowfullscreen=""
        aria-hidden="false"
        tabindex="0"
      ></iframe>
    </div>
  </v-main>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    name: '',
    nameRules: [v => !!v || 'Name is required', v => (v && v.length <= 10) || 'Name must be less than 10 characters'],
    email: '',
    emailRules: [v => !!v || 'E-mail is required', v => /.+@.+\..+/.test(v) || 'E-mail must be valid'],
    text: '',
    textRules: [v => !!v || 'Name is required', v => (v && v.length >= 10) || 'Text must be more than 20 characters'],
    checkbox: false,
    lazy: false
  }),

  methods: {
    submit() {
      alert('나중에 만들께요!')
    },
    reset() {
      this.$refs.form.reset()
    },
    resetValidation() {
      this.$refs.form.resetValidation()
    }
  }
}
</script>
