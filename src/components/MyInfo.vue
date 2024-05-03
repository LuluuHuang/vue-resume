<template>
    <div class="row sec1 d-flex justify-content-center align-items-center">
        <div class="col-lg-4 col-md-7 col-sm-8 col-8 p-4">
            <img :src="infos.pic" alt="" class="mb-3"/>
            <p class="fs-2 chName fw-bolder">{{infos.name}}</p>
            <p class="fs-3 engName">{{infos.engName}}</p>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-6 col-12 animate__animated animate__fadeInUp">
            <p class="fs-3 btnStyle">技能</p>
            <ul v-for="(skill,i) in infos.skills" class="skills" :key="i">
                <li>{{skill}}</li>
            </ul>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-6 col-12 animate__animated animate__fadeInUp animate__delay-1s">
            <p class="fs-3 btnStyle">工作經歷</p >
            <ul v-for="(exp,i) in infos.experience" class="exp" :key="i">
                <li>{{exp}}</li>
            </ul>
            <p class="fs-3 btnStyle">學歷</p>
            <ul class="edu">
                <li>{{infos.educate}}</li>
            </ul>
        </div>
    </div>
</template>
<script>
    export default {
        data(){
            return{
                bgImg:'/img/bg2.jpg',
                infos:{
                    name:'黃堉茹',
                    engName:'Lulu Huang',
                    pic:'/img/lu.jpg',
                    skills:[
                        'JavaScript',
                        'HTML',
                        'CSS',
                        'SCSS',
                        'Vue.js',
                        'Bootstrap',
                    ],
                    experience:[
                        '長林創新股份有限公司 前端工程師',
                        '汨宇國際有限公司 行銷專員',
                        '霧峰區戶政事務所 行政助理'
                    ],
                    educate:'世新大學 公共關係暨廣告學系 畢業'
                }
            }
        }
    }
</script>