<template>
    <a href="#" class="btn btn-white btn-animated">Discover our tools</a>
</template>
<style scoped>
.btn:link,
.btn:visited {
    text-transform: uppercase;
    text-decoration: none;
    padding: 15px 40px;
    display: inline-block;
    border-radius: 100px;
    transition: all .2;
    position: relative;
}

.btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, .2);
}

.btn:active {
    transform: translateY(-1px);
    box-shadow: 0 5px 10px rgba(0, 0, 0, .2);
}
.btn-white {
    background-color: #fff;
    color: #777;
}
.btn::after {
 content: '';
 display: inline-block;
 height: 100%;
 width: 100%;
 border-radius: 100px;
 z-index: -1;
 position: absolute;
 top: 0;
 left: 0;
 transition: all .4s;
}

.btn-white::after {
    background-color: #fff;
}

.btn:hover::after {
    transform: scale(1.5);
    opacity: 0;
}
@keyframes animate {
    0% {
        opacity: 0;
        transform: translateY(30px);
    }
    100% {
        opacity: 1;
        transform: translate(0);
    }   
}

.btn-animated {
    animation: animate .5s ease-out .75s;
    animation-fill-mode: backwards;
}
</style>