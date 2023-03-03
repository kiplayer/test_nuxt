<template>
  <div>
      Sync1 Component<br />
      <input
        type="checkbox"
        v-bind:checked="data"
        v-on:change="$emit('doSync3', $event.target.checked)"
      >
  </div>
</template>

<script>
export default {
  name: 'Sync3',
  props: {
    data: Boolean,
  },
};
</script>