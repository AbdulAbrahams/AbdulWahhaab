<template>
    <div class="space"></div>
    <h1 class="proHead">Projects</h1>
        <div class="body">
            <div class="row justify-content-center mx-2">
                <div class="card mx-2 my-3" v-for="content in projects">
            <div class="poster">
                <img :src="content.image" alt="">
            </div>
            <div class="details">
                <h2>{{ content.name }}</h2>
                <div class="buttons">
                    <a :href="content.github"><button class="mx-3 p-1">GitHub</button></a>
                    <a :href="content.netlify"><button class="mx-3 p-1 px-2">Live</button></a> 
                </div>
            </div>
        </div> 
            </div>
           
        </div>
    </template>
    
    <script>
         export default {
            methods: {
          scrollTop() {
            document.body.scrollTop = document.documentElement.scrollTop = 0;
          }
        },
            name:'Projects',
            data(){
                return{
                    projects:[
                         {
                            name: 'Supremium E-commerce Store',
                            image: 'https://i.postimg.cc/brg8q9sX/pics.png',
                            netlify: 'https://supremium100.web.app/',
                            github: 'https://github.com/AbdulAbrahams/Capstone.git'
                        },
                        {
                            name: 'Old Portolio',
                            image: 'https://i.postimg.cc/3J3mdYyG/Screenshot-2023-01-12-134548.png',
                            netlify: 'https://abdulwahhaab.netlify.app/',
                            github: 'https://github.com/AbdulAbrahams/ProjectPortfolio.git'
                        },
                        {
                            name: 'JavaScript Calculator',
                            image: 'https://i.postimg.cc/QMnLHPxq/Screenshot-2023-01-11-153133.png',
                            netlify: 'https://abdulcalculator.netlify.app/',
                            github: 'https://github.com/AbdulAbrahams/calculator.git'
                        },
                        {
                            name: 'Sneaky Kicks Store',
                            image: 'https://i.postimg.cc/vmqHY4dc/Screenshot-2023-01-11-151336.png',
                            netlify: 'https://sneakykickscpt.netlify.app/',
                            github: 'https://github.com/AbdulAbrahams/JS-project.git'
                        },
                        {
                            name: 'Comic Strip',
                            image: 'https://i.postimg.cc/CLKKtynF/saitama.png',
                            netlify: 'https://saitamavsgoku.netlify.app/',
                            github: 'https://github.com/AbdulAbrahams/comic.git'
                        },
                        {
                            name: 'Exclusive Kicks',
                            image: 'https://i.postimg.cc/BnBP95Q3/exclusive.png',
                            netlify: 'https://exclusivekicks.netlify.app/',
                            github: 'https://github.com/AbdulAbrahams/exclusive-kicks.git'
                        }
                    ]
                }
            }
        }
    </script>
    
    <style scoped>

    .proHead{
        text-align: left;
        mix-blend-mode: difference;
        font-size: clamp(3.4rem, 5vw, 6.5rem);
    }
    .body{
        display: flex;
        justify-content: center;
        align-items: center;
        overflow-x: hidden;
    }
    .card{
        background-color: transparent;
        position: relative;
        max-width: 400px;
        height: 250px;
        overflow: hidden;
        border-radius: 10px;
        border: 0px;
    }
    .card .poster{
        position: relative;
        overflow: hidden;
    }
    .card .poster::before{
        content: '';
        position: absolute;
        bottom: -100px;
        width: 100%;
        height: 100%;
        background: linear-gradient(0deg,rgb(0, 0, 0) 40%, transparent);
        transition: 0.5s;
        z-index: 1;
    }
    .card:hover .poster::before{
        bottom: 0px;
    }
    .card .poster img{
        width: 100%;
        height: 35vh;
        transition: 0.5s;
    }
    .card:hover .poster img{
        filter: blur(8px);
    }
    .card .details{
        position: absolute;
        width: 100%;
        left: 0;
        bottom: 0;
        z-index: 2;
        padding: 20px;
        transition: 0.5s;
    }
    .card .details .buttons{
        position: absolute;
        width: 100%;
        left: 0;
        bottom: -60px;
        z-index: 2;
        padding: 20px;
        transition: 0.5s;
        background: transparent;
        color: white;
    }
    .card:hover .details{
        bottom: 50px;
    }
    .card .details h2{
        color: rgb(255, 255, 255);
        font-size: 31px;
    }
    .card .details .buttons{
        margin-top: 15px;
    }
    .details .buttons a button{
        background: rgb(0, 0, 0);
        border: 2px solid rgb(255, 255, 255);
        color: rgb(255, 255, 255);
    }
    .details .buttons a button:hover{
        background: rgb(255, 255, 255);
        border: 2px solid rgb(255, 255, 255);
        color: rgb(0, 0, 0);
        transition: 0.3s;
    }
    @media screen and (width <600px){
        .proHead{
            margin-top: 20% !important;
        }
    }
    </style>