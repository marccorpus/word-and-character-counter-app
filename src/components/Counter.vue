<template>
  <b-container>
    <b-row class="mb-3">
      <b-col class="text-center">
        <h1>Word and Character Counter</h1>
      </b-col>
    </b-row>

    <b-row>
      <b-col md="6" offset-md="3">
        <b-card class="card">
          <b-form-textarea
            v-model="text"
            placeholder="Enter something..."
            rows="10"
            ref="textarea"
            class="shadow-none"
          ></b-form-textarea>
        </b-card>
      </b-col>
    </b-row>

    <Result :words-count="wordsCount" :characters-count="charactersCount" />
  </b-container>
</template>

<script>
import Result from "./Result.vue";

export default {
  data() {
    return {
      text: "",
    };
  },
  computed: {
    wordsCount() {
      return this.text.split(/\s+/).filter((item) => item).length;
    },
    charactersCount() {
      return this.text.length;
    },
  },
  components: {
    Result,
  },
  mounted() {
    this.$refs.textarea.focus();
  },
};
</script>

<style scoped>
.card {
  border-radius: 8px;
}
textarea {
  border: none;
  outline: none;
  font-size: 16px;
  line-height: 28px;
  resize: none;
  color: #0e101a;
}
</style>
