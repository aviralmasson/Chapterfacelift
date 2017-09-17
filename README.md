# Chapterfacelift

# To change title:
let nod= document.querySelector('.item-page__main-title')

nod
<h1 title="Thug Kitchen: The Official Cookbook: Eat Like You Give a F*ck" data-a8n="item-page__main-title" class="item-page__main-title" style="overflow-wrap: break-word;">
nod.textcontent

nod.textContent='Irresistable Indian Food';
"Irresistable Indian Food"


# Change Book cover
let node= document.querySelector('.product-image__image--single')
node
<img class="product-image__image--single" src="https://dynamic.indigoimages.ca/books/1770894659.jpg?altimages=false&amp;scaleup=true&amp;maxheight=515&amp;width=380&amp;quality=85&amp;sale=30&amp;lang=en" data-a8n="product-image__image" alt="Thug Kitchen: The Official Cookbook: Eat Like You Give a F*ck by Thug Thug Kitchen">
node.src="http://img.taste.com.au/qDjJh8W8/taste/2016/11/butter-chicken-101831-1.jpeg";
"http://img.taste.com.au/qDjJh8W8/taste/2016/11/butter-chicken-101831-1.jpeg"




# Navigation

let nav1 = ['Butter Chicken', 'Chicken Tandoori', 'Chilly Cheese','Curry Meatballs','Kadahi Panner','Masala Chicken','Kidney beans','Butter Naan','Mix Veg'];
let n1= document.querySelectorAll('.top-nav__list-link');
undefined
n1
NodeList [ <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link> ]
n1= document.querySelectorAll('[class^=top-nav__list-link]');
NodeList [ <a.top-nav__list-link>, <a.top-nav__list-link--active>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link> ]

        n1= Array.from(document.querySelectorAll('[class^=top-nav__list-link]'));
Array [ <a.top-nav__list-link>, <a.top-nav__list-link--active>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link>, <a.top-nav__list-link> ]

  n1.map( (navitem, index) => navitem.textcontent= nav1[index]);
Array [ "Butter Chicken", "Chicken Tandoori", "Chilly Cheese", "Curry Meatballs", "Kadahi Panner", "Masala Chicken", "Kidney beans", "Butter Naan", "Mix Veg", undefined ]      

# To change logo

let logo1= document.querySelector('[data-a8n]');

logo1
<ul class="header__skip-links" data-a8n="header__skip-links">

logo1= document.querySelector('[data-a8n=indigo-logo]');
<a href="https://www.chapters.indigo.ca/en-ca/" class="indigo-logo" data-a8n="indigo-logo">

let logo2= document.createElement('img');

logo2
<img>
logo2.src="https://dcassetcdn.com/design_img/206812/133691/133691_2282653_206812_image.jpg";

logo2
<img src="https://dcassetcdn.com/design_img/206812/133691/133691_2282653_206812_image.jpg">

let oldlogo1= document.querySelector('[data-a8n-indigo-logo] svg');
oldlogo1
logo1.replaceChild(logo2,oldlogo1)

# To change inner HTML
let details= {'Price' : '20$' , 'weight' : '0.75kg','Location' : 'Duckworth st'};

details
Object { Price: "20$", weight: "0.75kg", Location: "Duckworth st" }

let some_html=`
<ul>
<li>abc1</li>
 <li>def2</li>
<li>ghi3</li>
</ul>
`
;

let a= document.getElementById('item-page__item-purchase-container')
a
<section class="item-purchase__container" id="item-page__item-purchase-container" aria-labelledby="product-purchase-label" data-a8n="item-purchase-container">

function render(obj){
let some_html=`
<ul>
<li>${obj.Price}</li>
 <li>${obj.weight}</li>
<li>${obj.Location}</li>
</ul>
`
; return some_html; }

render
function render()
render(details)
"
<ul>
<li>20$</li>
 <li>0.75kg</li>
<li>Duckworth st</li>
</ul>
"

 a.innerHTML=render (details);
"
<ul>
<li>20$</li>
 <li>0.75kg</li>
<li>Duckworth st</li>
</ul>
"       
     

# Using array objects


details= [{'Price' : '20$' , 'weight' : '.75kg','Location' : 'Duckworth st'},
{'Price' : '12$' , 'weight' : '0.50kg','Location' : 'Duckworth st 2'} ];

render(details[1]);
"
<ul>
<li>12$</li>
 <li>0.50kg</li>
<li>Duckworth st 2</li>
</ul>
"
a.innerHTML=render (details[1]);
"
<ul>
<li>12$</li>
 <li>0.50kg</li>
<li>Duckworth st 2</li>
</ul>
"

# Add to cart-
let button= document.getElementById('add-to-cart-button');

button
<button type="button" id="add-to-cart-button" data-a8n="item-page__button-add-to-cart" class="common-button add-to-cart-button__primary ">
button.addEventListener('click',function(){
document.documentElement.innerHTML='';
});
