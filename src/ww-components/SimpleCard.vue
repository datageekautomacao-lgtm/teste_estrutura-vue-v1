<template>
  <div class="card">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>

    <button @click="handleClick">
      {{ buttonText }}
    </button>
  </div>
</template>

<script>
export default {
  name: "SimpleCard",

  props: {
    title: {
      type: String,
      default: "Título do Card"
    },
    description: {
      type: String,
      default: "Descrição simples do componente para teste no WeWeb."
    },
    buttonText: {
      type: String,
      default: "Clique aqui"
    }
  },

  methods: {
    handleClick() {
      this.$emit("clicked");
    }
  }
};
</script>

<style scoped>
.card {
  padding: 20px;
  border-radius: 12px;
  border: 1px solid #ddd;
  background: #fff;
  text-align: center;
}

button {
  margin-top: 12px;
  padding: 10px 16px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  background: #333;
  color: #fff;
}
</style>
