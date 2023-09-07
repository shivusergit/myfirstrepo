<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<%@ page session="false" contentType="text/html; charset=UTF-8"%>
<%@page import="com.dcalonline.util.DCalFormatter"%>
<%@page import="com.dcalonline.security.csrf.token.*"%>
<%@ page import="com.fdc.security.util.AppnSecurityAPI"%>
<%com.dcalonline.util.LangStringFactory lang = new com.dcalonline.util.LangStringFactory(request);%>
<%String csrfToken = new CsrfToken().getStoredToken(request);
String csrfKey = CsrfToken.CSRF_PARAMETER_NAME;
%>
<html xmlns="http://www.w3.org/1999/xhtml">
<head><jsp:include page="/HTML/826/Common/meta.jsp" />
<title><%=lang.get("SecurityText")%></title>
<link type="text/css" rel="stylesheet" href="<%=com.dcalonline.util.JspUtil.getCustomCss(request)%>">
<script type="text/javascript"	src="/Resources/Jscript/Common/common.js"></script>
<script type="text/javascript" src="/Resources/Jscript/Common/jquery/jquery.min.js"></script>
<script type="text/javascript" src="/Resources/Jscript/Common/jquery/jquery-migrate.min.js"></script>
<script type="text/javascript" src="/Resources/Jscript/ckeditor5/ckeditor.js"></script>
<script type="text/javascript"	src="/Resources/Jscript/Common/popup.js"></script>
<script type="text/javascript" src="/Resources/Jscript/Administration/IssuerSetup/Template.js"></script> 
<script type="text/javascript" src="/Resources/Jscript/Common/preventClick.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/ckeditor5/39.0.2/ckeditor.js"></script>
</head>
 <style>
            #container {
                width: 500px;
                margin: 20px auto;
                magicline_color: 'white'
            }
            .ck-editor__editable[role="textbox"] {
                /* editing area */
                min-height: 400px;
            }
            .ck-content .image {
                /* block images */
                max-width: 80%;
                margin: 20px auto;
            }
        </style>
</head>

<body leftmargin="2" topmargin="2">
<form action="/dcal/IssuerSetupServlet" method="post">
<input id="companyId" name="companyId" type="hidden" value="<%=AppnSecurityAPI.encoder().encodeForSafeHTML(request.getParameter("companyId"))%>" />
<input id="isoCode" name="isoCode" type="hidden" value="<%=AppnSecurityAPI.encoder().encodeForSafeHTML(request.getParameter("isoCode"))%>" />
<input id="csrf_security_token" type="hidden" name="<%=csrfKey %>" value="<%=csrfToken %>" />
<input name="htmlcontent" id="htmlcontent" type="hidden" />

<!--top curve table-->
<table border="0" cellspacing="0" cellpadding="0" width="500">
	<tr>
		<td width="8" height="10" valign="top" class="navbarbg"><img src="/Resources/images/top_lt_cr.gif" width="8" height="8" alt="" border="0"></td>
		<td width="474" class="navbarbg"><img src="/Resources/images/sp.gif" width="1" height="1" alt="" border="0"></td>
		<td width="8" valign="top" class="navbarbg"><img src="/Resources/images/top_rt_cr.gif" width="8" height="8" alt="" border="0"></td>
	</tr>
	<tr>
		<td colspan="3"><img src="/Resources/images/sp.gif" width="1" height="1" alt="" border="0"></td>
	</tr>
	<tr>
		<td colspan="3" class="tableheader"><img src="/Resources/images/sp.gif" width="1" height="4" alt="" border="0"></td>
	</tr>
</table>
&nbsp;<b><%=lang.get("UploadText")%></b><br>
       <style>
            #container {
                width: 1000px;
                margin: 20px auto;
            }
            .ck-editor__editable[role="textbox"] {
                /* editing area */
                min-height: 200px;
            }
            .ck-content .image {
                /* block images */
                max-width: 80%;
                margin: 20px auto;
            }
        </style>
        <div id="container">
            <div id="editor">
            </div>
        </div>

<script type="text/javascript">
var editor;

// At page startup, load the default language:
createEditor( '' );
function createEditor( languageCode ) {
	if ( editor )
		editor.destroy();

	// Replace the <textarea id="editor"> with an CKEditor
	// instance, using default configurations.
	editor = CKEDITOR.ClassicEditor.create  ( document.getElementById('editor'), {
	toolbar: {
				items:  [ 'Bold', 'Italic','Underline','-', 'NumberedList', 'BulletedList','-', 'Link', 'Unlink','Table', '-','Cut', 'Copy', 'Paste','-', 'JustifyLeft', 'JustifyCenter', 'JustifyRight' ],
				shouldNotGroupWhenFull: true
			},
	});
}

