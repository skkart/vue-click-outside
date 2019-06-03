# vue-click-outside
Vue directive for handling click outside event for any given element.

## Example

```vue
<template>
  <div>
    <div v-click-outside="hide" @click="isOutSideClicked = false">Hello</div>
    <div v-if="isOutSideHelloClicked">You Clicked outside hello!!!</div>
    <div v-else-if="isOutSideClicked === false">You Clicked inside hello!!!</div>
  </div>
</template>

<script>
import directivesClickOutside from 'vue-click-outside'

export default {
  data () {
    return {
      isOutSideClicked: null
    }
  },

  // this section is important to import directive
  directives: {
    'click-outside': directivesClickOutside
  },

  methods: {
    hide () {
      this.isOutSideClicked = true
    }
  }
}
</script>
```
