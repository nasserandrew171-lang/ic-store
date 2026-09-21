<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ic_stor | سوق الأزياء</title>

<style>

*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Tahoma,Arial,sans-serif;
    background:#f7f5f2;
    color:#171717;
}

button,input{
    font-family:inherit;
}

button{
    cursor:pointer;
}

/* =========================
   شريط الشحن
========================= */

.top-bar{
    background:#111;
    color:#fff;
    text-align:center;
    padding:10px;
    font-size:14px;
}

/* =========================
   الهيدر
========================= */

header{
    background:#fff;
    position:sticky;
    top:0;
    z-index:1000;
    border-bottom:1px solid #ddd;
}

.header-main{
    height:90px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 6%;
}

.logo{
    font-family:Georgia,serif;
    font-size:40px;
    letter-spacing:5px;
}

.logo span{
    color:#b28a5a;
}

.header-icons{
    display:flex;
    align-items:center;
    gap:20px;
}

.icon-btn{
    border:0;
    background:none;
    font-size:27px;
    position:relative;
}

.count{
    position:absolute;
    top:-5px;
    right:-10px;
    background:#111;
    color:white;
    width:21px;
    height:21px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:11px;
}

/* =========================
   البحث
========================= */

.search-box{
    margin:0 4%;
    border-bottom:1px solid #bbb;
    display:flex;
    align-items:center;
    padding:8px 5px;
}

.search-box input{
    border:0;
    outline:none;
    width:100%;
    font-size:16px;
    background:transparent;
    padding:8px;
}

/* =========================
   القائمة
========================= */

nav{
    background:#fff;
    display:flex;
    justify-content:center;
    gap:55px;
    padding:18px 10px;
}

nav button{
    border:0;
    background:none;
    font-size:17px;
    color:#111;
}

nav button:hover{
    color:#a47a45;
}

/* =========================
   الصفحات
========================= */

.page{
    display:none;
    min-height:70vh;
}

.page.active{
    display:block;
}

/* =========================
   الرئيسية
========================= */

.hero{
    min-height:650px;
    position:relative;
    background:
    linear-gradient(rgba(0,0,0,.50),rgba(0,0,0,.68)),
    url("https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=1800&q=85");
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#fff;
    text-align:center;
}

.hero-content{
    max-width:750px;
    padding:30px;
}

.hero-small{
    letter-spacing:6px;
    font-size:14px;
    margin-bottom:25px;
}

.hero h1{
    font-family:Georgia,serif;
    font-size:70px;
    line-height:1.1;
    margin-bottom:25px;
}

.hero p{
    font-size:19px;
    line-height:2;
    margin-bottom:30px;
}

.hero-btn{
    border:0;
    background:#fff;
    color:#222;
    padding:17px 45px;
    font-size:16px;
}

/* =========================
   الأقسام
========================= */

.section{
    padding:65px 5%;
}

.section-title{
    text-align:center;
    margin-bottom:40px;
}

.section-title span{
    display:block;
    color:#999;
    letter-spacing:5px;
    font-size:12px;
    margin-bottom:12px;
}

.section-title h2{
    font-family:Georgia,serif;
    font-size:36px;
}

/* =========================
   المنتجات
========================= */

.products{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:25px;
}

.product{
    background:#fff;
    position:relative;
    overflow:hidden;
    border:1px solid #eee;
    cursor:pointer;
}

.product-image{
    height:330px;
    position:relative;
    overflow:hidden;
    background:#eee;
}

.product-image img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:.4s;
}

.product:hover .product-image img{
    transform:scale(1.05);
}

.favorite{
    position:absolute;
    top:12px;
    left:12px;
    width:40px;
    height:40px;
    border-radius:50%;
    border:0;
    background:#fff;
    font-size:21px;
    z-index:2;
}

.favorite.active{
    color:#c22;
}

.product-info{
    padding:15px;
}

.product-brand{
    color:#999;
    font-size:12px;
    margin-bottom:7px;
}

.product-name{
    font-size:16px;
    margin-bottom:9px;
}

.product-price{
    font-weight:bold;
    font-size:18px;
}

.product-actions{
    display:flex;
    gap:8px;
    margin-top:15px;
}

.add-cart{
    flex:1;
    background:#111;
    color:#fff;
    border:0;
    padding:12px;
}

/* =========================
   الصفحات الداخلية
========================= */

.inner-header{
    background:#111;
    color:#fff;
    padding:45px 7%;
}

.inner-header h1{
    font-family:Georgia,serif;
    font-size:42px;
    margin-bottom:10px;
}

.inner-header p{
    color:#ccc;
}

.page-content{
    padding:55px 5%;
}

/* =========================
   المحلات
========================= */

.stores{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:25px;
}

.store-card{
    background:#fff;
    border:1px solid #ddd;
    overflow:hidden;
    cursor:pointer;
    transition:.3s;
}

.store-card:hover{
    transform:translateY(-5px);
}

.store-cover{
    height:210px;
    position:relative;
    overflow:hidden;
}

.store-cover img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.store-logo{
    position:absolute;
    bottom:-35px;
    right:25px;
    width:75px;
    height:75px;
    border-radius:50%;
    background:#fff;
    border:4px solid #fff;
    overflow:hidden;
}

.store-logo img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.store-info{
    padding:50px 20px 20px;
}

.store-info h3{
    font-size:21px;
    margin-bottom:8px;
}

.store-info p{
    color:#777;
    font-size:14px;
    line-height:1.8;
}

.store-stats{
    display:flex;
    gap:18px;
    margin-top:15px;
    font-size:13px;
}

