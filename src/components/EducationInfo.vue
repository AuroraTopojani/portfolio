<template>
  <div class="">
    <div>
      <p>{{ date }}</p>
      <p>{{ title }}</p>
      <p>{{ description }}</p>
    </div>
    <hr />
  </div>
</template>

<script>
export default {
  props: {
    date: {
      type: String,
    },
    title: {
      type: String,
    },
    description: {
      type: String,
    },
  },
};
</script>
