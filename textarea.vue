<template>
  <div class="form-group">
    <label :for="name">{{ label }}:</label>
    <textarea class="form-control" placeholder="Placeholder"
              :id="name"
              :name="name"
              :value="value"
              @input="update"></textarea>
  </div>
</template>

<script>
  export default {
    props: {
      name: { required: true },
      label: { required: false },
      value: { required: false },
    },
    data() {
      return {}
    },
    methods: {
      update(e) {
        this.$emit('input', e.target.value);
      }
    },
  }
</script>
