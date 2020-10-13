<template>
  <div>
    <b-jumbotron>
      <template v-slot:lead>
        {{ currentQuestion.question }}
      </template>
      <hr class="my-4">
      <ul>
        <li v-for="answer in currentQuestion.incorrect_answers" v-bind:key="answer">
          {{ answer }}
        </li>
        <li>
          {{ currentQuestion.correct_answer}}
        </li>
      </ul>

      <b-button variant="primary" href="#">Submit</b-button>
      <b-button variant="success" href="#">Next</b-button>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  props: {
    currentQuestion: Object,
  }
}
</script>