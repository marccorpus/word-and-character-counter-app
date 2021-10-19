<template>
  <b-row>
    <b-col md="6" offset-md="3">
      <b-card class="card">
        <b-row no-gutters class="text-center">
          <b-col>
            <h2>{{ wordsCount }}</h2>
            <div class="label">Words</div>
          </b-col>
          <b-col>
            <h2>{{ charactersCount }}</h2>
            <div class="label">Characters</div>
          </b-col>
        </b-row>
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: ["wordsCount", "charactersCount"],
};
</script>

<style scoped>
.card {
  background-color: #3b250e;
  color: #fff;
  margin-top: -18px;
  border-radius: 0 0 8px 8px;
  box-shadow: 0 20px 40px rgba(30, 21, 49, 0.4);
}
.label {
  color: #ccc;
}
</style>
