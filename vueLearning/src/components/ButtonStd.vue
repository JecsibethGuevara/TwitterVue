<template>
  <button :class="btnClass" @click="handleClick">
    {{ buttonText }}
  </button>
</template>

<script>
export default {
  props: {
    buttonText: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: "primary",
    },
    onClick: {
      type: Function,
      default: () => {},
    },
  },
  computed: {
    btnClass() {
      return `btn-${this.color}`;
    },
  },
  methods: {
    handleClick() {
      this.onClick();
    },
  },
};
</script>

<style scoped>
/* Add your button styling here */
button {
  padding: 10px 20px;
  border: none;
  cursor: pointer;
}

.btn-primary {
  background-color: #007bff;
  color: #fff;
}

.btn-secondary {
  background-color: #6c757d;
  color: #fff;
}

/* Add more styles for other colors as needed */
</style>
