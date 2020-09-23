<div align="center">

## Words follow the mouse\.\(smooth\)


</div>

### Description

This piece of javascript will make words follow your mouse cursor, very smooth, possibly the best code for this type of thing
 
### More Info
 
Just copy and paste everything

Please vote for my code :-)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Mouse Pad](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/mouse-pad.md)
**Level**          |Advanced
**User Rating**    |3.8 (42 globes from 11 users)
**Compatibility**  |
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__2-57.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/mouse-pad-words-follow-the-mouse-smooth__2-2227/archive/master.zip)





### Source Code

```
<SCRIPT language=JavaScript>message = 'Follow me';
FonT = 'Verdana';
ColoR = '#ffffff';
SizE = 2; //1 to 7 only!
var amount = 5, ypos =- 50, xpos = 0, Ay = 0, Ax = 0, By = 0, Bx = 0, Cy = 0, Cx = 0, Dy = 0, Dx = 0, Ey = 0, Ex = 0;
if (document.layers) {
for (i = 0; i < amount; i++) {
document.write('<layer name=nsl'+i+' top=0 left=0><font face='+FonT+' size='+SizE+' color='+ColoR+'>'+message+'</font></layer>');
}
window.captureEvents(Event.MOUSEMOVE);
function nsmouse(evnt) {
xpos = evnt.pageX + 20;
ypos = evnt.pageY + 20;
}
window.onMouseMove = nsmouse;
}
else if (document.all) {
document.write("<div id='outer' style='position:absolute;top:0px;left:0px'>");
document.write("<div style='position:relative'>");
for (i = 0; i < amount; i++) {
document.write('<div id="text"'+i+' style="position:absolute;top:0px;left:0px;width:400px;height:20px"><font face='+FonT+' size='+SizE+' color='+ColoR+'>'+message+'</font></div>')
}
document.write("</div>");
document.write("</div>");
function iemouse() {
ypos = event.y + 20;
xpos = event.x + 20;
}
window.document.onmousemove = iemouse;
}
function makefollow() {
if (document.layers) {
document.layers['nsl'+0].top = ay;
document.layers['nsl'+0].left = ax;
document.layers['nsl'+1].top = by;
document.layers['nsl'+1].left = bx;
document.layers['nsl'+2].top = cy;
document.layers['nsl'+2].left = cx;
document.layers['nsl'+3].top = Dy;
document.layers['nsl'+3].left = Dx;
document.layers['nsl'+4].top = Ey;
document.layers['nsl'+4].left = Ex;
}
else if (document.all) {
outer.style.pixelTop = document.body.scrollTop;
text[0].style.pixelTop = ay;
text[0].style.pixelLeft = ax;
text[1].style.pixelTop = by;
text[1].style.pixelLeft = bx;
text[2].style.pixelTop = cy;
text[2].style.pixelLeft = cx;
text[3].style.pixelTop = Dy;
text[3].style.pixelLeft = Dx;
text[4].style.pixelTop = Ey;
text[4].style.pixelLeft = Ex;
 }
}
function move() {
ey = Ey += (ypos - Ey) * 0.2;
ex = Ex += (xpos - Ex) * 0.2;
dy = Dy += (ey - Dy) * 0.3;
dx = Dx += (ex - Dx) * 0.3;
cy = Cy += (dy - Cy) * 0.4;
cx = Cx += (dx - Cx) * 0.4;
by = By += (cy - By) * 0.5;
bx = Bx += (cx - Bx) * 0.5;
ay = Ay += (by - Ay) * 0.6;
ax = Ax += (bx - Ax) * 0.6;
makefollow();
setTimeout('move()', 10);
}
window.onload=move;</SCRIPT>
```

