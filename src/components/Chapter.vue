<script>
export default {
  props: ["title", "text", "id"],
};
</script>

<template>
  <div class="box m-2">
    <h1>{{ title }}</h1>
    <p>{{ text }}</p>

    <button
      class="button is-danger is-outlined is-right"
      @click="$emit('delete')"
    >
      <span>Delete</span>
      <span class="icon is-small">
        <i class="fas fa-times"></i>
      </span>
    </button>
  </div>
</template>