/* =========================
   صفحة التاجر
========================= */

.store-page-cover{
    height:350px;
    position:relative;
    background-size:cover;
    background-position:center;
}

.store-overlay{
    position:absolute;
    inset:0;
    background:linear-gradient(transparent,rgba(0,0,0,.85));
}

.store-profile{
    position:absolute;
    bottom:-70px;
    right:7%;
    left:7%;
    display:flex;
    align-items:flex-end;
    gap:20px;
    color:#fff;
}

.store-profile-logo{
    width:125px;
    height:125px;
    border-radius:50%;
    border:5px solid #fff;
    overflow:hidden;
    background:#fff;
    flex-shrink:0;
}

.store-profile-logo img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.store-profile-info{
    padding-bottom:12px;
}

.store-profile-info h1{
    font-size:34px;
    margin-bottom:8px;
}

.store-profile-info p{
    color:#eee;
}

.follow-btn{
    margin-right:auto;
    margin-bottom:15px;
    border:1px solid #fff;
    background:#fff;
    color:#111;
    padding:13px 28px;
}

.follow-btn.following{
    background:#111;
    color:#fff;
}

.store-details{
    background:#fff;
    margin-top:95px;
    padding:25px 7%;
    display:flex;
    flex-wrap:wrap;
    gap:40px;
    border-bottom:1px solid #ddd;
}

.store-detail strong{
    display:block;
    font-size:20px;
    margin-bottom:5px;
}

.store-detail span{
    color:#888;
    font-size:13px;
}

/* =========================
   صفحة المنتج
========================= */

.product-page-box{
    max-width:1100px;
    margin:50px auto;
    background:#fff;
    display:grid;
    grid-template-columns:1fr 1fr;
    box-shadow:0 5px 25px rgba(0,0,0,.08);
}

.product-page-image{
    min-height:600px;
}

.product-page-image img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.product-page-info{
    padding:50px;
}

.product-page-brand{
    color:#999;
    margin-bottom:12px;
}

.product-page-info h1{
    font-family:Georgia,serif;
    font-size:38px;
    margin-bottom:20px;
}

.product-page-price{
    font-size:27px;
    font-weight:bold;
    margin:20px 0;
}

.product-description{
    color:#666;
    line-height:2;
    margin-bottom:25px;
}

.size-title{
    margin-bottom:12px;
}

.sizes{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
    margin-bottom:25px;
}

.size{
    padding:11px 18px;
    border:1px solid #ccc;
    background:#fff;
}

.size.selected{
    background:#111;
    color:#fff;
}

.big-add{
    width:100%;
    padding:16px;
    background:#111;
    color:#fff;
    border:0;
    font-size:17px;
}

/* =========================
   السلة
========================= */

.cart-panel{
    position:fixed;
    top:0;
    left:-430px;
    width:400px;
    max-width:95%;
    height:100vh;
    background:#fff;
    z-index:3000;
    box-shadow:0 0 30px rgba(0,0,0,.2);
    transition:.3s;
    padding:25px;
    overflow:auto;
}

.cart-panel.open{
    left:0;
}

.cart-header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:25px;
}

.close{
    border:0;
    background:none;
    font-size:27px;
}

.cart-item{
    display:flex;
    gap:12px;
    border-bottom:1px solid #eee;
    padding:15px 0;
}

.cart-item img{
    width:80px;
    height:90px;
    object-fit:cover;
}

.cart-item-info{
    flex:1;
}

.qty{
    display:flex;
    align-items:center;
    gap:9px;
    margin-top:10px;
}

.qty button{
    width:26px;
    height:26px;
    border:1px solid #ddd;
    background:#fff;
}

.remove{
    color:#a00;
    background:none;
    border:0;
}

.cart-total{
    border-top:1px solid #ddd;
    margin-top:20px;
    padding-top:20px;
    display:flex;
    justify-content:space-between;
    font-size:20px;
    font-weight:bold;
}

.checkout{
    width:100%;
    background:#111;
    color:white;
    border:0;
    padding:16px;
    margin-top:20px;
}

/* =========================
   زر الرجوع
========================= */

.back-btn{
    background:#111;
    color:#fff;
    border:0;
    padding:13px 25px;
    margin:25px 5%;
}

/* =========================
   الحساب
========================= */

.account-box{
    max-width:600px;
    background:#fff;
    margin:30px auto;
    padding:40px;
    text-align:center;
}

.account-avatar{
    width:90px;
    height:90px;
    border-radius:50%;
    background:#111;
    color:#fff;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:40px;
    margin:0 auto 20px;
}

/* =========================
   زر الدعم
========================= */

.support-btn{
    position:fixed;
    bottom:85px;
    right:20px;
    width:58px;
    height:58px;
    border-radius:50%;
    border:0;
    background:#111;
    color:#fff;
    font-size:25px;
    box-shadow:0 5px 20px rgba(0,0,0,.25);
    z-index:2400;
    transition:.3s;
}

.support-btn:hover{
    transform:scale(1.08);
    background:#b28a5a;
}

/* =========================
   نافذة الدعم
========================= */

.support-overlay{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.55);
    z-index:4000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.support-overlay.open{
    display:flex;
}

.support-box{
    width:100%;
    max-width:430px;
    background:#fff;
    padding:30px;
    border-radius:14px;
    box-shadow:0 10px 40px rgba(0,0,0,.3);
    position:relative;
    animation:supportOpen .25s ease;
}

