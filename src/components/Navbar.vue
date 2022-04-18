<template>
    <div class="navbar">
        <div class="nav-container">
            <div class="left-side">
                <ul class="icons-left-side icons">
                    <li><i class="icon fa-regular fa-calendar"></i></li>
                    <li><i class="icon fa-regular fa-message"></i></li>
                    <li><i class="icon fa-regular fa-envelope"></i></li>
                    <li><i class="icon fa-regular fa-calendar-check"></i></li>
                    <li class="star" @click= "toggle"  >
                        <i class="icon fa-regular fa-star"></i>
                        <ul class="star-menu dNone" id="child" >
                                <li class="star-search"><input type="search" placeholder="Explore Vuexy..." ></li>
                                <li class="hov"><i class="icon  star-icon fa-regular fa-message"></i><span>Chat</span><i class="icon list-icon fa-regular fa-star"></i></li>
                                <li class="hov"><i class="icon  star-icon fa-regular fa-calendar"></i><span>Calendar App</span><i class="icon list-icon fa-regular fa-star"></i></li>
                                <li class="hov"><i class="icon  star-icon fa-regular fa-envelope"></i><span>Email</span><i class="icon list-icon fa-regular fa-star"></i></li>
                                <li class="hov"><i class="icon  star-icon fa-regular fa-calendar-check"></i><span>Todo</span><i class="icon list-icon fa-regular fa-star"></i></li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="right-side">
                <ul class="icons-right-side icons">
                    <li><img class="imag"  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAAA1CAMAAACA7r40AAAA/FBMVEWyIjNPN2Y8O27///8/PnBOTXxycpY9PG9RUX5HR3dIR3dLSnlPTny4uMpWVYFFRHVwb5VlZIx7e52DgqOIh6aIiKc+PXBJSHhTUn9hYYqyIjReXohgX4lYV4Lr6/C2tcjPdYB0c5haWYRYV4Nra5GJiac+PW/FxdTHYG1RUH3eoajltbtOTXvty89BQHHg3+hSUX6GYoC6usyVlbFycZa7u8yUk6+sq8FCQXO0tMe1tMhiYYpMS3pDQnNvbpTExNN8fJ7GxdTGxtWCgqLHx9WXlrLXi5SYl7Kiobrg4Oiiorrn5u3n5+2jo7ukpLvw8PTx8fX09Pf19firqsC5sMNxAAAAAnRSTlPQ9qN1Xw4AAAGlSURBVHhe7ZXFiiRBFEVjznvp5W7t7j3u7m7//y8D1dAMGbnI4jW5KOpsgjibCxFcrrtVEmcBGAGQJHB98d3EgEM/ygsg/nwRAy15rxQ4Ywh3JQX49hVgKA/Ad1hDkkGTMSQJjGkOEmo133FmwAEQyl8FfSj3gFgkzjsQAw6AZ796AP2fGcDBS8/ZQ7ZQlJ2d+bEFqp6zhuh9Cf9/pDtKkTs04KBTD4jgx3eICOodoshz1p7M6UUAUQ+Ap2Pf2UMI5UBBX18/Ut7ZQ84Jui10QKsbcA7dt77jxIBDt+sxMNzrD4HL+rZS4Iw9iTZkCjRFmsBUHkcUOGMI7dkpKezuQsrprM3zR76zN572ekdBX623gaONJ0d5B5sGHAA1+QTwRQJgX2Q/7+w9GZGlDZKERpoxgkbDc8s0WscGSo+WGMiNVlgwWuFNjdafPsDe7wzg3RvP2UNCFGVtbX6EoOo7PhgoO1rGnswHiquB4mqgfIcxpBTGkNslMf2JVMAShRxXgJtUwBKFbFbAqicL4U4qYNWThXCHFbDqyUK4swpY9WQhXBX8A2rVjaQ6HWXmAAAAAElFTkSuQmCC" alt="en" width="22" height="14"></li>
                    <li><span class="span english">English</span></li>
                    <li><i class="icon fa-regular fa-moon"></i></li>
                    <li><i class="icon fa-solid fa-magnifying-glass"></i></li>
                    <li class="shop-cart"><i class="icon  fa-solid fa-cart-shopping"></i></li>
                    <li class="noti"><i class="icon fa-regular fa-bell"></i></li>
                    <li class="john-word"><span class="span doe">John Doe</span><span class="span admin">admin</span></li>
                    <li class="user"><span class="imgg"><img class="imag" src="https://pixinvent.com/demo/vuexy-vuejs-admin-dashboard-template/demo-1/img/13-small.d796bffd.png"></span></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="shop-container">
        <div class="shop">
        <h2>Shop</h2>
        <ul class="shop-icons">
            <li><i class="fa-solid house fa-house"></i></li>
            <li><i class="fa-solid fa-angle-right"></i></li>
            <li class="ecom">ECommerce</li>
            <li class="arrow2"><i class="fa-solid  fa-angle-right"></i></li>
            <li class="shp">Shop</li>
        </ul>
    </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
        }
    },
    methods : {
        toggle : function (){
            document.getElementById("child").classList.toggle("dNone")
        }
    }

}
</script>

