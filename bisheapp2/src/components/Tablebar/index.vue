<template>
<body>
    <div class="nav">
        <input type="checkbox">
        <span></span>
        <span></span>
        <div class="menu">
            <li><a href="#">home</a></li>
            <li><a href="#">about</a></li>
            <li><a href="#">main</a></li>
            <li><a href="#">main</a></li>
            <li><a href="#">main</a></li>
        </div>
    </div>
</body>
</template>

<script>
export default {

}
</script>

<style scoped>
body {
    margin: 0;
    padding: 0;
    width: 500px;
    height: 100px;
    /* min-height: 100vh; */
    background-color: rgb(255, 255, 255);
    font-family: 'Open Sans', Verdana, Geneva, Tahoma, sans-serif;
}
body , .nav , .menu {
     display: flex;
     justify-content: center;
     align-items: center;
 }
.nav{
    position: relative;
    background-color: #fff;
    padding: 20px ;
    transform: 0.5s;
    border-radius: 50px;
    overflow: hidden;
    box-shadow: 0 8px 15px rgba(0,0,0,.2);
}
.menu{
    margin: 0;
    padding: 0;
    width: 0;
    overflow: hidden;
    transition: .5s;
}
.nav input:checked ~ .menu{
    width: 450px;
}
.menu li{
    list-style: none;
    margin: 0 10px;
}
.menu li a{
   text-decoration: none; 
   color: #666;
   text-transform: uppercase;
   font-weight: 600;
   transition: .5s;
}
.menu li a:hover{
    color: #000;
}
.nav input{
    width: 40px;
    height: 40px;
    cursor: pointer;
    opacity: 0;
}
.nav span{
    position: absolute;
    left: 30px;
    width: 30px;
    height: 4px;
    border-radius: 50px;
    background-color: #666;
    pointer-events: none;
    transition: .5s;
}
.nav input:checked ~span{
    background-color: #f974a1;
}
.nav span:nth-child(2){
    transform: translateY(-8px);
    left: 25px;
}
.nav input:checked ~ span:nth-child(2){
    transform: translateY(0) rotate(-45deg);
}
.nav span:nth-child(3){
    transform: translateY(8px);
    left: 25px;
}
.nav input:checked ~ span:nth-child(3){
    transform: translateY(0) rotate(45deg);
}
</style>