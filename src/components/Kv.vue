<template>
    <div class="section1">
      <div class="textArea">
        <img src="./../assets/img/images-kv-ai.png" class="aiImg">
        <span class="name">OPPO Reno12 Pro</span>
        <span class="color">给点银色瞧瞧</span>
      </div>
    </div>
</template>
<style lang="less" scoped>
    .section1 {
      height: 440px;
      width: calc(100%-128px);
      background-image: url('./../assets/img/images-kv-bg.jpeg'); /* 设置背景图 */
      background-size: cover; /* 背景图覆盖整个div区域 */
      background-position: center; /* 背景图居中显示 */
      background-repeat: no-repeat; /* 背景图不重复 */
      display: flex;
      align-items: center;
      padding: 0 64px;
      .textArea {
        display: flex;
        flex-direction: column;
        .aiImg {
          width: 140px;
          height: 30px;
        }
        .name {
          font-size: 32px;
          font-weight: bold;
          margin: 6px 0 0 0 ;
        }
        .color {
          font-size: 68px;
          font-weight: bold;
        }
      }
    }
</style>