@keyframes supportOpen{

    from{
        opacity:0;
        transform:translateY(20px) scale(.96);
    }

    to{
        opacity:1;
        transform:translateY(0) scale(1);
    }

}

.support-close{
    position:absolute;
    top:12px;
    left:15px;
    border:0;
    background:none;
    font-size:28px;
    cursor:pointer;
    color:#555;
}

.support-title{
    text-align:center;
    margin-bottom:8px;
    font-family:Georgia,serif;
    font-size:28px;
}

.support-subtitle{
    text-align:center;
    color:#777;
    font-size:14px;
    margin-bottom:25px;
}

.support-item{
    display:flex;
    align-items:center;
    gap:15px;
    background:#f7f5f2;
    padding:15px;
    margin-bottom:12px;
    border-radius:10px;
}

.support-icon{
    width:42px;
    height:42px;
    border-radius:50%;
    background:#111;
    color:#fff;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:20px;
    flex-shrink:0;
}

.support-item-content{
    flex:1;
}

.support-item-content small{
    display:block;
    color:#888;
    margin-bottom:4px;
}

.support-item-content a{
    color:#111;
    text-decoration:none;
    font-weight:bold;
    word-break:break-word;
}

.support-item-content a:hover{
    color:#b28a5a;
}

/* =========================
   الفوتر
========================= */

footer{
    background:#111;
    color:#fff;
    padding:50px 7%;
    margin-top:60px;
}

.footer-logo{
    font-family:Georgia,serif;
    font-size:35px;
    letter-spacing:5px;
    margin-bottom:20px;
}

.footer-text{
    color:#bbb;
    line-height:2;
}

/* =========================
   تنقل الموبايل
========================= */

.mobile-nav{
    display:none;
}

/* =========================
   موبايل
========================= */

@media(max-width:1000px){

    .products{
        grid-template-columns:repeat(3,1fr);
    }

    .stores{
        grid-template-columns:repeat(2,1fr);
    }

    nav{
        gap:30px;
    }

}

@media(max-width:700px){

    body{
        padding-bottom:70px;
    }

    .header-main{
        height:75px;
        padding:0 18px;
    }

    .logo{
        font-size:28px;
        letter-spacing:3px;
    }

    .header-icons{
        gap:10px;
    }

    .icon-btn{
        font-size:23px;
    }

    nav{
        gap:20px;
        justify-content:flex-start;
        overflow-x:auto;
        padding:14px 16px;
    }

    nav button{
        white-space:nowrap;
        font-size:14px;
    }

    .hero{
        min-height:570px;
    }

    .hero h1{
        font-size:45px;
    }

    .hero p{
        font-size:15px;
    }

    .products{
        grid-template-columns:repeat(2,1fr);
        gap:10px;
    }

    .product-image{
        height:250px;
    }

    .product-info{
        padding:10px;
    }

    .product-name{
        font-size:14px;
    }

    .product-price{
        font-size:15px;
    }

    .product-actions{
        gap:5px;
    }

    .add-cart{
        padding:10px 5px;
        font-size:12px;
    }

    .stores{
        grid-template-columns:1fr;
    }

    .store-profile{
        right:20px;
        left:20px;
    }

    .store-profile-logo{
        width:90px;
        height:90px;
    }

    .store-profile-info h1{
        font-size:23px;
    }

    .follow-btn{
        padding:10px 15px;
    }

    .product-page-box{
        grid-template-columns:1fr;
        margin:20px 12px;
    }

    .product-page-image{
        min-height:400px;
        height:400px;
    }

    .product-page-info{
        padding:25px;
    }

    .product-page-info h1{
        font-size:29px;
    }

    .mobile-nav{
        display:flex;
        position:fixed;
        bottom:0;
        right:0;
        left:0;
        height:65px;
        background:#fff;
        border-top:1px solid #ddd;
        z-index:2500;
        justify-content:space-around;
    }

    .mobile-nav button{
        border:0;
        background:none;
        font-size:12px;
        color:#555;
        display:flex;
        flex-direction:column;
        align-items:center;
        justify-content:center;
        gap:4px;
    }

    .mobile-nav button.active{
        color:#111;
        font-weight:bold;
    }

    .support-btn{
        right:15px;
        bottom:80px;
        width:52px;
        height:52px;
        font-size:22px;
    }

    .support-box{
        padding:25px 18px;
    }

}

@media(max-width:450px){

    .products{
        grid-template-columns:repeat(2,1fr);
        gap:8px;
    }

    .product-image{
        height:215px;
    }

    .section{
        padding:45px 10px;
    }

    .product-actions{
        display:flex;
        flex-direction:row;
    }

    .add-cart{
        min-width:0;
    }

    .hero h1{
        font-size:38px;
    }

    .store-profile{
        gap:10px;
    }

    .store-profile-logo{
        width:70px;
        height:70px;
    }

    .store-profile-info h1{
        font-size:18px;
    }

}

</style>
</head>

<body>

<div class="top-bar">
    شحن مجاني فوق 1500 ج.م — استبدال واسترجاع خلال 14 يومًا
</div>

<header>

    <div class="header-main">

        <div class="header-icons">

            <button class="icon-btn" onclick="openCart()">
                🛍️
                <span class="count" id="cartCount">0</span>
            </button>

            <button class="icon-btn" onclick="goTo('favorites')">
                ♡
                <span class="count" id="favCount">0</span>
            </button>

        </div>

        <div class="logo">
            ic_stor<span>.</span>
        </div>

    </div>

    <div class="search-box">

        <input
            id="search"
            type="text"
            placeholder="ابحث في المتجر..."
            oninput="searchProducts()"
        >

        <span>⌕</span>

    </div>

    <nav>

        <button onclick="goTo('home')">
            الرئيسية
        </button>

        <button onclick="filterProducts('نساء')">
            نساء
        </button>

        <button onclick="filterProducts('رجال')">
            رجال
        </button>

        <button onclick="filterProducts('أطفال')">
            أطفال
        </button>

        <button onclick="filterProducts('أحذية')">
            أحذية
        </button>

        <button onclick="goTo('stores')">
            المحلات
        </button>

    </nav>

