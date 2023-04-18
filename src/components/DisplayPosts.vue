<template>
  <div>
    <button @click="toggle_button">Change Layout</button>
    <section v-if="show_post === true">
      <div class="horizontal_div" v-for="(posts, i) in posts" :key="i">
        <p>{{posts.content}}</p>
        <p>User : {{posts.user}}</p>
        <p>Created At: {{posts.date_created}}</p>
      </div>
    </section>
    <section v-if="show_post === false">
      <div class="vertical_div" v-for="(posts, i) in posts" :key="i">
        <p>{{posts.content}}</p>
        <p>User : {{posts.user}}</p>
        <p>Created At: {{posts.date_created}}</p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    toggle_button: function () {
      this.show_post = !this.show_post;
    },
  },
  data() {
    return {
      show_post: true,
      posts: [
        {
          content: `The ocean is very big`,
          user: `User_Number_1`,
          date_created: `14 - 02 - 2023`
        },
        {
          content: `there are many animals in the ocean`,
          user: `User_Number_2`,
          date_created: `25 - 12 - 2022`
        },
      ],
    };
  },
};
</script>

<style scoped>
.horizontal_div {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.vertical_div {
  display: grid;
  grid-template-columns: 1fr;
}
</style>