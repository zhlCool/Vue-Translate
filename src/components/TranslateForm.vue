<template>
  <div class="row" id="translateForm">
    <div class="col-md-6 col-md-offset-3">
      <form id="transFrom" class="well form-inline" v-on:submit="formSubmit">
        <input class="form-control" type="text" v-model="textToTranslate" placeholder="请输入需要翻译的内容">
        <select class="form-control"  v-model="language">
          <option value="en">English</option>
          <option value="zh">Chinese</option>
          <option value="fr">French</option>
          <option value="ru">Russian</option>
          <option value="ko">Koream</option>
          <option value="ja">Janpenese</option>
          <option value="az">Azerbaijan</option>
          <option value="sq">Albanian</option>
          <option value="am">Amharic</option>
          <option value="ar">Arabic</option>
          <option value="hy">Armenian</option>
          <option value="tr">Turkish</option>
          <option value="it">Italian</option>
        </select>
        <input class="btn btn-primary" type="submit" value="翻译">
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: 'translateForm',
  data:function(){
    return{
      textToTranslate:'',
      language:''
    }
  },
  methods:{
    formSubmit:function(e){
        this.$emit("formSubmit",this.textToTranslate,this.language);
        e.preventDefault();
    }
  },
  created:function(){
      this.language = "en";
  }
}
</script>
<style>
#transFrom{
 border:1px solid #ccc;
 border-radius:10px;
}
</style>