</header>


<!-- ==================================================
     الصفحة الرئيسية
================================================== -->

<div class="page active" id="page-home">

    <section class="hero">

        <div class="hero-content">

            <div class="hero-small">
                خريف / شتاء 2026
            </div>

            <h1>
                أناقتك<br>
                تبدأ من هنا
            </h1>

            <p>
                مجموعة جديدة تجمع بين البساطة والجودة،
                والتفاصيل التي تصنع الفرق.
            </p>

            <button
                class="hero-btn"
                onclick="goTo('products')"
            >
                تسوق المجموعة
            </button>

        </div>

    </section>

    <section class="section">

        <div class="section-title">

            <span>مختاراتنا</span>

            <h2>
                أحدث المنتجات
            </h2>

        </div>

        <div
            class="products"
            id="homeProducts"
        ></div>

    </section>

</div>


<!-- ==================================================
     صفحة المنتجات
================================================== -->

<div class="page" id="page-products">

    <div class="inner-header">

        <h1>
            المنتجات
        </h1>

        <p>
            اكتشف أحدث المنتجات من جميع المحلات
        </p>

    </div>

    <section class="page-content">

        <div
            class="products"
            id="allProducts"
        ></div>

    </section>

</div>


<!-- ==================================================
     صفحة المحلات
================================================== -->

<div class="page" id="page-stores">

    <div class="inner-header">

        <h1>
            المحلات
        </h1>

        <p>
            اكتشف جميع التجار والمحلات الموجودة على ic_stor
        </p>

    </div>

    <section class="page-content">

        <div
            class="stores"
            id="storesContainer"
        ></div>

    </section>

</div>


<!-- ==================================================
     صفحة التاجر
================================================== -->

<div class="page" id="page-store">

    <button
        class="back-btn"
        onclick="goTo('stores')"
    >
        ← العودة إلى المحلات
    </button>

    <div
        class="store-page-cover"
        id="storeCover"
    >

        <div class="store-overlay"></div>

        <div class="store-profile">

            <div class="store-profile-logo">

                <img
                    id="storeLogo"
                    src=""
                    alt=""
                >

            </div>

            <div class="store-profile-info">

                <h1 id="storeName"></h1>

                <p id="storeDescription"></p>

            </div>

            <button
                class="follow-btn"
                id="followBtn"
                onclick="toggleFollow()"
            >
                متابعة
            </button>

        </div>

    </div>

    <div class="store-details">

        <div class="store-detail">

            <strong id="storeProductsCount">
                0
            </strong>

            <span>
                منتج
            </span>

        </div>

        <div class="store-detail">

            <strong id="storeFollowers">
                0
            </strong>

            <span>
                متابع
            </span>

        </div>

        <div class="store-detail">

            <strong id="storeYears">
                0
            </strong>

            <span>
                عضو منذ
            </span>

        </div>

        <div class="store-detail">

            <strong id="storeLocation">
                -
            </strong>

            <span>
                موقع المحل
            </span>

        </div>

    </div>

    <section class="section">

        <div class="section-title">

            <span>
                منتجات التاجر
            </span>

            <h2 id="storeProductsTitle">
                منتجات المحل
            </h2>

        </div>

        <div
            class="products"
            id="storeProducts"
        ></div>

    </section>

</div>


<!-- ==================================================
     صفحة تفاصيل المنتج
================================================== -->

<div class="page" id="page-product">

    <button
        class="back-btn"
        onclick="goBackFromProduct()"
    >
        ← العودة
    </button>

    <div class="product-page-box">

        <div class="product-page-image">

            <img
                id="pageProductImage"
                src=""
                alt=""
            >

        </div>

        <div class="product-page-info">

            <div
                class="product-page-brand"
                id="pageProductBrand"
            ></div>

            <h1 id="pageProductName"></h1>

            <div
                class="product-page-price"
                id="pageProductPrice"
            ></div>

            <p
                class="product-description"
                id="pageProductDescription"
            ></p>

            <h3 class="size-title">
                اختر المقاس
            </h3>

            <div
                class="sizes"
                id="pageProductSizes"
            ></div>

            <button
                class="big-add"
                onclick="addPageProductToCart()"
            >
                أضف إلى السلة
            </button>

        </div>

    </div>

</div>


<!-- ==================================================
     صفحة المفضلة
================================================== -->

<div class="page" id="page-favorites">

    <div class="inner-header">

        <h1>
            المفضلة ❤️
        </h1>

        <p>
            المنتجات التي حفظتها
        </p>

    </div>

    <section class="page-content">

        <div
            class="products"
            id="favoriteProducts"
        ></div>

    </section>

</div>


<!-- ==================================================
     صفحة الحساب
================================================== -->

<div class="page" id="page-account">

    <div class="inner-header">

        <h1>
            حسابي
        </h1>

        <p>
            إدارة حسابك ومتابعتك
        </p>

    </div>

    <section class="page-content">

        <div class="account-box">

            <div class="account-avatar">
                👤
            </div>

            <h2>
                مرحبًا بك في ic_stor
            </h2>

            <p style="color:#777;margin-top:12px;line-height:2;">
                يمكنك لاحقًا إضافة بيانات الحساب
                والعناوين والطلبات من هنا.
            </p>

        </div>

    </section>

