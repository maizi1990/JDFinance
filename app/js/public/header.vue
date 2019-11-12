<template>
  <div :class="$style.header">
    <span :class="$style.left">
      <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
    </span>
    <btn :class="$style.btnDownload">APP下载</btn>
  </div>
</template>

<script>
import btn from "../core/btn.vue";
export default {
 
  components: {
    btn
  },
  
};
</script>

<style lang="scss" module>
.header {
 	height: 100px;
 	line-height: 100px;
 	color: #666;
 	position: fixed;
 	top: 0;
 	left: 0;
 	right: 0;
 	font-size: 28px;
 	background: url(http://m.jr.jd.com/spe/qyy/main/images/jr-logo.png) no-repeat center center #fff;
 	background-size: auto 50%;
 	.left{
 		margin-left: 18px;
 		height: 30px;
    	line-height: 30px;
 	}
 	.btnDownload {
 		float: right;
		font-size: 24px;
	    border-width: 0;
	    height: 56px;
	    line-height: 56px;
	    min-width: 120px;
	    padding: 0;
	    border-radius: 4px;
	    margin: 18px 24px 0 0;
 	}
}
</style>
