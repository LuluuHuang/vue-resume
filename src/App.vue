<script>
// import { RouterLink, RouterView } from 'vue-router'
import MyInfo from './components/MyInfo.vue'
import MyProject from './components/MyProject.vue'
import MyFooter from './components/MyFooter.vue'

export default{
    components:{
        MyInfo,
        MyProject,
        MyFooter
    }
}
</script>

<template>
    <div class="bg">
        <div class="container">
        <MyInfo></MyInfo>
        <MyProject></MyProject>
        </div>
        <div class="container-fluid p-0">
            <MyFooter></MyFooter>
        </div>
    </div>
</template>

<style lang="scss">
    @import"./assets/all.scss";

    .bg{
        background-image: url('/img/bg2.jpg');
        background-size: cover;
        background-position: center;
    }
.sec1{
    height: 90vh;
    img{
        width: 100%;
        clip-path: circle(50% at 50% 50%);
    }
    p{
        text-align: center;
        margin: 0;
        a{
            color: black;
            i{
                font-size: 30px;
            }
        }
    }
    .engName,.skills{
        font-family:Times New Roman;
    }
    ul{
        margin: 0;
        padding: 0;
        list-style: none;
        text-align: center;
        li{
            font-size: 20px;
        }
    }
    .btnStyle{
        margin: 5% 20%;
        border-radius: 30px;
        background-color: #c99a93;
        color: white;
        cursor:pointer;
    }
}
.sec2{
    display: flex;
    overflow: hidden;
    .sec2Title{
        font-family:Times New Roman;
        p{
            position: relative;
            z-index: 0;
            width: fit-content;
        }
    }
    .sec2Title>p::before{
        content: '';
        position: absolute;
        z-index: -1;
        left: -10px;
        top: 2px;
        width: 52px;
        height: 52px;
        border-radius: 50%;
        background-color: #c99a93;
    }
    .work{
        padding: 20px;
        height: 400px;
        position: relative;
        .code{
            position: absolute;
            left: 0;
            top: 0;
            z-index: 1;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background-color: #c99a93;
            display: flex;
            justify-content: center;
            align-items: center;
            text-decoration:none;
            color: white;
        }
        .work_content{
            background-color: rgba(255, 255, 255, 0.8);
            border: 1px solid rgba(163, 161, 161, 0.5);
            border-radius: 10px;
            box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
            height: 100%;
            overflow: hidden;
            position: relative;
            p{
                text-align: center;
                font-size: 1.5em;
                font-weight: 700;
                margin: 10px 0 5px 0;
                height: 10%;
            }
            .underline {
                position: absolute;
                left: 50%;
                width: 0;
                height: 2px;
                background-color: rgba(163, 161, 161, 0.5);
                transform: translateX(-50%);
                transition: width 0.5s ease;
            }
            .pic{
                border-radius: 0 0 10px 10px;
                height: 70%;
                background-size: cover;
                background-position: top;
                background-repeat: no-repeat;
            }
            .pillcontainer{
                margin: 15px 10px 0 10px;
                height: 20%;
                font-family:Times New Roman;
                span{
                    background-color: antiquewhite;
                }
            }

        }
    }
    .work{
        .work_content:hover{
            .underline {
                width: 80%;
            }
            .pic{
                scale: 1.05;
                transition-duration: 0.6s;
            }
        }
        
    }
}
footer{
    background-color: #c99a93;
}
@media screen and (max-width: 960px) {
    .sec1 {
      /* 在手機版時的樣式 */
      height: auto; /* 或是設定其他適合手機螢幕的高度 */
    }
    .sec2{
        padding-top: 50px;
    }
}
</style>
