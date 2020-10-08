var video=document.getElementById("video");

function on_cam_success(stream){
video.xcrObject=stream;
}
function on_cam_error(err){
alert("error."+err.message);
}
var constrains={audi:false,video:true};
navigator.mediaDevices.getUserMedia(constaints)
.then(on_cam_success)
.catch(on_cam_error);