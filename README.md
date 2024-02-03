# javascript-web-html-to-pdf

## Description
A demo of html rendering to pdf. In this demo
the entire body of the html page in rendered to
a canvas tag then passed to pdf lib. The rendering is basicaly
an image so it will be uneditable. 

There is some security issue
with htmltocanvas, so that html fragments are not rendered.
A workaround to this issue is to have a seperate pdf page for each
html page then merge the pdfs. [Workaround](https://stackoverflow.com/questions/47632710/html2canvas-creating-multiple-divs)

Another issue in htmltocanvas lib is bootstrap, rendering to a web page is fine but when using htmltocanvas the css is wrong.
A workaround to this issue is to customize boostrap by removing the print media type. This was tested for boostrap v3.7 and later v5.3 both should this issue. [Remove print media type](https://stackoverflow.com/questions/16858954/how-to-properly-use-jspdf-library)

## Tech stack
- htmltocanvas
- jspdf
- promise

## Docker stack
- httpd:latest

## To run
`sudo ./install.sh -u`
- Available at http://localhost

## To stop
`sudo ./install.sh -d`

## To see help
`sudo ./install.sh -h`
