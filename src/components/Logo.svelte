<style>
  
  *{
    margin:0;
  }
  a{
    text-decoration: none;
  }
  #logo-cont{
    display: flex;
    flex-direction: column;
    align-items: flex-end;
  }
  .cross {
  position: absolute;
  left: 10px;
  top: -26px;
  width: 100px;
  height: 100px;
  /* opacity: 0.3; */
}
.cross:hover {
  opacity: 1;
}
.cross:before, .cross:after {
  position: absolute;
  left: 15px;
  content: ' ';
  height: 100px;
  width: 3px;
  background-color: #DBF8D9;
}
.cross:before {
  transform: rotate(90deg) translateY(-30px);
 
}
.cross:after {
  transform: rotate(-180deg) translate(5px, -35px);
}


</style>
<div id="logo-cont">
  <div class="cross"></div>
  <a href="/">
    <h1>jacob stordahl</h1>
  </a>
  <p>front end engineer in training</p>
</div>