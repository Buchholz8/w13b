<template>
    <section >
        <button @click="toggle_button"></button>
        <div>
            <p> {{post[`content`]}} </p>
            <p> {{post[`user`]}} </p>
            <p> {{post[`date_created`]}} </p>
        </div>
    </section>
</template>

<script>
export default {
  methods: {
    toggle_button: function(){

    },
    data() {
      return {
        posts: [
          {
            content: `The ocean is very big`,
            user: `User_Number_1`,
            date_creeated: 02 - 20 - 2023,
          },
          {
            content: `there are many animals in the ocean`,
            user: `User_Number_2`,
            date_creeated: 02 - 12 - 2022,
          },
        ],
      };
    },
  },
};
</script>

<style scoped>
</style>