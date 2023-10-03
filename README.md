# javascript-intermediate
This repository is shall document my progress in learning intermediate Javascript concepts
let newWin = window.open("about:blank","hello","width=200,height=200");
newWin.document.write("Hello, world!");
// This opens a window with the specified dimensions and message "Hello, World!"
let newWin = window.open("about:blank","hello","width=200,height=200");
newWin.document.write(<script>window.opener.document.body.innerHTML = 'Test'<\/script>);
// window.opener: refers to the parent window that opened the new window
// window.opener.document.body: Access the <body> element of the parent window

Same origin concept 
URLs have the same origin if they have the same protocol, domain and port
The following web addresses do not have the same origin
http://www.site.com (www. is important)
http://site.org (another domain, org is important)
