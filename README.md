inbex.html <!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Ноутбукарий — магазин ноутбуков</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Onest:wght@400;500;700;800&display=swap">
<style>
:root{--bg:#e9edf1;--surface:#f8fafb;--ink:#14202b;--muted:#566574;--line:#cdd5dc;--accent:#2446d8;--on-accent:#fff;--ok:#1f7a4d;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#10171e;--surface:#18222c;--ink:#e8edf2;--muted:#93a3b3;--line:#2a3846;--accent:#6d8cff;--on-accent:#0b1220;--ok:#5fd29b}}
:root[data-theme="dark"]{--bg:#10171e;--surface:#18222c;--ink:#e8edf2;--muted:#93a3b3;--line:#2a3846;--accent:#6d8cff;--on-accent:#0b1220;--ok:#5fd29b}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:400 16px/1.5 Onest,system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);background:var(--surface);z-index:10}
button,input,select,textarea{font:inherit;color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
header{position:sticky;top:env(safe-area-inset-top,0px);z-index:9;background:var(--surface);border-bottom:1px solid var(--line)}
.bar{max-width:1120px;margin:0 auto;padding:10px 12px;display:flex;flex-wrap:wrap;align-items:center;gap:8px}
.logo{font-weight:800;font-size:22px;letter-spacing:-.02em;margin-right:auto;display:flex;align-items:center;gap:10px}.logo svg{width:38px;height:auto;flex:none}
.cartbtn{background:var(--accent);color:var(--on-accent);border:0;border-radius:10px;padding:10px 16px;font-weight:700;cursor:pointer}
.hero{max-width:1120px;margin:0 auto;padding:40px 16px 12px}
.hero h1{font-size:clamp(34px,7vw,64px);line-height:1.02;letter-spacing:-.035em;font-weight:800;margin:0 0 12px;max-width:14ch}
.hero p{color:var(--muted);margin:0;max-width:52ch}
.tools{max-width:1120px;margin:0 auto;padding:20px 16px;display:grid;gap:10px;grid-template-columns:1fr}
@media(min-width:720px){.tools{grid-template-columns:2fr 1fr 1fr 1.2fr}}
.tools input[type=search],.tools select{width:100%;padding:11px 12px;border:1px solid var(--line);border-radius:10px;background:var(--surface)}
.price label{display:flex;justify-content:space-between;font-size:14px;color:var(--muted)}
.price input{width:100%;accent-color:var(--accent)}
.grid{max-width:1120px;margin:0 auto;padding:0 16px 48px;display:grid;gap:16px;grid-template-columns:repeat(auto-fill,minmax(250px,1fr))}
.card{background:var(--surface);border:1px solid var(--line);border-radius:14px;overflow:hidden;display:flex;flex-direction:column}
.pic{background:var(--bg);padding:18px 24px 6px}
.pic svg{width:100%;height:auto;display:block}
.body{padding:14px 16px 16px;display:flex;flex-direction:column;gap:8px;flex:1}
.body h3{margin:0;font-size:18px;letter-spacing:-.01em}
.brand{color:var(--muted);font-size:14px}
dl{margin:0;display:grid;grid-template-columns:auto 1fr;gap:2px 12px;font-size:14px}
dt{color:var(--muted)}dd{margin:0;text-align:right}
.buy{margin-top:auto;display:flex;align-items:center;justify-content:space-between;gap:8px;padding-top:10px;border-top:1px solid var(--line)}
.cost{font-weight:800;font-size:20px;letter-spacing:-.01em}
.add,.call{background:var(--ink);color:var(--bg);border:0;border-radius:10px;padding:9px 14px;font-weight:700;cursor:pointer}
.empty{grid-column:1/-1;text-align:center;color:var(--muted);padding:48px 0}
.shade{position:fixed;inset:0;background:rgba(10,16,22,.5);opacity:0;pointer-events:none;transition:opacity .2s;z-index:20}
.shade.on{opacity:1;pointer-events:auto}
aside{position:fixed;top:0;right:0;bottom:0;width:min(420px,100%);background:var(--surface);z-index:21;transform:translateX(100%);transition:transform .25s;display:flex;flex-direction:column;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
aside.on{transform:none}
aside h2{margin:0;padding:16px;font-size:20px;display:flex;justify-content:space-between;align-items:center;border-bottom:1px solid var(--line)}
.x{background:none;border:0;font-size:26px;line-height:1;cursor:pointer}
.items{flex:1;overflow:auto;padding:8px 16px}
.row{display:grid;grid-template-columns:1fr auto;gap:4px 12px;padding:12px 0;border-bottom:1px solid var(--line)}
.row b{font-weight:700}.row small{color:var(--muted)}
.qty{display:flex;align-items:center;gap:8px;grid-column:1/-1}
.qty button{width:32px;height:32px;border-radius:8px;border:1px solid var(--line);background:var(--bg);cursor:pointer}
.qty .rm{width:auto;padding:0 10px;margin-left:auto;font-size:14px}
.foot{padding:16px;border-top:1px solid var(--line);display:grid;gap:10px}
.total{display:flex;justify-content:space-between;font-size:20px;font-weight:800}
.foot input{width:100%;padding:11px 12px;border:1px solid var(--line);border-radius:10px;background:var(--bg)}
.err{color:#c0392b;font-size:14px;min-height:1.2em}
.done{padding:32px 16px;text-align:center}
.done strong{color:var(--ok)}
@media (prefers-reduced-motion:reduce){*{transition:none!important}}
.sell{background:var(--ink);color:var(--bg)}
@media(max-width:480px){.logo{font-size:18px;gap:6px}.logo svg{width:30px}.cartbtn{padding:9px 11px;font-size:14px}}
.tag{font-size:14px;color:var(--muted);margin:0}
.priv .pic{padding:0}.priv .pic img{width:100%;aspect-ratio:4/3;object-fit:cover;display:block}
.call{display:inline-block;background:var(--ink);color:var(--bg);border:0;border-radius:10px;padding:9px 14px;font-weight:700;cursor:pointer;text-decoration:none}
.ghost{background:none;border:1px solid var(--line);border-radius:10px;padding:9px 14px;cursor:pointer}
.del{background:none;border:0;color:var(--muted);text-decoration:underline;cursor:pointer;padding:0;font-size:14px;text-align:left}
.modal{position:fixed;inset:0;z-index:30;display:none;align-items:flex-start;justify-content:center;overflow:auto;padding:calc(16px + env(safe-area-inset-top,0px)) 12px 16px;background:rgba(10,16,22,.55)}
.modal.on{display:flex}
.sheet{background:var(--surface);border-radius:14px;width:min(520px,100%);padding:16px;display:grid;gap:10px}
.sheet input,.sheet select,.sheet textarea{width:100%;padding:11px 12px;border:1px solid var(--line);border-radius:10px;background:var(--bg)}
.two{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.note{font-size:13px;color:var(--muted)}
</style>
</head>
<body>
<header><div class="bar"><span class="logo"><svg viewBox="0 0 38 30" role="img" aria-label="Логотип"><rect x="5" y="2" width="28" height="19" rx="3.5" fill="none" stroke="var(--accent)" stroke-width="2.6"/><path d="M15 8v7M23 8v7M15 11.5h8" stroke="var(--ink)" stroke-width="2.4" stroke-linecap="round"/><rect x="1" y="24" width="36" height="3.6" rx="1.8" fill="var(--accent)"/></svg>Ноутбукарий</span><button class="cartbtn sell" id="sell">Продать ноутбук</button><button class="cartbtn" id="open" aria-label="Открыть корзину">Корзина · <span id="cnt">0</span></button></div></header>

<section class="hero">
<h1>Ноутбуки для учёбы, работы и игр</h1>
<p>Новые ноутбуки из магазина и объявления от владельцев. Хотите продать свой? Нажмите «Продать ноутбук».</p>
</section>

<section class="tools" aria-label="Фильтры">
<input type="search" id="q" placeholder="Поиск по названию" aria-label="Поиск">
<select id="brand" aria-label="Бренд"><option value="">Все бренды</option></select>
<select id="sort" aria-label="Сортировка">
<option value="pop">Популярные</option><option value="asc">Сначала дешевле</option><option value="desc">Сначала дороже</option>
</select>
<div class="price"><label for="max"><span>Цена до</span><span id="maxv"></span></label><input type="range" id="max" min="40000" max="260000" step="5000" value="260000"></div>
</section>

<main class="grid" id="grid"></main>

<div class="modal" id="modal"><div class="sheet" role="dialog" aria-label="Новое объявление">
<h2 style="margin:0">Продать ноутбук</h2>
<div class="two"><select id="sb" aria-label="Бренд"><option>Apple</option><option>ASUS</option><option>Acer</option><option>Dell</option><option>HP</option><option>Lenovo</option><option>MSI</option><option>Другой</option></select><input id="sm" placeholder="Модель, например Vivobook 15"></div>
<input id="sc" placeholder="Процессор, например Core i5-1235U">
<div class="two"><input id="sr" type="number" min="1" placeholder="ОЗУ, ГБ"><input id="ss" type="number" min="0" placeholder="SSD, ГБ"></div>
<div class="two"><input id="sp" type="number" min="1" placeholder="Цена, сом"><select id="sk" aria-label="Состояние"><option>Новый</option><option>Отличное</option><option>Хорошее</option><option>Есть дефекты</option></select></div>
<div class="two"><input id="sy" placeholder="Город"><input id="st" inputmode="tel" placeholder="Телефон +996"></div>
<textarea id="sd" rows="2" placeholder="Описание: состояние, комплект, причина продажи"></textarea>
<label class="note">Фото ноутбука <input id="sf" type="file" accept="image/*"></label>
<div class="err" id="se"></div><div class="note" id="sn"></div>
<div class="two"><button class="call" id="spub">Опубликовать</button><button class="ghost" id="scan">Отмена</button></div>
</div></div>
<div class="shade" id="shade"></div>
<aside id="cart" aria-label="Корзина" aria-hidden="true">
<h2>Корзина <button class="x" id="close" aria-label="Закрыть">×</button></h2>
<div class="items" id="items"></div>
<div class="foot" id="foot"></div>
</aside>

<script>
var P=[
{id:1,brand:"Lenovo",name:"IdeaPad Slim 3",cpu:"Ryzen 5 7520U",ram:16,ssd:512,scr:15.6,kg:1.6,price:49990,c:"#8a97a6",pop:9,use:"Учёба"},
{id:2,brand:"ASUS",name:"Vivobook 15",cpu:"Core i5-1335U",ram:16,ssd:512,scr:15.6,kg:1.7,price:59990,c:"#5d7aa8",pop:8,use:"Офис"},
{id:3,brand:"Acer",name:"Aspire 5",cpu:"Core i7-1355U",ram:16,ssd:1024,scr:15.6,kg:1.8,price:72990,c:"#9aa3ad",pop:6,use:"Офис"},
{id:4,brand:"Apple",name:"MacBook Air 13",cpu:"Apple M3",ram:16,ssd:512,scr:13.6,kg:1.24,price:124990,c:"#c9ccd1",pop:10,use:"Работа"},
{id:5,brand:"HP",name:"Pavilion Plus 14",cpu:"Core Ultra 5",ram:16,ssd:512,scr:14,kg:1.4,price:84990,c:"#7b8fa1",pop:5,use:"Работа"},
{id:6,brand:"MSI",name:"Katana 15",cpu:"Core i7-13620H, RTX 4060",ram:16,ssd:1024,scr:15.6,kg:2.25,price:129990,c:"#2b2f38",pop:7,use:"Игры"},
{id:7,brand:"ASUS",name:"ROG Strix G16",cpu:"Core i9-14900HX, RTX 4070",ram:32,ssd:1024,scr:16,kg:2.5,price:199990,c:"#1d2230",pop:6,use:"Игры"},
{id:8,brand:"Apple",name:"MacBook Pro 14",cpu:"Apple M3 Pro",ram:18,ssd:1024,scr:14.2,kg:1.6,price:219990,c:"#3a3d42",pop:8,use:"Работа"},
{id:9,brand:"Xiaomi",name:"RedmiBook 15",cpu:"Core i3-1115G4",ram:8,ssd:256,scr:15.6,kg:1.8,price:42990,c:"#8f98a3",pop:7,use:"Учёба"},
{id:10,brand:"Acer",name:"Extensa 15",cpu:"Ryzen 3 7320U",ram:8,ssd:256,scr:15.6,kg:1.7,price:39990,c:"#a0a8b1",pop:6,use:"Учёба"},
{id:11,brand:"Lenovo",name:"V15 G4",cpu:"Core i5-13420H",ram:16,ssd:512,scr:15.6,kg:1.7,price:54990,c:"#6f7b88",pop:6,use:"Офис"},
{id:12,brand:"HP",name:"15-fd",cpu:"Core i5-1335U",ram:8,ssd:512,scr:15.6,kg:1.7,price:52990,c:"#97a1ac",pop:5,use:"Офис"},
{id:13,brand:"Honor",name:"MagicBook X16",cpu:"Core i5-12450H",ram:16,ssd:512,scr:16,kg:1.88,price:57990,c:"#7c8794",pop:6,use:"Офис"},
{id:14,brand:"Dell",name:"Inspiron 15",cpu:"Core i5-1334U",ram:16,ssd:512,scr:15.6,kg:1.65,price:64990,c:"#8b94a0",pop:5,use:"Офис"},
{id:15,brand:"Huawei",name:"MateBook D16",cpu:"Core i7-13700H",ram:16,ssd:1024,scr:16,kg:1.7,price:79990,c:"#a9afb8",pop:7,use:"Работа"},
{id:16,brand:"ASUS",name:"Zenbook 14 OLED",cpu:"Core Ultra 7",ram:16,ssd:1024,scr:14,kg:1.2,price:109990,c:"#5e7088",pop:8,use:"Работа"},
{id:17,brand:"Lenovo",name:"ThinkPad E14",cpu:"Core i5-1335U",ram:16,ssd:512,scr:14,kg:1.64,price:74990,c:"#2a2d33",pop:7,use:"Работа"},
{id:18,brand:"HP",name:"EliteBook 840",cpu:"Core i7-1355U",ram:32,ssd:1024,scr:14,kg:1.36,price:139990,c:"#6c7886",pop:5,use:"Работа"},
{id:19,brand:"Dell",name:"XPS 13",cpu:"Core Ultra 7",ram:16,ssd:512,scr:13.4,kg:1.19,price:149990,c:"#b4bac2",pop:6,use:"Работа"},
{id:20,brand:"Microsoft",name:"Surface Laptop 5",cpu:"Core i7-1255U",ram:16,ssd:512,scr:13.5,kg:1.27,price:134990,c:"#9fa8b8",pop:5,use:"Работа"},
{id:21,brand:"Samsung",name:"Galaxy Book4 Pro",cpu:"Core Ultra 7",ram:16,ssd:512,scr:14,kg:1.23,price:144990,c:"#8794a6",pop:5,use:"Работа"},
{id:22,brand:"Apple",name:"MacBook Air 15",cpu:"Apple M3",ram:16,ssd:512,scr:15.3,kg:1.51,price:154990,c:"#2f3a4a",pop:9,use:"Работа"},
{id:23,brand:"Apple",name:"MacBook Pro 16",cpu:"Apple M3 Max",ram:36,ssd:1024,scr:16.2,kg:2.14,price:259990,c:"#34373c",pop:6,use:"Работа"},
{id:24,brand:"Acer",name:"Nitro V 15",cpu:"Ryzen 5 7535HS, RTX 4050",ram:16,ssd:512,scr:15.6,kg:2.1,price:94990,c:"#2d3340",pop:8,use:"Игры"},
{id:25,brand:"Lenovo",name:"LOQ 15",cpu:"Core i5-12450H, RTX 3050",ram:16,ssd:512,scr:15.6,kg:2.4,price:89990,c:"#363b47",pop:8,use:"Игры"},
{id:26,brand:"HP",name:"Victus 16",cpu:"Ryzen 7 8845HS, RTX 4060",ram:16,ssd:1024,scr:16.1,kg:2.3,price:119990,c:"#2a3140",pop:6,use:"Игры"},
{id:27,brand:"Dell",name:"G15 5530",cpu:"Core i7-13650HX, RTX 4060",ram:16,ssd:512,scr:15.6,kg:2.5,price:134990,c:"#30343d",pop:5,use:"Игры"},
{id:28,brand:"ASUS",name:"TUF Gaming A15",cpu:"Ryzen 7 7735HS, RTX 4060",ram:16,ssd:512,scr:15.6,kg:2.2,price:114990,c:"#3b3f4a",pop:9,use:"Игры"},
{id:29,brand:"MSI",name:"Thin GF63",cpu:"Core i5-12450H, RTX 4050",ram:16,ssd:512,scr:15.6,kg:1.86,price:84990,c:"#262a34",pop:7,use:"Игры"},
{id:30,brand:"MSI",name:"Raider GE78",cpu:"Core i9-14900HX, RTX 4080",ram:32,ssd:2048,scr:17,kg:3.0,price:259990,c:"#1b1e27",pop:4,use:"Игры"},
{id:31,brand:"Lenovo",name:"Legion Pro 5",cpu:"Ryzen 7 7745HX, RTX 4070",ram:32,ssd:1024,scr:16,kg:2.5,price:189990,c:"#2c3039",pop:6,use:"Игры"},
{id:32,brand:"Xiaomi",name:"Redmi G Pro",cpu:"Core i7-14650HX, RTX 4060",ram:16,ssd:1024,scr:16,kg:2.5,price:124990,c:"#363c46",pop:5,use:"Игры"}
];
var cart={},$=function(i){return document.getElementById(i)};
function rub(n){return n.toLocaleString("ru-RU")+" сом"}
function pic(p){return '<svg viewBox="0 0 200 124" role="img" aria-label="'+p.brand+' '+p.name+'"><rect x="34" y="8" width="132" height="86" rx="7" fill="'+p.c+'"/><rect x="40" y="14" width="120" height="74" rx="3" fill="#0e1520"/><rect x="40" y="14" width="120" height="74" rx="3" fill="url(#g)" opacity=".55"/><path d="M12 98h176l-9 16a6 6 0 0 1-5 3H26a6 6 0 0 1-5-3z" fill="'+p.c+'"/><rect x="82" y="98" width="36" height="4" rx="2" fill="#0e1520" opacity=".3"/><defs><linearGradient id="g" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#4c6bff"/><stop offset="1" stop-color="#0e1520"/></linearGradient></defs></svg>'}
var brands=[].concat.apply([],P.map(function(p){return[p.brand]})).filter(function(b,i,a){return a.indexOf(b)==i}).sort();
brands.forEach(function(b){var o=document.createElement("option");o.value=o.textContent=b;$("brand").appendChild(o)});

function list(){
 var q=$("q").value.trim().toLowerCase(),b=$("brand").value,m=+$("max").value,s=$("sort").value;
 $("maxv").textContent=rub(m);
 var r=P.concat(L).filter(function(p){return(!b||p.brand==b)&&p.price<=m&&(p.brand+" "+p.name).toLowerCase().indexOf(q)>-1});
 r.sort(function(a,c){return s=="asc"?a.price-c.price:s=="desc"?c.price-a.price:c.pop-a.pop});
 $("grid").innerHTML=r.length?r.map(function(p){if(p.phone)return pcard(p);return '<article class="card"><div class="pic">'+pic(p)+'</div><div class="body"><span class="brand">'+p.brand+' · '+p.use+'</span><h3>'+p.name+'</h3><dl><dt>Процессор</dt><dd>'+p.cpu+'</dd><dt>Память</dt><dd>'+p.ram+' ГБ / SSD '+p.ssd+' ГБ</dd><dt>Экран</dt><dd>'+p.scr+'″</dd><dt>Вес</dt><dd>'+p.kg+' кг</dd></dl><div class="buy"><span class="cost">'+rub(p.price)+'</span><button class="add" data-id="'+p.id+'">В корзину</button></div></div></article>'}).join(""):'<p class="empty">Ничего не найдено. Измените бренд или увеличьте максимальную цену.</p>';
}
function total(){var t=0,n=0;for(var k in cart){var p=P.filter(function(x){return x.id==k})[0];t+=p.price*cart[k];n+=cart[k]}return{t:t,n:n}}
function drawCart(msg){
 var T=total();$("cnt").textContent=T.n;
 if(msg){$("items").innerHTML='<div class="done"><h3><strong>Заказ оформлен</strong></h3><p>'+msg+'</p></div>';$("foot").innerHTML='';return}
 if(!T.n){$("items").innerHTML='<p class="empty">В корзине пусто. Добавьте ноутбук из каталога.</p>';$("foot").innerHTML='';return}
 $("items").innerHTML=Object.keys(cart).map(function(k){var p=P.filter(function(x){return x.id==k})[0];return '<div class="row"><div><b>'+p.brand+' '+p.name+'</b><br><small>'+rub(p.price)+'</small></div><b>'+rub(p.price*cart[k])+'</b><div class="qty"><button data-d="-1" data-id="'+k+'" aria-label="Уменьшить">−</button><span>'+cart[k]+'</span><button data-d="1" data-id="'+k+'" aria-label="Увеличить">+</button><button class="rm" data-d="0" data-id="'+k+'">Убрать</button></div></div>'}).join("");
 $("foot").innerHTML='<div class="total"><span>Итого</span><span>'+rub(T.t)+'</span></div><input id="nm" placeholder="Имя" autocomplete="name"><input id="ph" placeholder="Телефон" inputmode="tel" autocomplete="tel"><div class="err" id="err"></div><button class="cartbtn" id="ord">Оформить заказ</button>';
}
function show(on){$("cart").classList.toggle("on",on);$("shade").classList.toggle("on",on);$("cart").setAttribute("aria-hidden",!on);if(on&&!document.getElementById("nm")&&!total().n)drawCart()}
document.addEventListener("click",function(e){
 var t=e.target.closest?(e.target.closest("button,a,[data-id]")||e.target):e.target,id=t.getAttribute&&t.getAttribute("data-id");
 if(t.classList.contains("add")){cart[id]=(cart[id]||0)+1;drawCart();t.textContent="Добавлено";setTimeout(function(){t.textContent="В корзину"},900)}
 else if(t.hasAttribute&&t.hasAttribute("data-d")){var d=+t.getAttribute("data-d");if(d==0||(cart[id]+d)<1)delete cart[id];else cart[id]+=d;drawCart()}
 else if(t.id=="ord"){var n=$("nm").value.trim(),p=$("ph").value.replace(/\D/g,"");
  if(n.length<2){$("err").textContent="Укажите имя.";return}
  if(p.length<10){$("err").textContent="Укажите телефон полностью.";return}
  var no=Math.floor(10000+Math.random()*89999);cart={};drawCart("Номер заказа "+no+". Менеджер позвонит вам, "+n+", в течение часа.")}
 else if(t.id=="open"||t.parentNode&&t.parentNode.id=="open"){if(!total().n)drawCart();show(true)}
 else if(t.id=="close"||t.id=="shade")show(false);
});
["q","brand","sort","max"].forEach(function(i){$(i).addEventListener("input",list)});
document.addEventListener("keydown",function(e){if(e.key=="Escape")show(false)});
var L=ld(),DB=null,uid="";
function ld(){try{return JSON.parse(localStorage.getItem("nb_l")||"[]")}catch(e){return[]}}
function sv(){try{localStorage.setItem("nb_l",JSON.stringify(L))}catch(e){}}
function esc(x){return String(x==null?"":x).replace(/[&<>"']/g,function(c){return{"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]})}
function pcard(p){var im=p.img&&String(p.img).indexOf("data:image/")==0?'<img alt="" src="'+esc(p.img)+'">':pic({brand:esc(p.brand),name:esc(p.name),c:"#8a97a6"});
 return '<article class="card priv"><div class="pic">'+im+'</div><div class="body"><span class="brand">От владельца · '+esc(p.city)+' · '+esc(p.cond)+'</span><h3>'+esc(p.brand+" "+p.name)+'</h3><dl><dt>Процессор</dt><dd>'+esc(p.cpu||"—")+'</dd><dt>Память</dt><dd>'+esc(p.ram||"—")+' ГБ / SSD '+esc(p.ssd||"—")+' ГБ</dd></dl><p class="tag">'+esc(p.desc||"")+'</p>'+(uid&&p.uid==uid||!DB&&p.local?'<button class="del" data-del="'+esc(p.id)+'">Снять с продажи</button>':'')+'<div class="buy"><span class="cost">'+rub(+p.price||0)+'</span><a class="call" href="tel:'+esc(String(p.phone).replace(/[^\d+]/g,""))+'">Позвонить</a></div></div></article>'}
function shrink(f,cb){var r=new FileReader();r.onload=function(){var im=new Image();im.onload=function(){var k=Math.mi
