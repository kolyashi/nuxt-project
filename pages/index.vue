<template>
<v-col>
    <v-container>
        <v-col align="center">
            <img src="/Screenshot_1.png" alt="Видео нет,поэтому только картинка">
            <h3 style="font-weight: 400;margin-bottom: 20px; margin-top:30px;">Figma connects everyone in the design process so teams can deliver</h3>
            <v-btn outlined color="black" @click="scrollToForm">
                Sign up free
            </v-btn>
        </v-col>
    </v-container>
    <v-img src="/Screenshot_2.png" style="width: 150%;"></v-img>
    <v-container>
        <SocialCard/>
    </v-container>
    <LastDivider/>
    <v-container ref="registerForm">
        <RegisterForm/>
    </v-container>
</v-col>
</template>
    
<script>
import SocialCard from '../components/SocialCard.vue';

export default {
  name: 'index',
  components: {SocialCard},
  methods: {
    scrollToForm() {
        const el = this.$refs.registerForm;

        if(el) {
            el.scrollIntoView({behavior: 'smooth'});
        }
    }
  }
};
</script>