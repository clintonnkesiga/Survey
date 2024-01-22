<template>
<PageComponent title="View or create a survey">
  View or create a survey
</PageComponent>
</template>

<script setup>
import store from "../store";
import {ref} from "vue";
import {useRoute} from "vue-router";
import PageComponent from "../components/PageComponent.vue";

const route = useRoute();

let model = ref({
  title: '',
  status: false,
  description: null,
  image: null,
  expire_date: null,
  questions: [],
});

if (route.params.id) {
  model.value = store.state.surveys.find(
    (s) => s.id === parseInt(route.params.id)
  );
}
</script>

<style scoped>

</style>
