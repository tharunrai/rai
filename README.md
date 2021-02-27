
<!DOCTYPE html> 
<html>
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width"/>
<title>Dackward dance</title>
<style>
*{
 margin:0;
 padding:0;
 box-sizing:border-box;
 }
 body {
 font-family: comic-san;
 font-weight:400;
 line-height:1.4;
 font-size:1em;
 background:#fff;
 }
 .loader {
  position:fixed; 
  top:0;
  left:0;
  bottom:0;
  height:100vh;
  width:100%;
  background:#000;
  display:flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index:9;
 }
  .loader h1 {
  color:#fff;
  animation:blink 1s ease infinite;
 }
 .loader button {
  display:inline-block;
  padding:10px 25px;
  border-radius:4px;
  background:#000;
  color:#fff;
  outline:none;
  border:1px solid #fff;
  margin:7px;
  text-transform:uppercase;
  transition:0.5s;
  opacity:0;
  transform:translateY(30px);
 }
 .loader button.show {
  opacity:1;
  transform:translateY(0);
 }
 .loader button.show ~ h1{
  display:none;
 }
 @keyframes blink {
 0%,100%{
 opacity:1;
 }
 50%{
  opacity:0;
 }
 }
 .main {
  position:relative;
  width:100%;
  overflow:hidden;
  min-height:100vh;
  display:flex;
  flex-direction: column;
  justify-content: center;
  align-items:flex-end;
  background:url("https://cdn3.vectorstock.com/i/1000x1000/01/02/background-cartoon-duck-funny-vector-21650102.jpg");
  background-size: cover;
  background-position: center top;
 }
 
.dance {
 position:absolute;
 z-index:6;
}
.dance img {
 width:400px;
}
 .d1 {
  position:absolute;
  right:0;
  transform:translateX(-100%);
  top:35%;
  width:400px;
  z-index:6;
 }
 .d1 img {
  width:300px;
 }
 .d2 {
 position:absolute;
 right:70%;
 bottom:0%;
 }
 .d3 {
 position:absolute;
 right:50%;
 transform:translateX(-90%);
 top:0%;
 } 
 .d4 {
 left:0%;
 top:50%;
 }
 .d5{
 position:absolute;
 left:80%;
 transform:translateX(-100%);
 top:35%;
 width:400px;
 z-index:6;
 }
  .d5 img {
  width:300px;
 }
 .d6{
 position:absolute;
 right:65%;
 transform:translateX(-100%);
 bottom:10%;
 width:400px;
 z-index:6;
 }
 .d6 img {
  width:400px;
 }
 .witch {
  position:absolute;
  top:0;
  left:-20%;
  animation:witch 10s Linear infinite;
  animation-delay:2s;
 }
 .witch img{
  width:180px;
 }
 @keyframes witch {
 0%{
  left:-20%;
 }
 60% {
  left:120%;
 }
 100% {
 left:120%;
 }
 }
 

</style>
</head>
<body> 
<div class="loader" onclick="playMusic()">
  <img src="https://www.animatedimages.org/data/media/481/animated-duck-image-0019.gif" >
  <button onclick="start()">enter the duckward</button>
  <h1>  Loading...</h1>
</div>
<audio src="https://mobcup.net/d/dv0nemca/mp3" loop id="music"> </audio>
<main class="main" >
  <div class="dance" >
   <div class="d1" >
    <img src="https://thumbs.gfycat.com/AcidicColorfulBoar.webp" alt="">
   </div> 
   <div class="d2" >
    <img src="https://i.pinimg.com/originals/68/a8/b8/68a8b821ce9babedbcf7509f0641f3c1.gif"  alt=""  >
   </div> 
   <div class="d3" >
    <img src="https://thumbs.gfycat.com/AcidicColorfulBoar.webp" alt=""  >
   </div>
   <div class="d4" >
    <img src="https://thumbs.gfycat.com/AcidicColorfulBoar.webp"  alt="" >
  <div class="d5" >
  <img src="https://thumbs.gfycat.com/AcidicColorfulBoar.webp"  alt="" >
  <div class="d6" >
    <img src="https://i.pinimg.com/originals/68/a8/b8/68a8b821ce9babedbcf7509f0641f3c1.gif"  alt=""  >
   </div>
  </div>
  </div> 
  </div>
  <div class="witch" >
    <img src="https://thumbs.gfycat.com/AcidicColorfulBoar.webp" alt=""  >
  </div>
</main>
<script>
const loader = document.querySelector(".loader");
window.addEventListener("load", function(){
 loader.querySelector("button").classList.add("show");
});
setTimeout(function(){
loader.querySelector("button").classList.add("show");
},14000)
function start() {
 loader.style.display = "none";
 playMusic()
}
const music = document.getElementById("music");
function playMusic() {
 if(music.paused) {
  music.play()
  }
  }

</script>
</body>
</html>

