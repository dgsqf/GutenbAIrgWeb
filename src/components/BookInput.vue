<script>
import Chapter from "./Chapter.vue";
export default {
  data() {
    return {
      book: {
        title: "",
        chapters: [
          {
            id: 0,
            title: "test",
            text: "this is a test chapter",
          },
          {
            id: 1,
            title: "test2",
            text: "this is a test chapter",
          },
        ],
      },
    };
  },
  components: { Chapter },
};
</script>

<template>
  <Chapter
    @delete="book.chapters.splice(chapter.id)"
    v-for="chapter in book.chapters"
    :key="chapter.id"
    :title="chapter.title"
    :text="chapter.text"
    :id="id"
  />
</template>
