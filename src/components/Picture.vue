<template>
    <div class="picture">
        <div class="block">
            <img src="./../assets/img/p1.jpeg" class="bgImg">
            <span class="text">超美小直屏</span>
            <span class="smallText fade-in-text">超时髦，超百搭</span>
            <img src="./../assets/img/down.png" class="downIcon">
        </div>
        <div class="block">
            <img src="./../assets/img/p2.png" class="bgImg">
            <span class="text">实况照片</span>
             <span class="smallText fade-in-text">我的照片起风了</span>
            <img src="./../assets/img/down.png" class="downIcon">
        </div>
        <div class="block">
            <img src="./../assets/img/p3.jpeg" class="bgImg">
            <span class="text fade-in-text">天玑星速，超能玑师</span>
            <span class="smallText fade-in-text">天玑 9200+ 星速版 旗舰芯片</span>
            <img src="./../assets/img/down.png" class="downIcon">
        </div>
        <div class="block">
            <img src="./../assets/img/p4.jpeg" class="bgImg">
            <span class="text">AI 影像，<br>一键拯救废片</span>
            <span class="smallText fade-in-text">AI 闭眼修复<br>AI 消除<br>AI 抠图<br></span>
            <img src="./../assets/img/down.png" class="downIcon">
        </div>
    </div>
</template>
<style lang="less" scoped>
.picture {
    height: 561px;
    width: calc(100%-128px);
    background: rgb(32, 31, 28);
    display: flex;
    justify-content: center;
    align-items: center;
    @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
    }
    padding:0 64px 60px 64px;
    .fade-in-text {
        opacity: 0;
        animation: fadeIn 0.4s ease-in-out forwards;
    }
    .block {
        width: 281px;
        height: 421px;
        border-radius: 24px;
        position: relative;
        cursor: pointer;
        transitiion-behavior: normal;
        transition-duration: 0.6s;
        transition-timing-function: ease;
        transition-delay: 0s;
        transition-property: width;
        &:hover {
            width: 328px;
            .smallText {
                display: inline;
            }
            .text {
                bottom: 30px;
            }
            &:last-child {
                .text {
                    bottom: 70px;
                }
            }
        }
        .bgImg {
            height: 100%;
            left: 0;
            -o-object-fit: cover;
            object-fit: cover;
            position: absolute;
            top: 0;
            width: 100%;
            border-radius: 24px;
        }
        &:not(:last-child) {
            margin-right: 7px;
        }
        .text {
            font-size: 24px;
            font-weight: bold;
            color: #fff;
            position: absolute;
            bottom: 10px;
            left: 12px;
            transition-duration: 0.6s;
            transition-timing-function: ease;
            transition-delay: 0s;
            transition-property: bottom;
        }
        .downIcon {
            height: 21px;
            width: 21px;
            position: absolute;
            bottom: 14px;
            right: 12px;
        }
        .smallText {
            display: none;
            font-size: 14px;
            font-weight: 400;
            color: rgba(255,255,255,.55);
            position: absolute;
            bottom: 10px;
            left: 12px;
        }
    }
}
</style>