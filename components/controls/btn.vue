<template>
  <button
    class="btn"
    :class='setClass'
    :type='type'
    @click="callback($event)"

   >
    {{ name }}

  </button>
</template>

<script>
import "@/assets/css/btn.scss"

export default {
  name: "Btn",
  props: {
    type: String,
    name: String,
    // Btn type
    darkBtn: Boolean,
    gradientBtn: Boolean
  },
  methods: {
    callback: function(e) {
      this.$emit('click', e);
    }
  },
  computed: {
    setClass(){
      const typeBtn = this.darkBtn
      ? "darkBtn"
      : this.gradientBtn
      ? "gradientBtn"
      : ""
      return "btn_" + typeBtn
    }
  }
}
</script>
