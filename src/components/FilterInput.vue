<template>
  <div class="">
    <input v-model="message" placeholder="Mensaje" />
    <p>El mensaje es: {{ message | replace | toUpperCase}}</p>

    <h4>Preguntas</h4>
    <p>
        1 - A
    </p>
    <p>
        2 - B
    </p>
    <p>
        3 - D
    </p>
    <p>
        4 - A, B
    </p>
    <p>
        5 - B
    </p>
  </div>
</template>

<script>
export default {
  name: 'FilterInput',
  filters: {
    toUpperCase: function (value) {
      if (!value) return ''
      value = value.toString()
      return value.toUpperCase()
    },
    replace: function (value) {
      const chars = {
        a: 'u',
        e: 'o',
        o: 'e',
        u: 'a'
      }

      return value.replace(/[aeou]/g, function (c) { return chars[c] })
    }
  },
  data () {
    return {
      message: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
