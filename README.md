<div align="center">

## Easy Cross Browser Client Side Data Storage


</div>

### Description

A great way to persist data (on the client)between pages when working within a frameset.

This is a good, more stable substitute for session cookies.

Trying to pass querystring values or form values back and forth can get messy and if your string gets too long some browsers will choke.

Cookies can be an unstable solution because they can't get too long either and some browsers will mysteriously lose them.

This is a simple, dynamic solution that does the trick in version 4 IE and Netscape browsers.

If this is of use to you, send me a quick note and let me know! shawn_james@hotmail.com
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Shawn "Big Badger" Brown](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/shawn-big-badger-brown.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |
**Category**       |[Data Structures](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/data-structures__2-67.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/shawn-big-badger-brown-easy-cross-browser-client-side-data-storage__2-2568/archive/master.zip)





### Source Code

```
<pre>
&lt;html&gt;
&lt;head&gt;
&lt;SCRIPT&gt;
var strBuffer = new Array();
function GetValue(strName) {
 return strBuffer[strName.toLowerCase()];
}
function SetValue(strName, strValue) {
 strBuffer[strName.toLowerCase()] = strValue;
}
&lt;/SCRIPT&gt;
&lt;/head&gt;
&lt;frameset rows="*,39" onload="LoadVars();" BORDER=0 FRAMEBORDER=0 MARGINHEIGHT=0 MARGINWIDTH=0 FRAMESPACING=0 NORESIZE scrolling=auto&gt;
	&lt;frame src="somepage.asp" name="main" NORESIZE scrolling=auto&gt;
	&lt;frame src="someotherpage.asp" name="buttons" NORESIZE scrolling=no&gt;
&lt;/frameset&gt;
&lt;/html&gt;
usage examples:
parent.SetValue("Value1","ThisIsValue1");
parent.SetValue("value1","ThisIsChangedValue1");(note, case insensitive)
parent.SetValue("Value2","ThisIsValue2");
strVal = parent.GetValue("Value1");
</pre>
```

