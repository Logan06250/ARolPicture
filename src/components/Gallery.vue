<template>
    <div id="Gallery">
        <div class="img-container">
            <div class="menu-container">
                <div class="toggle" id="toggle" @click="expand()">
                    <section class="wow slideInDown" data-wow-duration="1s">
                        <i class="fa fa-plus" id="plus"></i>
                    </section>
                    </div>
                    <div class="menu menu-option" id="menu">
                    <a href="#" >
                        <i class="fa fa-microphone"></i>
                    </a>
                    <a href="#" >
                        <i class="fa fa-user"></i>
                    </a>
                    <a href="#" @click="contact" >
                        <i class="fa fa-envelope"></i>
                    </a>
                </div>
            </div>
                <div class="centered ">             
                    <section class="wow fadeInLeft" data-wow-duration="3s">
                        <p class="headtext" style="margin-left: 50px">  ArolPicture </p>
                    </section>
                    <section class="wow fadeInRight" data-wow-duration="3s">
                        <p class="headtext" > Gallery </p>
                    </section>
                </div>
                
                <div class="social"> 
                    <section class="wow fadeInDown" data-wow-duration="1s">
                        <i class="fab fa-twitter"></i> -
                        <i class="fab fa-facebook-f"></i> -
                        <i class="fab fa-instagram"></i> -
                        <i class="fab fa-linkedin"></i>
                    </section>    
                </div>
        </div>
        <div class="row wow fadeIn" data-wow-duration="1s"> 
            <div class="column">
                <a href="#" class="pop">
                    <img src="./../assets/grid/img12.jpg" style="width:100%">
                </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img4.jpg" style="width:100%">
                </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img9.jpg" style="width:100%">
                </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img8.jpg" style="width:100%">
                </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img13.jpg" style="width:100%">
                </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img6.jpg" style="width:100%">
                </a>
                    <a href="#" class="pop">
                        <img src="./../assets/grid/img10.jpg" style="width:100%">
                    </a>
                
            </div>
            <div class="column">
                <a href="#" class="pop">
                    <img src="./../assets/grid/img15.jpg" style="width:100%">
                 </a>
                 <a href="#" class="pop">
                    <img src="./../assets/grid/img6.jpg" style="width:100%">
                 </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img7.jpg" style="width:100%">
                 </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img3.jpg" style="width:100%">
                 </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img8.jpg" style="width:100%">
                 </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img9.jpg" style="width:100%">
                 </a>
                <a href="#" class="pop">
                    <img src="./../assets/grid/img12.jpg" style="width:100%">
                 </a>
            </div>
            <div class="column">
                <img src="./../assets/grid/img9.jpg" style="width:100%">
                <img src="./../assets/grid/img14.jpg" style="width:100%">
                <img src="./../assets/grid/img7.jpg" style="width:100%">
                <img src="./../assets/grid/img2.jpg" style="width:100%">
                <img src="./../assets/grid/img3.jpg" style="width:100%">
                <img src="./../assets/grid/img4.jpg" style="width:100%">
                <img src="./../assets/grid/img5.jpg" style="width:100%">
                
            </div>
            <div class="column">
                <img src="./../assets/grid/img5.jpg" style="width:100%">
                <img src="./../assets/grid/img2.jpg" style="width:100%">
                <img src="./../assets/grid/img3.jpg" style="width:100%">
                <img src="./../assets/grid/img7.jpg" style="width:100%">
                <img src="./../assets/grid/img12.jpg" style="width:100%">
                <img src="./../assets/grid/img6.jpg" style="width:100%">
                <img src="./../assets/grid/img15.jpg" style="width:100%">
            </div>
        </div>


        <div class="modal fade" id="imagemodal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
            <div class="modal-dialog">
                <div class="modal-content">              
                    <div class="modal-body">
                        <img src="" class="imagepreview" style="width: 100%; height: 100%" >
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    
        
</script>
<script>

