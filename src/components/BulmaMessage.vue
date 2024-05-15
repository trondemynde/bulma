<template>
  <article :class="['message', messageType]">
    <div class="message-header">
      <p>{{ title }}</p>
      <button class="delete" aria-label="delete" @click="$emit('close')"></button>
    </div>
    <div class="message-body">
      <slot></slot>
    </div>
  </article>
</template>

<script>
export default {
  name: "BulmaMessage",
  props: {
    title: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      validator(value) {
        return ['is-primary', 'is-link', 'is-info', 'is-success', 'is-warning', 'is-danger'].includes(value);
      },
      default: 'is-primary'
    }
  },
  computed: {
    messageType() {
      return this.type;
    }
  }
};
</script>
