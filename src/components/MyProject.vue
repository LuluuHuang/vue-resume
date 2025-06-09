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
        <a v-if="project.code" :href="project.code" class="code" target="_blank">
            原始碼
        </a>
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
                <a :href="project.link" target="_blank">
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
                    name:'旅遊網站',
                    link:'https://luluuhuang.github.io/tourWebVue/#/',
                    img:'./img/旅遊.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap5',
                        'SCSS',
                        'Vue3',
                        'RWD',
                    ],
                    code:'https://github.com/LuluuHuang/tourWebVue',
                },
                {
                    name:'小型POS系統',
                    link:'https://luluuhuang.github.io/pos-system/#/',
                    img:'./img/pos.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap5',
                        'SCSS',
                        'Vue3',
                        'RWD',
                    ],
                    code:'https://github.com/LuluuHuang/pos-system',
                },
                {
                    name:'電子喜帖網站',
                    link:'https://luluuhuang.github.io/HSwedding',
                    img:'./img/HSWedding.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'JavaScript',
                        'Bootstrap5',
                        'SCSS',
                        'RWD',
                    ],
                    code:'https://github.com/LuluuHuang/HSwedding',
                },
                {
                    name:'飯店官網',
                    link:'http://www.younglake.com.tw/',
                    img:'./img/水漾.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap3',
                        'JavaScript',
                        'jQuery',
                        'RWD',
                    ]
                },
                {
                    name:'電子零件公司官網',
                    link:'https://trumps.com.tw/',
                    img:'./img/創宇.jpg',
                    skill:[
                        'HTML',
                        'CSS',
                        'Bootstrap3',
                        'JavaScript',
                        'jQuery',
                        'RWD',
                    ]
                },
                {
                    name:'個人攝影工作室形象網站',
                    link:'https://luluuhuang.github.io/project-YTD/',
                    img:'./img/05-昨日攝影.jpeg',
                    skill:[
                        'HTML',
                        'JavaScript',
                        'CSS',
                        'SCSS',
                        'RWD',
                    ],
                    code:'https://github.com/LuluuHuang/project-YTD',
                },
                // {
                //     name:'中興新村現場導覽網站',
                //     link:'http://zrsi.beedemo.world/',
                //     img:'./img/中興.jpg',
                //     skill:[
                //         'HTML',
                //         'CSS',
                //         'Bootstrap3',
                //         'JavaScript',
                //         'jQuery',
                //         'RWD',
                //     ]
                // },
                // {
                //     name:'生技公司一頁式訂購網站',
                //     link:'http://www.fhmedical.com.tw/',
                //     img:'./img/芳和.jpg',
                //     skill:[
                //         'HTML',
                //         'CSS',
                //         'SCSS',
                //         'JavaScript',
                //         '紅陽金流'
                //     ]
                // }
            ]
        }
    }
}
</script>