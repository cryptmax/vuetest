<template>
  <div class="form-group">
    <textarea class="form-control" placeholder="Placeholder"
              :id="name"
              :name="name"
              :value="value"
              @input="update"></textarea>
    <label :for="name">{{ label }}:</label>
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
