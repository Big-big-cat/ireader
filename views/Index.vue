<template>
    <main id="main" class="container">
        <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
        <ol class="carousel-indicators">
            <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
            <li data-target="#carouselExampleIndicators" data-slide-to="3"></li>
        </ol>
        <div class="carousel-inner">
            <div class="carousel-item active">
            <img class="d-block w-100" src="img/index/banner1.png" alt="First slide">
            </div>
            <div class="carousel-item">
            <img class="d-block w-100" src="img/index/banner2.png" alt="Second slide">
            </div>
            <div class="carousel-item">
            <img class="d-block w-100" src="img/index/banner3.png" alt="Third slide">
            </div>
            <div class="carousel-item">
            <img class="d-block w-100" src="img/index/banner4.png" alt="4th slide">
            </div>
        </div>
        <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
        </a>
        <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
        </a>
        </div>
        <div>
        <h3 class="pb-3">
            <nav class="navbar navbar-light border-bottom border-secondary pb-0 mb-2">
            <a class="navbar-brand" href="#">
                <img src="img/index/computer_icon.png" class="d-inline-block align-top" alt="">
                首页推荐 / 1F
            </a>
            </nav>
            <div class="row mb-2">
            <div class="col-md-7">
                <div class="card border-0 flex-md-row box-shadow h-md-250">
                <div class="card-body d-flex flex-column align-items-start">
                    <h5 class="d-inline-block mb-2">{{res[0].title}}</h5>
                    <h6 class="mb-5">
                    <a class="text-dark" href="javascript:;">{{res[0].details}}</a>
                    </h6>
                    <span class="text-primary">¥{{res[0].price.toFixed(2)}}</span>
                    <router-link class="btn btn-primary" :to="`/details/${res[0].href.split('=')[1]}`">查看详情</router-link>
                </div>
                <img class="card-img-right flex-auto d-none d-md-block" data-src="holder.js/200x250?theme=thumb" :src="res[0].pic" data-holder-rendered="true">
                </div>
            </div>
            <div class="col-md-5 pl-0">
                <div class="card border-0 flex-md-row box-shadow h-md-250">
                <div class="card-body d-flex flex-column align-items-start">
                    <h5 class="d-inline-block mb-2">{{res[1].title}}</h5>
                    <h6 class="mb-5">
                    <a class="text-dark" href="javascript:;">{{res[1].details}}</a>
                    </h6>
                    <span class="text-primary">¥{{res[1].price.toFixed(2)}}</span>
                    <router-link class="btn btn-primary" :to="`/details/${res[1].href.split('=')[1]}`">查看详情</router-link>
                </div>
                <img class="card-img-right flex-auto d-none d-md-block mt-5" data-src="holder.js/200x250?theme=thumb" :src="res[1].pic" data-holder-rendered="true">
                </div>
            </div>
            </div>
            <div class="row mb-2">
            <div class="col-md-5">
                <div class="card border-0 flex-md-row box-shadow h-md-250">
                <div class="card-body d-flex flex-column align-items-start">
                    <h5 class="d-inline-block mb-3">{{res[2].title}}</h5>
                    <span class="text-primary">¥{{res[2].price.toFixed(2)}}</span>
                    <router-link class="btn btn-primary" :to="`/details/${res[2].href.split('=')[1]}`">查看详情</router-link>
                </div>
                <img class="card-img-right flex-auto d-none d-md-block mt-5" data-src="holder.js/200x250?theme=thumb" :src="res[2].pic" data-holder-rendered="true">
                </div>
            </div>
            <div class="col-md-7 pl-0">
                <div class="row pr-3">
                    <div class="col-md-4 p-0 pl-2" v-for="p of res.slice(-3)">
                    <div class="card border-0 text-center">
                        <img class="card-img-top" :src="p.pic">
                        <div class="card-body p-0 pr-1 pl-1">
                        <span class="d-inline-block">{{p.title}}</span>
                        <span class="text-primary small">¥{{p.price.toFixed(2)}}</span>
                        <router-link class="btn btn-primary" :to="`/details/${p.href.split('=')[1]}`">查看详情</router-link>
                        </div>
                    </div>
                    </div>
                <!--删除105~124行-->
                </div>
            </div>
            </div>
        </h3>
        </div>
        <ul class="nav nav-pills nav-fill mb-3">
        <li class="nav-item">
            <a class="nav-link" href="#">
            <img src="img/footer/icon1.png">
            <h6 class="text-muted">品质保障</h6>
            </a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="#">
            <img src="img/footer/icon2.png">
            <h6 class="text-muted">私人订制</h6>
            </a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="#">
            <img src="img/footer/icon3.png">
            <h6 class="text-muted">学员特供</h6>
            </a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="#">
            <img src="img/footer/icon4.png">
            <h6 class="text-muted">专属特权</h6>
            </a>
        </li>
        </ul>
        <div class="btn-group-vertical position-fixed" role="group" aria-label="Basic example">
        <button type="button" class="btn btn-secondary btn-sm border-light border-left-0 border-right-0">首页<br>推荐</button>
        <button type="button" class="btn btn-secondary btn-sm border-light border-left-0 border-right-0">最新<br>上架</button>
        <button type="button" class="btn btn-secondary btn-sm border-light border-left-0 border-right-0">热销<br>单品</button>
        </div>
  </main>
</template>
<script>
    export default { 
        data(){
            return {
                res:[
                  {title:"", price:0,href:""},
                  {title:"", price:0,href:""},
                  {title:"", price:0,href:""},
                ]
            }
        },
        created(){
//main.js : 
// import axios from 'axios'
// Vue.prototype.axios=axios;
//服务端: app.js中 22行:
  //http://localhost:8080
            this.axios.get("http://localhost:3000/index")
            .then(res=> this.res=res.data )
        }
    }
</script>
<style scoped>/*拷贝index.css*/
    /*定制每层楼中每张商品图片的大小*/
    #main>div:nth-child(2)>h3>div:nth-child(2)>div:first-child img{
    margin-left:-200px; 
    height: 250px;
    }
    #main>div:nth-child(2)>h3>div:nth-child(2)>div:last-child img{
    margin-left:-150px; 
    height: 200px;
    }
    #main>div:nth-child(2)>h3>div:nth-child(3)>div:first-child img{
    margin-left:-100px; 
    height: 150px;
    }
    #main>div:nth-child(2)>h3>div:nth-child(3)>div:first-child img{
    margin-left:-100px; 
    height: 150px;
    }
    #main>div:nth-child(2)>h3>div:nth-child(3)>div:last-child .card-img-top{
    height:95px;
    }
    #main>div:nth-child(2)>h3>div:nth-child(3)>div:last-child .card-body>span:first-child{
    font-size:.2em;
    }
    /*定制每张商品卡片的背景色*/
    #main>div:nth-child(2)>h3 .card{
    background-color:#e8e8e8;
    }
    /*定制电梯按钮的样式*/
    #main>.btn-group-vertical{
    top:100px;
    left:10px;
    }
    #main>.btn-group-vertical>.btn-secondary:hover {
    background-color: #e4393c;
    border-color: #e4393c;
    }
</style>