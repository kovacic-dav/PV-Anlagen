<template>
  <h2>{{ foerderungen }}</h2>
  <h2>{{ investitionsschutz }}</h2>
  <div>
    {{ description }}
  </div>
</template>

<script>
export default {
  name: 'Description',
  props: {
    foerderungen: String,
    investitionsschutz: String,
    description: String,
  },
};
</script>

<style></style>