</div>


<!-- ==================================================
     السلة
================================================== -->

<div
    class="cart-panel"
    id="cartPanel"
>

    <div class="cart-header">

        <h2>
            سلة المشتريات
        </h2>

        <button
            class="close"
            onclick="closeCart()"
        >
            ×
        </button>

    </div>

    <div id="cartItems"></div>

    <div class="cart-total">

        <span>
            الإجمالي
        </span>

        <span id="cartTotal">
            0 ج.م
        </span>

    </div>

    <button
        class="checkout"
        onclick="checkout()"
    >
        إتمام الطلب
    </button>

</div>


<!-- ==================================================
     زر الدعم
================================================== -->

<button
    class="support-btn"
    onclick="openSupport()"
    aria-label="الدعم"
>
    💬
</button>


<!-- ==================================================
     نافذة الدعم
================================================== -->

<div
    class="support-overlay"
    id="supportOverlay"
    onclick="closeSupportOutside(event)"
>

    <div class="support-box">

        <button
            class="support-close"
            onclick="closeSupport()"
        >
            ×
        </button>

        <h2 class="support-title">
            الدعم
        </h2>

        <p class="support-subtitle">
            نحن هنا لمساعدتك
        </p>


        <!-- =========================
             الهاتف
             عدّل الرقم هنا
        ========================= -->

        <div class="support-item">

            <div class="support-icon">
                📞
            </div>

            <div class="support-item-content">

                <small>
                    الهاتف
                </small>

                <a href="tel:01000000000">
                    01000000000
                </a>

            </div>

        </div>


        <!-- =========================
             واتساب
             عدّل الرقم هنا
        ========================= -->

        <div class="support-item">

            <div class="support-icon">
                💬
            </div>

            <div class="support-item-content">

                <small>
                    واتساب
                </small>

                <a
                    href="https://wa.me/201000000000"
                    target="_blank"
                >
                    تواصل معنا عبر واتساب
                </a>

            </div>

        </div>


        <!-- =========================
             البريد الإلكتروني
             عدّل الإيميل هنا
        ========================= -->

        <div class="support-item">

            <div class="support-icon">
                ✉️
            </div>

            <div class="support-item-content">

                <small>
                    البريد الإلكتروني
                </small>

                <a href="mailto:support@icstor.com">
                    support@icstor.com
                </a>

            </div>

        </div>

    </div>

</div>


<!-- ==================================================
     تنقل الموبايل
================================================== -->

<div class="mobile-nav">

    <button
        id="navHome"
        onclick="goTo('home')"
    >
        🏠
        <span>الرئيسية</span>
    </button>

    <button
        id="navProducts"
        onclick="goTo('products')"
    >
        👕
        <span>المنتجات</span>
    </button>

    <button
        id="navStores"
        onclick="goTo('stores')"
    >
        🏪
        <span>المحلات</span>
    </button>

    <button
        id="navFavorites"
        onclick="goTo('favorites')"
    >
        ❤️
        <span>المفضلة</span>
    </button>

    <button
        id="navAccount"
        onclick="goTo('account')"
    >
        👤
        <span>حسابي</span>
    </button>

</div>


<footer>

    <div class="footer-logo">
        ic_stor<span>.</span>
    </div>

    <p class="footer-text">

        سوق أزياء عربي يجمع أفضل المحلات والتجار
        في مكان واحد.

        <br>

        تسوق بسهولة واكتشف منتجات جديدة.

    </p>

</footer>


<script>

/* ==================================================
   بيانات المحلات
================================================== */

const stores = [

    {
        id:1,
        name:"دار الأناقة",
        description:"أزياء نسائية عصرية بتصميمات راقية",
        followers:1280,
        years:4,
        location:"القاهرة - مدينة نصر",
        logo:"https://images.unsplash.com/photo-1551488831-00ddcb6c6bd3?auto=format&fit=crop&w=300&q=80",
        cover:"https://images.unsplash.com/photo-1445205170230-053b83016050?auto=format&fit=crop&w=1600&q=85"
    },

    {
        id:2,
        name:"ستايل مان",
        description:"أزياء رجالية عصرية وكاجوال",
        followers:890,
        years:3,
        location:"الجيزة - المهندسين",
        logo:"https://images.unsplash.com/photo-1617127365659-c47fa864d8bc?auto=format&fit=crop&w=300&q=80",
        cover:"https://images.unsplash.com/photo-1617127365659-c47fa864d8bc?auto=format&fit=crop&w=1600&q=85"
    },

    {
        id:3,
        name:"عالم الصغار",
        description:"أجمل ملابس الأطفال لجميع الأعمار",
        followers:620,
        years:2,
        location:"سوهاج - شارع الجمهورية",
        logo:"https://images.unsplash.com/photo-1519238263530-99bdd11df2ea?auto=format&fit=crop&w=300&q=80",
        cover:"https://images.unsplash.com/photo-1519238263530-99bdd11df2ea?auto=format&fit=crop&w=1600&q=85"
    },

    {
        id:4,
        name:"خطوة",
        description:"أحذية وشنط بتصميمات مميزة",
        followers:1560,
        years:5,
        location:"الإسكندرية - سموحة",
        logo:"https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=300&q=80",
        cover:"https://images.unsplash.com/photo-1495555961986-6d4c1ecb7be3?auto=format&fit=crop&w=1600&q=85"
    }

];


