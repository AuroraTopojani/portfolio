<template>
  <div class="">
    <div>
      <i class="fa fa-2x py-2" :class="classIcon" aria-hidden="true">{{
          title
        }}</i>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    classIcon: {
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
