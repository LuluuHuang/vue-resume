<template>
    <div class="row sec1 d-flex justify-content-center align-items-center">
        <div class="col-lg-4 col-md-7 col-sm-8 col-8 p-4">
            <img :src="infos.pic" alt="" class="mb-3"/>
            <p class="fs-2 chName fw-bolder">{{infos.name}}</p>
            <p class="fs-3 engName">{{infos.engName}}</p>
            <p><a :href="infos.github" target="_blank"><i class="bi bi-github"></i></a></p>
            
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
                <li>{{exp.time}}</li>
                <li>{{exp.job}}</li>
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
                bgImg:'./img/bg2.jpg',
                infos:{
                    name:'黃堉茹',
                    engName:'Lulu Huang',
                    github:'https://github.com/LuluuHuang',
                    pic:'./img/lu.jpg',
                    skills:[
                        'HTML',
                        'CSS',
                        'JavaScript ES6',
                        'Vue3',
                        'SCSS',
                        'Bootstrap',
                        'Git',
                        'Figma',
                    ],
                    experience:[
                        {
                            job:'微樂應用科技有限公司 前端工程師',
                            time:'2024/10~今'
                        },
                        {
                            job:'長林創新股份有限公司 前端工程師',
                            time:'2023/2~2024/6'
                        },
                        // {
                        //     job:'汨宇國際有限公司 行銷專員',
                        //     time:'2022/3~2022/8'
                        // },
                        // {
                        //     job:'霧峰區戶政事務所 行政助理',
                        //     time:'2020/2~2021/10'
                        // }                        
                    ],
                    educate:'世新大學 公共關係暨廣告學系 畢業'
                }
            }
        }
    }
</script>