/* ==================================================
   المنتجات
================================================== */

const products = [

    {
        id:1,
        name:"فستان بيج أنيق",
        brand:"دار الأناقة",
        category:"نساء",
        store:1,
        price:1299,
        sizes:["S","M","L","XL"],
        image:"https://images.unsplash.com/photo-1595777457583-95e059d581b8?auto=format&fit=crop&w=800&q=85",
        description:"فستان أنيق مناسب للخروجات والمناسبات بتصميم بسيط وراقي."
    },

    {
        id:2,
        name:"جاكيت شتوي نسائي",
        brand:"دار الأناقة",
        category:"نساء",
        store:1,
        price:1599,
        sizes:["S","M","L"],
        image:"https://images.unsplash.com/photo-1548624313-0396c75ce8b1?auto=format&fit=crop&w=800&q=85",
        description:"جاكيت شتوي بتصميم عصري وخامة مناسبة للأجواء الباردة."
    },

    {
        id:3,
        name:"قميص رجالي أبيض",
        brand:"ستايل مان",
        category:"رجال",
        store:2,
        price:699,
        sizes:["M","L","XL","XXL"],
        image:"https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?auto=format&fit=crop&w=800&q=85",
        description:"قميص رجالي كلاسيكي مناسب للعمل والخروجات."
    },

    {
        id:4,
        name:"جاكيت رجالي",
        brand:"ستايل مان",
        category:"رجال",
        store:2,
        price:1899,
        sizes:["M","L","XL"],
        image:"https://images.unsplash.com/photo-1551028719-00167b16eac5?auto=format&fit=crop&w=800&q=85",
        description:"جاكيت رجالي أنيق بخامة عالية الجودة وتصميم عصري."
    },

    {
        id:5,
        name:"طقم أطفال شتوي",
        brand:"عالم الصغار",
        category:"أطفال",
        store:3,
        price:799,
        sizes:["4","6","8","10","12"],
        image:"https://images.unsplash.com/photo-1519457431-44ccd64a579b?auto=format&fit=crop&w=800&q=85",
        description:"طقم أطفال مريح وعملي للاستخدام اليومي."
    },

    {
        id:6,
        name:"بلوفر أطفال",
        brand:"عالم الصغار",
        category:"أطفال",
        store:3,
        price:499,
        sizes:["4","6","8","10"],
        image:"https://images.unsplash.com/photo-1503919545889-aef636e10ad4?auto=format&fit=crop&w=800&q=85",
        description:"بلوفر دافئ وناعم مناسب لفصل الشتاء."
    },

    {
        id:7,
        name:"حذاء رياضي أبيض",
        brand:"خطوة",
        category:"أحذية",
        store:4,
        price:999,
        sizes:["39","40","41","42","43","44"],
        image:"https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=800&q=85",
        description:"حذاء رياضي مريح للاستخدام اليومي والمشي."
    },

    {
        id:8,
        name:"حذاء كاجوال",
        brand:"خطوة",
        category:"أحذية",
        store:4,
        price:1199,
        sizes:["40","41","42","43"],
        image:"https://images.unsplash.com/photo-1525966222134-fcfa99b8ae77?auto=format&fit=crop&w=800&q=85",
        description:"حذاء كاجوال أنيق يناسب الإطلالات اليومية."
    }

];


/* ==================================================
   المتغيرات
================================================== */

let cart = [];
let favorites = [];

let currentFilter = "الكل";
let currentStore = null;

let currentProduct = null;
let selectedSize = "";

let previousPage = "products";


/* ==================================================
   نظام الصفحات
================================================== */

function goTo(page){

    document
        .querySelectorAll(".page")
        .forEach(p => p.classList.remove("active"));

    const target =
        document.getElementById("page-" + page);

    if(target){
        target.classList.add("active");
    }

    updateMobileNav(page);

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });

    if(page === "home"){
        renderHomeProducts();
    }

    if(page === "products"){
        renderAllProducts();
    }

    if(page === "stores"){
        renderStores();
    }

    if(page === "favorites"){
        renderFavorites();
    }

}


/* ==================================================
   تنقل الموبايل
================================================== */

function updateMobileNav(page){

    document
        .querySelectorAll(".mobile-nav button")
        .forEach(btn =>
            btn.classList.remove("active")
        );

    const map = {
        home:"navHome",
        products:"navProducts",
        stores:"navStores",
        favorites:"navFavorites",
        account:"navAccount"
    };

    if(map[page]){

        document
            .getElementById(map[page])
            .classList.add("active");

    }

}


/* ==================================================
   بطاقة المنتج
================================================== */

function createProductCard(product){

    const favorite =
        favorites.includes(product.id);

    return `

        <div
            class="product"
            onclick="openProduct(${product.id})"
        >

            <div class="product-image">

                <img
                    src="${product.image}"
                    alt="${product.name}"
                    loading="lazy"
                >

                <button
                    class="favorite ${favorite ? "active" : ""}"
                    onclick="event.stopPropagation(); toggleFavorite(${product.id})"
                >
                    ${favorite ? "♥" : "♡"}
                </button>

            </div>

            <div class="product-info">

                <div class="product-brand">
                    ${product.brand}
                </div>

                <div class="product-name">
                    ${product.name}
                </div>

                <div class="product-price">
                    ${product.price.toLocaleString()} ج.م
                </div>

                <div class="product-actions">

                    <button
                        class="add-cart"
                        onclick="event.stopPropagation(); addToCart(${product.id})"
                    >
                        أضف للسلة
                    </button>

                </div>

            </div>

        </div>

    `;
}


