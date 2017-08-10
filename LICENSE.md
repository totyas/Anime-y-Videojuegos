<style type="text/css"> body { background-image: url(aki va la url de tu imagen) } </style> 
<script language="Javascript">
<!-- Begin
function disableselect(e){
return false
}
function reEnable(){
return true
}
document.onselectstart=new Function ("return false"
if (window.sidebar){
document.onmousedown=disableselect
document.onclick=reEnable
}
// End -->
</script>
<form name="eMailer">
ENVÍA ESTA PÁGINA A UN AMIGO
<br>
Indica su e-mail:
<br>
<input type="text" name="address" size="25">
<br>
<input type="button" value="Recomendá esta Web!" onClick="mailThisUrl();">
</form>
<script language="JavaScript1.2">
var good;
function checkEmailAddress(field) {
// the following expression must be all on one line...
var goodEmail = field.value.match(/b(^(S+@).+((.com)|(.net)|
(.edu)|(.mil)|(.gov)|(.org)|(..{2,2}))$)b/gi);
if (goodEmail){
good = true
} else {
alert('Por favor introduce un e-mail valido')
field.focus()
field.select()
good = false
}
}
u = window.location;
m = "Pienso que te puede interesar esta página...";
function mailThisUrl(){
good = false
checkEmailAddress(document.eMailer.address)
if (good){
// the following expression must be all on one line...
window.location = "mailto:"+document.eMailer.address.value+"?subject="+m+"&body="+document.title+" "+u;
}
}
</script>
<BGSOUND SRC="sonido.mid" LOOP=none>
<WIDTH=200 HEIGHT=55 AUTOSTART="true" LOOP="false" HIDDEN="true">

