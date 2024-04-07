<template>
    <v-row justify="center">
    <div class="form-section d-flex justify-center align-center">
        <v-col>
            <h2>Try Figma for free</h2>
            <v-form v-model="valid">
                <v-col>
                <v-text-field
                    v-model="email"
                    :rules="emailRules"
                    label="E-mail"
                    hide-details
                    required>
                </v-text-field>
                <v-text-field
                    v-model="password"
                    :rules="passwordRules"
                    label="Password"
                    hide-details
                    required>
                </v-text-field>
                <v-btn outlined color="black" style="margin-top: 20px;">
                    Create Account
                </v-btn>
                <p align="center" style="margin-top: 10px;">Already have an account? <a>Log in</a></p>
                <small>By clicking 'Create account', I agree to Figmas's TOS and Privacy Policy</small>
            </v-col>
            </v-form>
        </v-col>
    </div>
</v-row>
</template>

<script>
  export default {
    data: () => ({
      valid: false,
      email: '',
      emailRules: [
        value => {
          if (value) return true

          return 'E-mail is requred.'
        },
        value => {
          if (/.+@.+\..+/.test(value)) return true

          return 'E-mail must be valid.'
        },
      ],
      password: '',
      passwordRules: [
        value => {
          if (value) return true
          else {
            return 'Passsword is requred.'
          }
        },
        value => {
          if (value.length > 6){
            return true
          }
          else {
            return 'Password must not be less than 6 chars.'
          }
        },
      ],
    }),
  }
</script>

<style scoped>
    .form-section {
        height: 95vh;
        max-width: 400px;
    }
</style>