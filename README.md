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
https://site.com (another protocol)
http://site.com:8080 (another port)

The "same origin" policy states that if a reference created by window.open or inside <iframe> and that comes from the same origin, we have full access to the window. Otherwise, if the origin is different we cannot access the content of the window. The only exception is the location: it can be changed allowing the user to be redirected. But it cannot read i.e information won't be leaked

Local storage to enable cross tab communication
// Open 2 tabs and inspection tools >> console tab and enter the code below
window.addEventListener('storage', function (e){
console.log(e)
});
// On the second tab, type the what is below 
localStorage.setItem('a','b')
// This will create an event whereby when a user clicks on the second tab it displays storageEvent information such as the new value, old value and URL from which the trigger occured. This is used=fule since it can be used to control a user by changing certain browser properties upon clicking or perfoming an action.
