<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <btn
      additionalClass="btn--bg-secondary"
      textColor="btn--color-text-primary"
      textBtn="secondary text"
      btnSize="wewe"
    ></btn>
    <custom-select
      name="qwqw"
      id="etrt"
    >
      <option
        v-for="option in options"
        :value="option.text"
        :key="option.value"
      >
        {{ option.text }}
      </option>
    </custom-select>
    <popup>
      sdsd
    </popup>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld'
import Btn from '@/components/Buttons/Btn'
import CustomSelect from '@/components/Select/CustomSelect'
import Popup from '@/components/Popup/Popup'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Btn,
    CustomSelect,
    Popup
  },
  data () {
    return {
      selectedOption: 'fgg',
      options: [
        { text: 'Один', value: 'А' },
        { text: 'Два', value: 'Б' },
        { text: 'Три', value: 'В' }
      ]
    }
  }
}
</script>
<style lang="scss">
  .gatsby-highlight {
    margin-bottom: 1.75rem;
    border-radius: 10px;
    background: #011627;
    -webkit-overflow-scrolling: touch;
    overflow: auto;
  }
  .punctuation {
    color: #c792ea;
  }
</style>
