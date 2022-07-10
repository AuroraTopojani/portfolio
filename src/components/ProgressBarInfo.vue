<template>

  <div class="">
    <p>{{ LanguageName }}</p>
    <div class="progress">
      <div
          class="progress-bar progress-bar-danger progress-bar-striped"
          role="progressbar"
          :aria-valuenow="knowledge"
          aria-valuemin="0"
          aria-valuemax="100"
          :style="PercentStyle"
      >
        {{ knowledge }}%
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    LanguageName: {
      type: String,
    },
    knowledge: {
      type: String,
    },
  },
  data() {
    return {
      PercentStyle: {
        width: this.knowledge + "%",
      },
    };
  },
};
</script>
