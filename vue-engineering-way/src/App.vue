<script setup>
    
</script>


<template>
<div class='bit-banner'>
  <img src="https://bit-1256306791.cos.ap-chengdu.myqcloud.com/fffa10ace4b071da45d9a0c4.jpg" 
  alt="比特轮播图" />

  <div class="ctrl">
    <a href="javascript:;" class="btn pre">&lt;</a>

    <a href="javascript:;" class="btn next">&gt;</a>
  </div>

</div>
</template>


<style scoped>

  .bit-banner {
    position: relative;
    width: 1200px;
    height: 337px;
    margin: 150px auto;
  }

  .bit-banner .ctrl .btn {
		position: absolute;
		top: 50%;
		width: 30px;
		height: 30px;
		margin-top: -15px;
		font-size: 14px;
		line-height: 30px;
		text-align: center;
		border-radius: 50%;
		background: rgba(0, 0, 0, 0.3);
	}

  .bit-banner .ctrl .btn.prev {
		left: 15px;
	}

	.bit-banner .ctrl .btn.next {
		right: 15px;
	}
</style>
