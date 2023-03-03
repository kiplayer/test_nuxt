<template>
  <div>
      Sync1 Component<br />
      <input
        type="checkbox"
        v-bind:checked="checked"
        v-on:change="$emit('doSync1', $event.target.checked)"
      >
  </div>
</template>

<script>
export default {
  name: 'Sync1',
  props: {
    checked: Boolean
  },
  model: {
    prop: 'checked',
    event: 'change'
  },
};
</script>