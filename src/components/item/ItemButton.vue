<script>
export default {
  name: "ItenButton ",
  data(){
    return{
      bgColor: null,
      textColor: null,
      borderColor:null,
    };
  },
  props: {
    text: String,
    color:String
  },
  created(){
    if(this.color === "lighter"){
      this.bgColor = "bg_lighter";
      this.textColor = "text_dark";
      this.borderColor ="border-dark";
    }else{
      this.bgColor = "bg_primary";
      this.textColor = "text_light";
      this.borderColor ="border-light";
    }
  }
};

</script>

<template>
  <button :class="bgColor" class="d-flex align-items-center p-0 py-2 me-3">
    <div :class="[textColor, borderColor]" class="px-4 fw-bold border-end border-1 py-1">{{text}}</div>
    <div :class="textColor" class="px-2 fs-6 py-1">&#10230</div>
  </button>
</template>

<style lang="scss" scoped>
  button{
    font-size: 0.8rem;
    width: 165px;
    border: none;
  }
  button:hover{
    div{
      padding-right: 0 !important;
      border-right: none !important;
    }

  }

</style>
