"# js-snipets" 
#crawl for links
document.querySelectorAll('span.p--small').forEach((element) => {  console.log( element.textContent+" :: "+  element.previousElementSibling.getAttribute('criticsscore') );
if(element.previousElementSibling.getAttribute('criticsscore')>80)
window.open("https://www.magnetdl.com/"+(element.textContent).trim().toLowerCase()[0]+"/"+(element.textContent).replace(/ /g, "-").toLowerCase()+"/se/desc/");
});
#check and download
window.open(document.documentElement.outerHTML.match(/magnet:\?xt=urn:[^\s]+/)[0], '_blank'); window.close();