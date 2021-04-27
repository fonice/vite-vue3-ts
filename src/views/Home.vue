<script lang="tsx">
  import HelloWorld from '@/components/HelloWorld.vue'
  import { defineComponent, ref } from 'vue'
  export default defineComponent({
    name: 'Home',
    components: {
      HelloWorld
    },
    setup() {
      const msg = ref('Hello World!')
      return () => (
        <>
          <hello-world msg={msg.value}> </hello-world>
        </>
      )
    }
  })
</script>
