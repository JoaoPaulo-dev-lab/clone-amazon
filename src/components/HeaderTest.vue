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
        <div style="display: flex; align-items: center;">
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
        
    </header>
  </div>
</template>

<script>
export default {
    name: 'HeaderTest',
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

    .logo-prime{
        max-width: 120px;
        margin-right: 15px;
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

</style>