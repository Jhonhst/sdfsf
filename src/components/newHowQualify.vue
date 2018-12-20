<template>

  <div class="container-fluid body-quelifi ">
    <div class="row">
      <div id="package-includes" class="col-12 col-sm-6 img">
        <span class="titles">PACKAGE INCLUDES</span>
      </div>
      <div id="star-rewards" class="col-12 col-sm-6 img">
        <span class="titles">STAR REWARDS</span>
      </div>
    </div>
    <div class="row">
      <div class="col-12 col-sm-6 img" id="qualifiers">
        <span class="titles">STAR QUALIFIERS</span>
      </div>
      <div class="col-12 col-sm-6 img" id="reminder">
        <span class="titles">QUALIFICATION REMINDER</span>
      </div>
    </div>   
  </div>
</template>

<style lang="scss">
.body-quelifi{
  margin-top: -55px;
  margin-bottom: 150px;
}
.img{
  padding: 8% 0% 8% 0%;
  border: 3px solid transparent;
}


/**************** Sass variables ***************/
    $full-background:cover;
    $auto:auto;
    $auto:auto;
    $relative:relative;
    $text-center:center;
    $no-repeat:no-repeat;
    $inline-block:inline-block;
    $full:100%;
    $half:50%;
    $normal-size-font:1em;
    $double-size-font:2em;
    $zero:0;
    $black:#000;
    $white:#fff;
    $test-color:blue;
    $test-border:3px solid red;
    $brown:#b06050;
    $display:inline-block;
    $flex:flex;
    $bold:bold;
    $transparent:transparent;
    $row:row;
    $wrap:wrap;
    $column:column;
    
/**************** Sass variables ***************/

/**************** Mixins***********************/
@mixin image(){
    background-size:$full $auto;
    background-repeat:$no-repeat;
    text-align:$text-center;
}

@mixin imageMobile(){
    background-size:$full $full;
    background-repeat:$no-repeat;
    text-align:$text-center;
}
/**************** Mixins***********************/

/****************Classes******************/
  .wrapper-qualify{
    display:$flex;
    background-color:$transparent;
    height:730px;
    flex-direction:$row;
    flex-wrap:$wrap;
  }

  .picture{
    display:$flex;
    justify-content:$text-center;
    align-items:center;
    border:6px solid $transparent;
    background-color:$transparent;
    text-align:$text-center;
    width:$half;
  }
  /****************Classes******************/

   /****************Identifiers**********/

  #package-includes{
    @include image();
    background-image:url('/../static/images/Package-Includes.jpg');
  }
  #star-rewards{
    @include image();
    background-image:url('/../static/images/Star-Rewards.jpg');
  }
  #qualifiers{
    @include image();
    background-image:url('/../static/images/Star-Qualifers.jpg');
  }

  #reminder{
    @include image();
    background-image:url('/../static/images/How-To-Qualify.jpg');
  }
   /****************Identifiers**********/


    
    /****************Classes******************/
    .titles{
    display:$flex;
    flex-direction:$column;
    width:$full;
    text-align:$text-center;
    font-size:1.5em;
    font-weight:bold;
    font-family: Helvetica, sans-serif !important;
    bottom:6.5em;
    }

    .picture{
    display:$flex;
    justify-content:$text-center;
    align-items:center;
    border:3px solid $transparent;
    background-color:$transparent;
    text-align:$text-center;
    width:$full;
  }

  /****************Classes******************/

  /****************Identifiers**********/

  #package-includes{
    @include  imageMobile(); 
    background-image:url('/../static/images/Package-Includes.jpg');
  }
    #star-rewards{
    @include imageMobile();
    background-image:url('/../static/images/Star-Rewards.jpg');
  }

   #qualifiers{
     @include imageMobile();
    background-image:url('/../static/images/Star-Qualifers.jpg');
  }

   #reminder{
    @include imageMobile();
    background-image:url('/../static/images/How-To-Qualify.jpg');
  }

  /****************Identifiers**********/
@media (min-width: 576px) {
  .titles{
    font-size: 2em;
  }
}

@media (min-width: 768px) {
  .titles{
    font-size: 2.5em;
  }
 }

@media (min-width: 992px) { 
  .titles{
    font-size: 3em;
  }
} 

</style>

