<template>
    <form>
        <p>Emoji Name: <input v-model="newName"></p>
        <p>Category: <input v-model="newCat"></p>
        <p>Image URL: <input v-model="newImage"></p>
        <button v-on:submit.prevent="Add(newEmoji)">Add</button>
    </form>
</template>

<script>

export default {
  data() {
    return {
      newName: '',
      newCat: '',
      newImage: ''
    };
  },
  computed: {
    newEmoji() {
      return {
        name: this.newName,
        category: this.newCat,
        image: this.newImage
      };
    }
  },
  props: {
    Add: Function,
  }
};

</script>
