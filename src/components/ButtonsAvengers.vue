<template>
  <div class="buttonsAvengers">
    <button v-for="buttonAvenger in arrAvengers" :key="buttonAvenger.id" @click="$emit('handle-set-avenger', buttonAvenger.name)" >{{buttonAvenger.name}}</button>
  </div>
</template>

<script>
export default {
  props: {
    avenger: {
      type: String,
    }
  },
  data() {
    return {
      arrAvengers: [
        {
          id: 1,
          name: "Hulk",

        },
        {
          id: 2,
          name: "Spider Man",
        },
        {
          id: 3,
          name: "Iron Man",
        },
        {
          id: 4,
          name: "Thor",
        },
        {
          id: 5,
          name: "Hawkeye",
        },
        {
          id: 6,
          name: "Black Widow",
        },
        {
          id: 7,
          name: "Captain America",
        },
      ],
    }
  },
  methods: {
  }

}
</script>

<style scoped>
  .buttonsAvengers {
    display: flex;
    justify-content: space-between;
    padding: 2rem 0;
    margin-inline: 7%;
  }

  button {
    font-family: "Oswald", sans-serif;
    color: white;
    background: none;
    font-size: 1rem;
    cursor: pointer;
    text-transform: uppercase;
    border: none;
    transition: all 0.3s;
    transform: scale(1);
    padding: 10px 35px;
    --coAvangerrnerSize: 13px;
    overflow: auto;
    clip-path:
      polygon(
        0 100%,
        0 var(--cornerSize),
        var(--cornerSize) 0,
        100% 0,
        100% calc(100% - var(--cornerSize)),
        calc(100% - var(--cornerSize)) 100%
      );
  }

  .buttonsAvengers button:hover {
      transform: scale(1.05);
      background-color: #e62429;
    }
</style>