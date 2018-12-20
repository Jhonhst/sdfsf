<template>
    <div class="container-fluid  body-year">
      <!-- <div class="row"> -->
        <div class="col-12 offset-md-2 col-md-8">
          <p class="lastYearTitle text-center mb-5">LAST YEAR'S HIGHLIGHTS</p>
            <div class="row ">
             <div class="col-12 col-sm-4">
              <img class="spheres" src="/../static/images/Catch-Up-1.png">
              <div class="text-center mt-3 mb-4">
                <a href="#" class="boton-login-c name-city">TENERIFE</a>            
              </div>
            </div>
            <div class="col-12  col-sm-4">
              <img class="spheres" src="/../static/images/Catch-Up-2.png">
              <div class="text-center mt-3 mb-4">
                <a href="#" class="boton-login-c name-city">ZANZIBAR</a>            
              </div>
            </div>
            <div class="col-12  col-sm-4">
              <img class="spheres" src="/../static/images/Catch-Up-3.png">
              <div class="text-center mt-3 mb-4">
                <a href="#" class="boton-login-c name-city" style="margin-top:40px;">  MIAMI</a>     
              </div>
            </div>
          </div>
        </div>
      <!-- </div> -->
    </div>
    <!-- <div class="lastYearWrapper">

      

      <div class="spheresWrapper">

        <div class="elements">
          <img class="spheres" src="/../static/images/Catch-Up-1.png">
          <div class="lastYearButton">
            TENERIFE
          </div>
        </div>

        <div class="elements">

          <img class="spheres" src="/../static/images/Catch-Up-2.png">
          <div class="lastYearButton">
            ZANZIBAR
          </div>
          </div>

        <div class="elements">
          
          <img class="spheres" src="/../static/images/Catch-Up-3.png">
          <div class="lastYearButton">
            MIAMI
          </div>
          </div>  
      </div>
          <div class="final-sunglasses-wrapper">
            <div class="element1">
              <img alt="Gafas" src="/../static/images/Gafas-Final.png">
            </div>
          <div class="element2">
            <img alt="Gafas" src="/../static/images/Gafas-Final.png">
          </div>
          </div>
    </div> -->


</template>


<style lang="scss">
.body-year{
   margin-top: -100px;
   margin-bottom: -80px;
   background-image: url('/static/images/Fondo-Palmeras.png'); 
   background-size: 100%  auto;
  // margin-bottom: -40%;
  padding: 0% 0% 10% 0%;
}
.name-city{
  margin-top: 100px !important;
}
.lastYearTitle{
  
  font-size: 2em;
}
@media (min-width: 576px) { 
  .lastYearTitle{
    font-size: 3em;
  }
 }

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) { 
    .lastYearTitle{
    font-size: 3em;
  }
 }

// Large devices (desktops, 992px and up)
@media (min-width: 992px) { 
    .lastYearTitle{
    font-size: 3em;
  }
 }

// Extra large devices (large desktops, 1200px and up)
@media (min-width: 1200px) {  
    .lastYearTitle{
    font-size: 3em;
  }
}
/**************** Sass variables ***************/
    // $full-background:cover;
    // $auto:auto;
    // $auto:auto;
    // $relative:relative;
    // $text-center:center;
    // $no-repeat:no-repeat;
    // $inline-block:inline-block;
    // $full:100%;
    // $half:50%;
    // $normal-size-font:1em;
    // $double-size-font:2em;
    // $zero:0;
    // $black:#000;
    // $white:#fff;
    // $test-color:blue;
    // $test-border:3px solid red;
    // $brown:#b06050;
    // $display:inline-block;
    // $flex:flex;
    // $bold:bold;
    // $transparent:transparent;
    // $row:row;
    // $wrap:wrap;
    // $column:column;
/**************** Sass variables ***************/

/**************** Mixins***********************/

// @mixin centerDiv(){

//     margin-left:$auto;
//     margin-right:$auto;

// }
/**************** Mixins***********************/

/****************Classes******************/

  // .lastYearWrapper{
  //   border:3px solid red;
  //   height:900px;
  //   width:$full;
  //   background-size:$full $auto;
  //   background-image:url('/static/images/Fondo-Palmeras-2.png');
  // }

  // .lastYearTitle{
  //   font-size:4em;
  //   margin-bottom:4%;
  // }

  // .spheresWrapper{
  //   @include centerDiv();
  //   display:$flex;
  //   flex-direction:$row;
  //   justify-content:$text-center;
  //   border:3px solid red;
  //   width:60%;
  //   font-weight:$bold;
  //   text-align:$text-center;

  // }

  // .elements{
  //   @include centerDiv();
  //   border:3px solid red;
  //   width:32%;
  // }

  // .lastYearButton{
  //   color:$white;
  //   background-image:url('/static/images/Btn-Login.png');
  //   background-repeat:$no-repeat;
  //   background-size:40% $auto;
  //   background-position:center;
  //   font-size:1.25em;
  //   padding:7%;

  // }

  // .spheres{

  //   width:$full;
  //   height:$auto;

  // }

  // .final-sunglasses-wrapper{
  //   display:$flex;
  //   flex-direction:$column;
  //   align-items:center;
  //   width:100%;
  // }

  // .element1{
  //  width:45%;
  //  visibility:hidden;
  // }
  // .element2{

  //   width:45%;
    

  // }

  /****************Classes******************/

  /****************Identifiers**********/

  /****************Identifiers**********/

  /****************Media queries********************/


  /****************Media queries********************/


</style>