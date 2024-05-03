<template>
    <div class="row sec2">
        <div class="col-12 d-flex justify-content-center sec2Title">
            <p class="fs-1">{{title}}</p>
        </div>
        <div
            class="col-lg-4 col-md-6 col-sm-12 work"
            v-for="project in projects"
            :key="project.name"
        >
            <div class="work_content">
                <p>{{project.name}}</p>
                <div class="underline"></div>
                <div class="pillcontainer">
                    <span
                    v-for="(item,i) in project.skill"
                    class="badge rounded-pill bg-secondary m-1"
                    :key="i"
                    >{{item}}</span
                >
                </div>
                <a :href="project.link">
                    <div
                    class="pic"
                    :style="{ 'background-image': 'url(' + project.img + ')' }"
                    ></div>
                </a>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            title:'Portfolio',
            projects:[
                {
                    name:'個人攝影工作室形象網站',
                    link:'https://luluuhuang.github.io/project-YTD/',
                    img:'/img/05-昨日攝影.jpeg',
                    skill:[
                        'HTML',
                        'JavaScript',
                        'CSS',
                        'SCSS'
                    ]
                },
                {
                    name:'飯店官網',
                    link:'http://www.younglake.com.tw/',
                    img:'/img/水漾.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap3',
                        'JavaScript',
                        'jQuery',
                        'C#',
                        'ASP.NET MVC'
                    ]
                },
                {
                    name:'電子零件公司官網',
                    link:'https://trumps.com.tw/',
                    img:'/img/創宇.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap3',
                        'JavaScript',
                        'jQuery',
                        'C#',
                        'ASP.NET MVC'
                    ]
                },
                {
                    name:'中興新村現場導覽網站',
                    link:'http://zrsi.beedemo.world/',
                    img:'/img/中興.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap3',
                        'JavaScript',
                        'jQuery',
                        'C#',
                        'ASP.NET MVC'
                    ]
                },
                {
                    name:'生技公司一頁式訂購網站',
                    link:'http://www.fhmedical.com.tw/',
                    img:'/img/芳和.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'SCSS',
                        'JavaScript',
                        '串金流'
                    ]
                },
                {
                    name:'旅遊網站',
                    link:'https://luluuhuang.github.io/tourWeb/',
                    img:'/img/旅遊.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'SCSS',
                        'JavaScript'
                    ]
                },
                {
                    name:'微軟官網仿切',
                    link:'https://luluuhuang.github.io/microsoft/',
                    img:'/img/06-微軟仿切.png',
                    skill:[
                        'HTML',
                        'CSS',
                        'SCSS'
                    ]
                },
                {
                    name:'簡易零售POS系統',
                    link:'#',
                    img:'',
                    skill:[
                        'HTML',
                        'CSS',
                        'SCSS',
                        'Vue.js'
                    ]
                }
            ]
        }
    }
}
</script>