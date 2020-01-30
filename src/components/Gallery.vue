<template>
    <div id="Gallery">
        <div class="img-container">
            <div class="menu">
                    <i class="fas fa-align-justify"></i>
            </div>
            <div class="centered headtext"> ArolPicture  Gallery</div>
        </div>
        <div class="row"> 
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
$(function() {
		$('.pop').on('click', function() {
			$('.imagepreview').attr('src', $(this).find('img').attr('src'));
			$('#imagemodal').modal('show');   
		});		
});
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
    transform: translate(-50%, -50%);
    font-family: Tahoma, Verdana, Segoe, sans-serif;
}
.menu {
    position: absolute;
    top: 10%;
    left: 5%;
    transform: translate(-50%, -50%);
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

</style>