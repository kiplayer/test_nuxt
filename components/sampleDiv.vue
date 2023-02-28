<template>
    <div>
        sampleDiv Component<br />
        title:{{ title }}
    </div>
</template>

<script>
export default {
  name: 'sampleDiv',
  props: {
    title: String,
  },
};
</script>