CKEDITOR.ClassicEditor.on( 'dialogDefinition', function( ev )
		 {
		  
		  var dialogName = ev.data.name;
		  var dialogDefinition = ev.data.definition;
		  
		  if ( dialogName == 'link' )//removing the target and advanced tab in Link fro blackList filter issue
		  {
		   
		   var infoTab = dialogDefinition.getContents( 'info' );   
		   
		   infoTab.remove( 'linkType' );
		   infoTab.remove( 'browse' );
		   
		   dialogDefinition.removeContents( 'target' );   
		   
		   dialogDefinition.removeContents( 'advanced' );
		  }
		 });

function updateHtml() {	
	  var webHtml,contentBytes=[],url,newwindow,companyId,isoCode,startPos,returnValue;
	  var params = {docType: 'SEC'};
	  returnValue=alertSaveMessage(params);
	  if (returnValue==1){	
	  webHtml = CKEDITOR.ClassicEditor.instances.webText.document.getBody().getHtml();
	  startPos =webHtml.indexOf("data-cke-"); 
	  if(startPos!=-1){
		  webHtml= replacedString(webHtml);
	  }	  	     
	  contentBytes =stringToBytes(webHtml);	  
	  if(contentBytes.length>300000){ //antisamy-policy.xml maxInputSize=300000
		url="/JSP/IssuerSetupTemplate/AlertMessage.jsp";
		newwindow=window.showModalDialog(url,window,'dialogWidth:380px;dialogHeight:240px;dialogTop:center;dialogLeft:center;resizable:no;help:no;status:no;scroll:no;');
	  } $.post(
				"/dcal/IssuerSetupServlet",
				{
					action: "updateTemplateLinkText",
					contentType:"HTML",
					docType:"SEC",
					companyId:document.getElementById('companyId').value,
					isoCode: document.getElementById('isoCode').value,
					csrf_security_token: document.getElementById('csrf_security_token').value,
					htmlcontent:webHtml					
				},			
				function(response, textStatus, request){
					setCSRFTokenFromHeader(opener.window, request);
						if(response==1)			
							window.close();
						else{
							alertErrorMessage();
							window.close();
						}
				}				
			);
	  }		
}

function closePopup(){
	if(parent.window.close() == undefined) parent.window._close(); else window.close();
}
</script>
<table width="500" border="0" cellspacing="0" cellpadding="0" >
	<tr>
		<td><img src="/Resources/images/sp.gif" width="1" height="5" alt="" border="0"/></td>
	</tr>
	<tr>
		<td class="tablebgcolorlist"><img src="/Resources/images/sp.gif" width="1" height="1" alt="" border="0"/></td>
	</tr>
	<tr>
		<td><img src="/Resources/images/sp.gif" width="1" height="3" alt="" border="0"/></td>
	</tr>
	<tr>
		<td height="30" align="left" class="buttonbarbg">
			<table border="0" cellspacing="0" cellpadding="0">
				<tr>
					<td height="30" align="center"><input type="button" value="<%=lang.get("Save1658")%>" class="submit" onclick="updateHtml();">&nbsp;
					<input type="button" value="<%=lang.get("Cancel")%>" class="submit" onClick="closePopup()"></td>
				</tr>
			</table>
		</td>
	</tr>
</table>




<!--bottom curve table-->

<table border="0" cellspacing="0" cellpadding="0" width="500">
	<tr>
		<td colspan="3"><img src="/Resources/images/sp.gif" width="1" height="5" alt="" border="0"></td>
	</tr>
	<tr>
		<td colspan="3" class="banding1" width="100%"><img src="/Resources/images/sp.gif" height="5" alt="" border="0"></td>
	</tr>
	<tr>
		<td colspan="3" width="480"><img src="/Resources/images/sp.gif" width="1" height="1" alt="" border="0"></td>
	</tr>
	<tr>
		<td width="8" height="10" valign="bottom" class="tableheader"><img src="/Resources/images/bottom_lt_cr.gif" width="8" height="8" alt="" border="0"></td>
		<td width="474" class="tableheader"><img src="/Resources/images/sp.gif" width="1" height="1" alt="" border="0"></td>
		<td width="8" valign="bottom" class="tableheader"><img src="/Resources/images/bottom_rt_cr.gif" width="8" height="8" alt="" border="0"></td>
	</tr>
</table>
</form>

</body>
</html>
