<script lang="tsx">
  import { ref, defineComponent } from 'vue'

  export default defineComponent({
    name: 'HelloWorld',
    props: {
      msg: {
        type: String,
        required: true
      }
    },
    setup: (props) => {
      const count = ref(0)
      return () => (
        <>
          <h1>{props.msg}</h1>
          <br />
          <button
            onClick={() => {
              count.value++
            }}
          >
            count is: {count.value}
          </button>
        </>
      )
    }
  })
</script>

<style scoped>
  a {
    color: #42b983;
  }

  label {
    margin: 0 0.5em;
    font-weight: bold;
  }

  code {
    background-color: #eee;
    padding: 2px 4px;
    border-radius: 4px;
    color: #304455;
  }
</style>