import WOW from 'wow.js'

    var wow = new WOW(
    {
        boxClass:     'wow',      // animated element css class (default is wow)
        animateClass: 'animated', // animation css class (default is animated)
        offset:       0,          // distance to the element when triggering the animation (default is 0)
        mobile:       true,       // trigger animations on mobile devices (default is true)
        live:         true,       // act on asynchronously loaded content (default is true)
        callback:     function(box) {
        // the callback is fired every time an animation is started
        // the argument that is passed in is the DOM node being animated
        },
        scrollContainer: null,    // optional scroll container selector, otherwise use window,
        resetAnimation: true,     // reset animation on end (default is true)
    }
    );
    wow.init();
export default {

    name: 'FaqsEditModal',
    
    mounted() {

    },
    data() {
        return {
            i:  0
        }
    }, 
    mounted: function (){
        $(function() {
            $('.pop').on('click', function() {
                $('.imagepreview').attr('src', $(this).find('img').attr('src'));
                $('#imagemodal').modal('show');   
            });		
        });
    },
    methods: {
        expand: function() {
            if(this.i==0){
            document.getElementById("menu").style.transform="scale(3)"; 
            document.getElementById("plus").style.transform="rotate(45deg)"; 
                this.i=1;
            }
            else{   document.getElementById("menu").style.transform="scale(0)"; 
            document.getElementById("plus").style.transform="rotate(0deg)"; 
                this.i=0;
            }
        },
        contact: function () {
            this.$router.push("contact")
        }

    }
}
</script>

<style>

.modal-body
{
   background-color: rgba(0,0,0,0.1);
}

.img-container {
    width: 100%;
    height: 100%;
    position: relative;
    text-align: center;
    filter: brightness(70%);
    -webkit-filter: brightness(70%);
    background-image: url("../assets/mainimg.jpg");
    min-height: 500px;
    background-attachment: fixed;
    color: white;


}
.centered {
    position: absolute;
    top: 70%;
    left: 20%;
    font-family: Tahoma, Verdana, Segoe, sans-serif;
}

.social {
    position: absolute;
    top: 1%;
    left: 85%;
    font-size: 25px;
    line-height: 100px;

}
.menu-container {
    position: absolute;
    top: 30px;
    left: 10px;
    /*transform: translate(-50%, -50%);*/
}

.headtext {
    font-style: oblique;
    font-weight: 900;
    font-size: 40px;
}

.main-logo {
    height: 150px;
    width: 150px;
}

.column img { transition: all .2s ease-in-out; }
.column img:hover { 
    /*transform: scale(1.05); */
    filter: brightness(80%);
    
    }

.row {
  display: -ms-flexbox; /* IE10 */
  display: flex;
  -ms-flex-wrap: wrap; /* IE10 */
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create four equal columns that sits next to each other */
.column {
  -ms-flex: 25%; /* IE10 */
  flex: 25%;
  max-width: 25%;
  padding: 0 4px;
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
}

/* Responsive layout - makes a two column-layout instead of four columns */
@media screen and (max-width: 800px) {
  .column {
    -ms-flex: 50%;
    flex: 50%;
    max-width: 50%;
  }
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    -ms-flex: 100%;
    flex: 100%;
    max-width: 100%;
  }
}

.fas {
    transform: scale(2);
    cursor: pointer;

}

.fas:hover {
    transform: scale(2.1)
}


.toggle {
  background-color: transparent;
  text-align: center;
  height: 80px;
  width: 80px;
  border-radius: 50%;
  position: absolute;
  margin: auto;
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
}

.fa-plus{
  font-size: 40px;
  color: white;
  display: block;
  margin-top: 20px;
  transition: 0.7s;
    cursor: pointer;

}

.menu {
  background-color: rgba(75, 75, 75, 0.39);
  height: 120px;
  width: 120px;
  transform: scale(0);
  border-radius: 50%;
  position: absolute;
  margin: auto;
  top: 0px;
  bottom: 0px;
  left: -15px;
  z-index: -1;
  transition: 0.8s;
}

.menu-option a {
  display: inline-block;
  position: absolute;
  font-size: 12px;
  color: rgb(212, 212, 212);
}

.menu-option a:nth-child(1){
  top: 55px;
  left: 100px;
}

.menu-option a:nth-child(2){
  top: 83px;
  left: 87px;
}

.menu-option a:nth-child(3){
  top: 100px;
  left: 50px;
}

.menu-option a:hover {
  color: #ffffff;
}
</style>