<style>
.navbar{
    position: fixed;
    direction: ltr;
    flex-direction: row;
    margin:18.2px 28px 0px 288px;
    padding: 0px;
    display: flex;
    justify-content: flex-end;
    border: 1px solid #ebe9f1;
    border-radius: .428rem;
    z-index: 11;
}
.nav-container{
    box-sizing: border-box;
    border-radius: .428rem;
    display: flex;
    width: 1201.2px;
    height: 62.4px;
    font-size: 14px ;
    font-weight: 400;
    line-height: 20.3px;
    padding: 11.2px 14px;
    letter-spacing: 0.14px;
    text-align: left;
    align-items: center;
    background-color: white;
    box-shadow: 0 2px 8px 0 rgb(34 41 47 / 14%);
    
}
.left-side{
    box-sizing: border-box;
    width: 761.862px;
    font-size: 14px;
}
.right-side{
    margin-left: 80px;
    margin-top: 0px;
    padding-right:12.5px ;
    width: 439.338px;
    display: flex;
    justify-content: flex-end;


}

.icons-left-side, .icons-right-side{
    display: flex;
    align-items: center;
    height: 40px;
    padding: 0px;
    font-size: 13px;
    list-style: none;
}
.imag{
    padding:0px 7px ;
    margin-top: 4px;
}

.icon{
    box-sizing: border-box;
width: 21px ;
height: 22.1px;
font-size: 14px;
padding: 0px 7px;
}
.star{
    position: relative;
    color: #ff9f43;
}
.star ul{
    color: #6e6b7b;

}
.span{
    display: block;
    padding: 0px 7px;
    letter-spacing: 1px;
}
.user{
    width: 40px;
}
.noti{
    position: relative;
}
.star-menu{
    padding:7px  0px ;
    width: 300px;    
    list-style: none;
    background-color: white;
    border: 1px solid #ebe9f1;
    position: absolute;
    left: 0px;
    top: 50px;
    border-radius: .357rem;
}
.dNone{
        display: none;
}
ul li{
    cursor: pointer;
}
.noti::before{
    content: '';
    position: absolute;
    bottom: 17px;
    left:17px;
    border: 9.5px solid transparent;
    border-radius:50% ;
    /* transform: translateY(-90%); */
    /* transform: translateX(-70%); */
    border-color: #ea5455 ;
}
.noti::after{
    content: '6';
    position: absolute;
    bottom: 16px;
    left:22px;
    font-size: 12px;
    font-weight: 600;
    color: white;
}

.shop-cart{
    position: relative;
}
.shop-cart::before{
    content: '';
    position: absolute;
    bottom: 17px;
    left:17px;
    border: 9.5px solid transparent;
    border-radius:50% ;
    border-color: #7367F0 ;
}
.shop-cart::after{
    content: '5';
    position: absolute;
    bottom: 16px;
    left:23px;
    font-size: 12px;
    font-weight: 600;
    color: white;
}

.john-word{
    line-height: 14px;
    padding-left: 2px;
    display: flex;
    flex-direction: column;
}
.star-menu li{
    padding: 9.1px 11px  ;
    height: 23.5px;
    
}
.hov{
    
    height: 23.5px;
}
.hov:hover{
    background-color: #7267f044;
}
.star-menu .star-search{
    padding: 14px;
    padding-bottom:20px ;    
}
.star-menu .star-search input{
    padding: .438rem 1rem;
    height: 37.99px;
    background-color: #fff;
    border: 1px solid #d8d6de;
    border-radius: .357rem;
    width: 100%;
    font-size: 14px;
}
::-webkit-input-placeholder{
    color: #BEBEC8;
}
.star-icon{
    width: 18px;
    height: 18px;
}
.list-icon{
    float: right;
    width: 16px;
}
.admin{
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 0px;
    margin-left:60%;
    transform: translateX(-60%);}
.imgg img{
    width: 40px;
    height: 40px;
    border-radius:50% ;
}
.imgg{
position: relative;
}
.imgg::after{
    content: '';
    position: absolute;
    top:2.5px;
    left:35.5px;
    border: 5px solid transparent;
    border-radius:50% ;
    border-color: #28C76F ;
}
.doe{
    font-weight: bold;
}
.english{
    letter-spacing: 0px;
    font-size: 14px;
    font-weight: 420;
}
.shop-container{
    position: absolute;
    display: flex;
    width: 895.400px;
    height: 33.4px;
    margin:108.5px 28px 0px 288px;
}
.shop h2 {
    margin-top: 0;
    width: 63.400px;
    height: 28.8px;
    border-right: 1px solid #d6dce1;
    padding-right: 14px;
    color: rgb(99, 99, 99);
    font-size: 23.996px;
    font-weight: 500;
}
.shop-icons{
    display: flex;
    list-style: none;
    margin-top: 4.5px;
    padding-left: 14.5px;
}
.shop-icons li{
    width: 0;
    padding-right:25.5px ;
    font-size: 12px;
    padding-top: 3px;
}
.house{
    font-size: 14px;
    color: #7367f0;
}
.shop{
    display: flex;
    
}
.shop-icons .ecom{
    width: 75px;
    margin-left: -10px;
    font-size: 14px;
    color: #7367f0;
}
.shop-icons .shp{
    font-size: 14px;
    color: #6e6b7b;
}
.shop-container .arrow2{
    padding-right: 15px ;
}
</style>