/* ==================================================
   عرض الرئيسية
================================================== */

function renderHomeProducts(){

    const container =
        document.getElementById("homeProducts");

    container.innerHTML = "";

    products
        .slice(0,4)
        .forEach(product => {

            container.innerHTML +=
                createProductCard(product);

        });

}


/* ==================================================
   عرض المنتجات
================================================== */

function renderAllProducts(){

    const container =
        document.getElementById("allProducts");

    const search =
        document
            .getElementById("search")
            .value
            .trim()
            .toLowerCase();

    const list =
        products.filter(product => {

            const categoryMatch =
                currentFilter === "الكل" ||
                product.category === currentFilter;

            const searchMatch =
                product.name
                    .toLowerCase()
                    .includes(search)
                ||
                product.brand
                    .toLowerCase()
                    .includes(search);

            return categoryMatch && searchMatch;

        });

    container.innerHTML = "";

    if(list.length === 0){

        container.innerHTML = `
            <p style="grid-column:1/-1;text-align:center;padding:60px;">
                لا توجد منتجات مطابقة للبحث.
            </p>
        `;

        return;
    }

    list.forEach(product => {

        container.innerHTML +=
            createProductCard(product);

    });

}


/* ==================================================
   البحث
================================================== */

function searchProducts(){

    currentFilter = "الكل";

    goTo("products");

}


/* ==================================================
   الفلترة
================================================== */

function filterProducts(category){

    currentFilter = category;

    goTo("products");

}


/* ==================================================
   المفضلة
================================================== */

function toggleFavorite(id){

    if(favorites.includes(id)){

        favorites =
            favorites.filter(
                item => item !== id
            );

    }else{

        favorites.push(id);

    }

    document.getElementById("favCount").textContent =
        favorites.length;

    renderHomeProducts();
    renderAllProducts();
    renderFavorites();

}


function renderFavorites(){

    const container =
        document.getElementById("favoriteProducts");

    const list =
        products.filter(
            p => favorites.includes(p.id)
        );

    container.innerHTML = "";

    if(list.length === 0){

        container.innerHTML = `
            <p style="grid-column:1/-1;text-align:center;padding:60px;">
                لا توجد منتجات في المفضلة حتى الآن ❤️
            </p>
        `;

        return;
    }

    list.forEach(product => {

        container.innerHTML +=
            createProductCard(product);

    });

}


/* ==================================================
   صفحة تفاصيل المنتج
================================================== */

function openProduct(id){

    const product =
        products.find(p => p.id === id);

    if(!product) return;

    currentProduct = product;

    previousPage =
        document
            .querySelector(".page.active")
            ?.id
            ?.replace("page-","")
        || "products";

    selectedSize =
        product.sizes[0];

    document.getElementById(
        "pageProductImage"
    ).src = product.image;

    document.getElementById(
        "pageProductImage"
    ).alt = product.name;

    document.getElementById(
        "pageProductBrand"
    ).textContent = product.brand;

    document.getElementById(
        "pageProductName"
    ).textContent = product.name;

    document.getElementById(
        "pageProductPrice"
    ).textContent =
        product.price.toLocaleString() + " ج.م";

    document.getElementById(
        "pageProductDescription"
    ).textContent =
        product.description;

    const sizes =
        document.getElementById(
            "pageProductSizes"
        );

    sizes.innerHTML = "";

    product.sizes.forEach(size => {

        sizes.innerHTML += `

            <button
                class="size ${size === selectedSize ? "selected" : ""}"
                onclick="selectProductSize('${size}',this)"
            >
                ${size}
            </button>

        `;

    });

    goTo("product");

}


function selectProductSize(size,button){

    selectedSize = size;

    document
        .querySelectorAll("#pageProductSizes .size")
        .forEach(btn =>
            btn.classList.remove("selected")
        );

    button.classList.add("selected");

}


function addPageProductToCart(){

    if(!currentProduct) return;

    addToCart(
        currentProduct.id,
        selectedSize
    );

}


function goBackFromProduct(){

    goTo(previousPage);

}


/* ==================================================
   السلة
================================================== */

function addToCart(id,size=null){

    const product =
        products.find(p => p.id === id);

    if(!product) return;

    if(!size){
        size = product.sizes[0];
    }

    const existing =
        cart.find(
            item =>
                item.id === id &&
                item.size === size
        );

    if(existing){

        existing.qty++;

    }else{

        cart.push({
            id:id,
            size:size,
            qty:1
        });

    }

    updateCart();

    alert("تمت إضافة المنتج إلى السلة 🛍️");

}


function updateCart(){

    document.getElementById(
        "cartCount"
    ).textContent =
        cart.reduce(
            (sum,item) =>
                sum + item.qty,
            0
        );

    const container =
        document.getElementById(
            "cartItems"
        );

    container.innerHTML = "";

    let total = 0;

    cart.forEach((item,index) => {

        const product =
            products.find(
                p => p.id === item.id
            );

        if(!product) return;

        total +=
            product.price *
            item.qty;

        container.innerHTML += `

            <div class="cart-item">

                <img
                    src="${product.image}"
                    alt="${product.name}"
                >

                <div class="cart-item-info">

                    <h4>
                        ${product.name}
                    </h4>

                    <div>
                        ${product.price.toLocaleString()} ج.م
                    </div>

                    <div>
                        المقاس: ${item.size}
                    </div>

                    <div class="qty">

                        <button
                            onclick="changeQty(${index},-1)"
                        >
                            -
                        </button>

                        <span>
                            ${item.qty}
                        </span>

                        <button
                            onclick="changeQty(${index},1)"
                        >
                            +
                        </button>

                        <button
                            class="remove"
                            onclick="removeFromCart(${index})"
                        >
                            حذف
                        </button>

                    </div>

                </div>

            </div>

        `;

    });

    document.getElementById(
        "cartTotal"
    ).textContent =
        total.toLocaleString() + " ج.م";

}


