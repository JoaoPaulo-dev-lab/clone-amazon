<template>
  <div>
    <header>
        <div class="content-header-1">
            <div class="logo">
                <img class="logo-prime" src="../assets/prime.png"/>
            </div>
            <div class="menu-desktop">
                <ul>
                    <li>
                        <a class="border-target-selected" href="">Início</a>
                    </li>
                    <li>
                        <a href="">Filmes</a>
                    </li>
                    <li>
                        <a href="">Series</a>
                    </li>
                    <li>
                        <a href="">Infantil</a>
                    </li>
                </ul>
            </div>
        </div>
            <div class="menu-mobile">
                
                <a class="icon-menu">
                    <i @click="showMobileMenu = !showMobileMenu" class="fa fa-bars"></i>
                </a>
            </div>
        <div  class="search-container">
            <div class="content-header-2">
                    <h4>
                        <i class="fa fa-search"></i>
                    </h4>
                    <input class="inp" type="text" placeholder="Busca">
            </div>
            <div style="display: flex; align-items: center;" class="more-plus">
                <span>
                    <i class="fa fa-user"></i>
                </span>
                <span>
                     <i class="fa fa-caret-down"></i>
                </span>
            </div>
        </div>
        <div class="children-menu-mobile" v-if="showMobileMenu">
                    <ul>
                        <li>
                            <a href=""><i class="fa fa-home" style="margin-right: 3px"></i> Início</a>
                        </li>
                        <li>
                            <a href=""><i class="fa fa-film" style="margin-right: 3px"></i> Filmes</a>
                        </li>
                        <li>
                            <a href=""><i class="fa fa-video" style="margin-right: 3px"></i> Series</a>
                        </li>
                        <li>
                            <a href=""><i class="fa fa-children" style="margin-right: 3px"></i> Infantil</a>
                        </li>
                    </ul>
                </div>
    </header>
  </div>
</template>

<script>
export default {
    name: 'HeaderTest',
    data(){
        return {
            showMobileMenu: false,
        };
    },
    methods: {
        
    }
}
</script>

<style scoped>
    .border-target-selected{
        border-bottom: 2px solid #fff;
    }

    header{
        padding: 13px 3%;
        background: #0f171e;
        display: flex;
        justify-content: space-between;/*Separar os elementos irmãos*/
        align-items: center;
        position: relative;
    }
    
    header .content-header-1{
        display: flex;
        align-items: center;

    }

    header .content-header-2{
        display: flex;
        align-items: center;
        color: #fff;
        border: 1px solid rgb(156, 155, 155);
        padding: 4px 7px;
    }

    header .content-header-2 input{
        background-color: rgba(0, 0, 0, 0);
        outline: none;
        padding: 3px 6px;
        border: 0;
        font-weight: bold;
        font-size: 16px;
    }

    header .content-header-2 h4{
        color: rgb(156, 155, 155);
        margin-right: 5px;
    }

    header .more-plus {
        margin-left: 15px;
        color: #fff;
    }

    header .more-plus span{
        font-size: 16px;
        margin-right: 12px;
        cursor: pointer;
    }

    header .search-container{
        display: flex; 
        align-items: center;
    }

    .logo-prime{
        max-width: 120px;
        margin-right: 15px;
    }

    .menu-mobile{
        color: rgb(242, 244, 247, .9);
        font-size: 30px;
        display: none;
        cursor: pointer;
    }

    header .children-menu-mobile{
        position: absolute;
        width: 100%;
        top: 60px;
        left: 0;
        z-index: 90999000;
        background-color: #0f171e !important;
    }

    header .children-menu-mobile ul{
        width: 100%;
        display: flex;
        align-items: center;
        flex-direction:column;
    }

    .menu-desktop ul{
        display: flex;
        align-items: center;
    }

    .menu-desktop ul li{
        margin-left: 30px;
        list-style: none;
    }

    .menu-desktop ul li a{
        text-decoration: none;
        color: rgb(242, 244, 247, .9);
        font-weight: bold;
        letter-spacing: 2px;
    }

    .menu-desktop ul li span{
        color: rgb(242, 244, 247, .9);
        cursor: pointer;
    }
    
    @media screen and (max-width: 915px){
        header .menu-desktop{
            display: none;
        }
        header .search-container{
            display: none;
        }
        header .menu-mobile{
            display: flex;
        }
        /* Daqui em diante*/
        header .children-menu-mobile ul li{
            display: block;
            width: 100%;
            text-align: center;
            cursor: pointer;
        }
        header .children-menu-mobile ul li a{
            list-style: none;
            color: rgb(242, 244, 247, .9);
            font-weight: bold;
            letter-spacing: 1px;
            font-size: 16px;
            text-decoration: none;
            display: flex;
            padding: 20px 0;
            justify-content: center;
            border-bottom: 1px solid #284866;
            transition: 0.6s
        }

        header .children-menu-mobile ul li a:hover{
            background-color: #04101b;
        }
    }

    @media screen and (max-width: 400px) {
        header .logo-prime{
        max-width: 80px;
    }
    }
</style>