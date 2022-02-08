<template>
    <a :href="`https://t.me/${this.username}`">
    <h1>
        <span>@ </span>{{ username }}
    </h1>
    </a>
</template>

<script>
export default {
  name: 'User',
  props: {
    username: String
  }
}
</script>

<style scoped>
    span {
        opacity: .5;
    }
    a {
        color: grey
    }
</style>