function changeQty(index,value){

    cart[index].qty += value;

    if(cart[index].qty <= 0){

        cart.splice(index,1);

    }

    updateCart();

}


function removeFromCart(index){

    cart.splice(index,1);

    updateCart();

}


function openCart(){

    document
        .getElementById("cartPanel")
        .classList.add("open");

    updateCart();

}


function closeCart(){

    document
        .getElementById("cartPanel")
        .classList.remove("open");

}


function checkout(){

    if(cart.length === 0){

        alert("السلة فارغة.");

        return;
    }

    alert(
        "تم تجهيز طلبك بنجاح! سيتم استكمال بيانات الشحن والدفع في الخطوة التالية."
    );

}


/* ==================================================
   المحلات
================================================== */

function renderStores(){

    const container =
        document.getElementById(
            "storesContainer"
        );

    container.innerHTML = "";

    stores.forEach(store => {

        const storeProducts =
            products.filter(
                p => p.store === store.id
            );

        container.innerHTML += `

            <div
                class="store-card"
                onclick="openStore(${store.id})"
            >

                <div class="store-cover">

                    <img
                        src="${store.cover}"
                        alt="${store.name}"
                        loading="lazy"
                    >

                    <div class="store-logo">

                        <img
                            src="${store.logo}"
                            alt="${store.name}"
                        >

                    </div>

                </div>

                <div class="store-info">

                    <h3>
                        ${store.name}
                    </h3>

                    <p>
                        ${store.description}
                    </p>

                    <div class="store-stats">

                        <span>
                            👕 ${storeProducts.length} منتجات
                        </span>

                        <span>
                            👥 ${store.followers.toLocaleString()} متابع
                        </span>

                    </div>

                </div>

            </div>

        `;

    });

}


/* ==================================================
   صفحة التاجر
================================================== */

function openStore(id){

    const store =
        stores.find(
            s => s.id === id
        );

    if(!store) return;

    currentStore = store;

    document.getElementById(
        "storeCover"
    ).style.backgroundImage =
        `url("${store.cover}")`;

    document.getElementById(
        "storeLogo"
    ).src = store.logo;

    document.getElementById(
        "storeName"
    ).textContent = store.name;

    document.getElementById(
        "storeDescription"
    ).textContent =
        store.description;

    const storeProducts =
        products.filter(
            p => p.store === store.id
        );

    document.getElementById(
        "storeProductsCount"
    ).textContent =
        storeProducts.length;

    document.getElementById(
        "storeFollowers"
    ).textContent =
        store.followers.toLocaleString();

    document.getElementById(
        "storeYears"
    ).textContent =
        store.years + " أعوام";

    document.getElementById(
        "storeLocation"
    ).textContent =
        store.location;

    document.getElementById(
        "storeProductsTitle"
    ).textContent =
        "منتجات " + store.name;

    const container =
        document.getElementById(
            "storeProducts"
        );

    container.innerHTML = "";

    storeProducts.forEach(product => {

        container.innerHTML +=
            createProductCard(product);

    });

    updateFollowButton();

    goTo("store");

}


/* ==================================================
   المتابعة
================================================== */

function getFollowedStores(){

    return JSON.parse(
        localStorage.getItem(
            "followedStores"
        ) || "[]"
    );

}


function toggleFollow(){

    if(!currentStore) return;

    let followed =
        getFollowedStores();

    if(
        followed.includes(
            currentStore.id
        )
    ){

        followed =
            followed.filter(
                id =>
                    id !== currentStore.id
            );

        currentStore.followers--;

    }else{

        followed.push(
            currentStore.id
        );

        currentStore.followers++;

    }

    localStorage.setItem(
        "followedStores",
        JSON.stringify(followed)
    );

    document.getElementById(
        "storeFollowers"
    ).textContent =
        currentStore.followers.toLocaleString();

    updateFollowButton();

    renderStores();

}


function updateFollowButton(){

    if(!currentStore) return;

    const followed =
        getFollowedStores();

    const button =
        document.getElementById(
            "followBtn"
        );

    if(
        followed.includes(
            currentStore.id
        )
    ){

        button.textContent =
            "✓ تمت المتابعة";

        button.classList.add(
            "following"
        );

    }else{

        button.textContent =
            "متابعة";

        button.classList.remove(
            "following"
        );

    }

}


/* ==================================================
   نظام الدعم
================================================== */

function openSupport(){

    document
        .getElementById("supportOverlay")
        .classList.add("open");

}


function closeSupport(){

    document
        .getElementById("supportOverlay")
        .classList.remove("open");

}


function closeSupportOutside(event){

    if(
        event.target ===
        document.getElementById("supportOverlay")
    ){

        closeSupport();

    }

}


/* إغلاق الدعم بزر ESC */

document.addEventListener("keydown",function(event){

    if(event.key === "Escape"){

        closeSupport();

    }

});


/* ==================================================
   التشغيل
================================================== */

renderHomeProducts();

renderAllProducts();

renderStores();

renderFavorites();

updateCart();

updateMobileNav("home");

</script>

</body>
</html>
