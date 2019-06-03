# vue-click-outside
Vue directive to work for click outside handling for any given div

## Example

```vue
<template>
  <div>
    <div v-click-outside="hide" @click="isOutSideHelloClicked = false">Hello</div>
    <div v-if="isOutSideHelloClicked">You Clicked outside hello!!!</div>
    <div v-else-if="isOutSideHelloClicked === false">You Clicked inside hello!!!</div>
  </div>
</template>

<script>
import directivesClickOutside from 'vue-click-outside'

export default {
  data () {
    return {
      isOutSideHelloClicked: null
    }
  },
  
  // this section is important to import directive
  directives: {
    'click-outside': directivesClickOutside
  },

  methods: {
    hide () {
      this.isOutSideHelloClicked = true
    }
  }
}
</script>
```
