<template>
    <div id="home">
        <nav>
            <div>
                <img src="favicon.ico" alt="">
                <div>部署测试</div> 
            </div>
            <ul>
                <li>主页</li>
                <li>联系</li>
                <li>关于</li>
            </ul>
        </nav>


        <div class="title">
        <div><a href="https://www.browserstack.com">BrowserStack</a>
        <div>BrowserStack 是著名的:多系统跨浏览器兼容性测试平台，平台每次注册后提供30分钟的试用，以后就会收费，针对这个问题，有人制作了小工具，集成了一键注册登陆功能，省去了每次手工注册的时间，为WEB网页开发人员提供方便。</div>

        </div>
        <div><a href="https://www.github.com">GitHub Actions</a>
        <div>大家知道，持续集成由很多操作组成，比如抓取代码、运行测试、登录远程服务器，发布到第三方服务等等。GitHub 把这些操作就称为 actions。很多操作在不同项目里面是类似的，完全可以共享。GitHub 注意到了这一点，想出了一个很妙的点子，允许开发者把每个操作写成独立的脚本文件，存放到代码仓库，使得其他开发者可以引用。如果你需要某个 action，不必自己写复杂的脚本，直接引用他人写好的 action 即可，整个持续集成过程，就变成了一个 actions 的组合。这就是 GitHub Actions 最特别的地方。</div>

        </div>
        <div><a href="https://aws.amazon.com/cn">AWS</a>
        <div>亚马逊云科技 - 亚马逊公司旗下云计算服务平台,为世界各地的客户提供一整套基础设施和云解决方案. 亚马逊云科技面向用户提供整套云计算服务,能够帮助企业降低IT投入成本和维护成本, 轻松上云.</div>
        </div>
        </div>

        <div id="btn">
              <button @click="alertInfo">
            点击一下，弹窗
            </button>
        </div>
      
     
      
    </div>
    
</template>

<script>
export default {
    methods:{
        alertInfo(){
            confirm('弹出测试信息')
        }
    }

}
</script>

<style scoped lang='less'>
nav{
    height:50px;
    border-bottom:1px solid #ccc;
    >div{
        float: left;
        padding-top:6px;
        padding-left:100px;
        >div{
            float:right;
            padding-left:20px;
            line-height:28px;
            color:#567;
            font-size:23px;
        }
        
    }
 
    >ul{
        list-style-type: none;
        float: right;
        li{
            float:left;
            line-height: 20px;
            font-size:21px;
            cursor: pointer;
            color:green;
            padding-right: 50px;
            &+li{
                color:#000;
            }
            &:last-child{
                padding-right: 120px;
            }
            &:hover{
                color:green;
            }
        }
    }
}

.title {
    display: flex;
    justify-content: space-around;
    margin-top:150px;
    width:100%;
    height:300px;
    margin-left:200px;
    >div{
        width:120px;
        height:30px;
        background:#fff;
        border-radius:6px;
        cursor: pointer;
        color:#000;
        line-height: 30px;
        text-align:center;
        border:1px solid green;
        >div{
            margin-top: 30px;
            height: 150px;
            overflow: hidden;
            border:1px solid green;
            border-radius: 5px;
            font-size:14px;
            line-height:25px;
        }
        a{
            text-decoration: none;
            color:#000;
        }

    }
    >div:hover{
        background: green;
        border:.11px solid #fff;
        box-shadow: 1px 1px 3px 3px #ccc;
        a{
            color:#fff;
        }
        >div{
            color:#000;
            line-height:25px;
            transform: scale(1.1);
            transition: transform .1s;
        }
    }
} 
nav::after{
    content:'';
    display: table;
    clear:both;
}
.title::after{
    content:'';
    display: table;
    clear:both;
}

#btn{
    width:120px;
    text-align: center;
    margin:100px auto;
    >button{
        width:120px;
        height:36px;
        background:green;
        color:#fff;
        outline: none;
        border:none;
        border-radius:5px;
        &:active{
            box-shadow: 2px 2px 2px 2px #999;
        }
    }
}

</style>
