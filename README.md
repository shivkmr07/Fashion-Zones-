# Fashion-Zones-
Welcome to Fashion Zones — your one-stop store for trendy products, home &amp; kitchen solutions, everyday essentials, garden tools, and smart utility items. We carefully select useful, affordable, and quality products that add comfort, style, and convenience to your daily life.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fashion Zones – Smart Living, Delivered</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ============================================================
   CSS VARIABLES & RESET
============================================================ */
:root {
  --cream: #faf7f2;
  --warm-white: #fff9f3;
  --terracotta: #c8603a;
  --terracotta-dark: #a84e2c;
  --terracotta-light: #e8845e;
  --amber: #d4843e;
  --sand: #e8d5b7;
  --sand-dark: #c9b99a;
  --charcoal: #2c2416;
  --warm-gray: #7a6e62;
  --light-gray: #f0ebe3;
  --success: #5a8a5a;
  --font-head: 'Playfair Display', Georgia, serif;
  --font-body: 'DM Sans', sans-serif;
  --radius: 12px;
  --shadow: 0 4px 24px rgba(44,36,22,0.10);
  --shadow-lg: 0 8px 40px rgba(44,36,22,0.16);
  --transition: 0.28s cubic-bezier(0.4,0,0.2,1);
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  font-family: var(--font-body);
  background: var(--cream);
  color: var(--charcoal);
  min-height: 100vh;
  overflow-x: hidden;
}
a { text-decoration: none; color: inherit; }
img { max-width: 100%; display: block; }
button { cursor: pointer; border: none; background: none; font-family: var(--font-body); }

/* ============================================================
   PRODUCTS DATA — EDIT HERE
============================================================ */
/* (Data is in JS below) */

/* ============================================================
   NAVBAR
============================================================ */
#navbar {
  position: sticky; top: 0; z-index: 1000;
  background: var(--warm-white);
  border-bottom: 1.5px solid var(--sand);
  box-shadow: 0 2px 12px rgba(44,36,22,0.07);
}
.nav-inner {
  max-width: 1200px; margin: 0 auto;
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px 20px;
  gap: 16px;
}
.nav-logo {
  font-family: var(--font-head);
  font-size: 1.6rem; font-weight: 900;
  color: var(--terracotta);
  letter-spacing: -0.5px;
  line-height: 1;
}
.nav-logo span { color: var(--charcoal); }
.nav-tagline {
  font-size: 0.7rem; color: var(--warm-gray);
  letter-spacing: 0.08em; text-transform: uppercase;
  display: block; margin-top: 2px;
}
.nav-actions { display: flex; align-items: center; gap: 12px; }
.nav-cart-btn {
  position: relative;
  background: var(--terracotta);
  color: #fff;
  padding: 9px 18px;
  border-radius: 50px;
  font-size: 0.9rem; font-weight: 600;
  display: flex; align-items: center; gap: 7px;
  transition: background var(--transition), transform var(--transition);
}
.nav-cart-btn:hover { background: var(--terracotta-dark); transform: translateY(-1px); }
.cart-count {
  background: #fff;
  color: var(--terracotta);
  font-size: 0.72rem; font-weight: 700;
  border-radius: 50%; width: 20px; height: 20px;
  display: inline-flex; align-items: center; justify-content: center;
  line-height: 1;
}
.nav-home-btn {
  font-size: 0.88rem; font-weight: 500;
  color: var(--warm-gray);
  padding: 8px 14px;
  border-radius: 50px;
  transition: background var(--transition), color var(--transition);
}
.nav-home-btn:hover { background: var(--light-gray); color: var(--charcoal); }

/* ============================================================
   PAGES
============================================================ */
.page { display: none; }
.page.active { display: block; }

/* ============================================================
   HOME — HERO
============================================================ */
.hero {
  background: linear-gradient(135deg, #2c2416 0%, #4a3520 40%, #c8603a 100%);
  position: relative; overflow: hidden;
  padding: 70px 20px 60px;
  text-align: center;
}
.hero::before {
  content: '';
  position: absolute; inset: 0;
  background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.04'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
}
.hero-content { position: relative; z-index: 1; max-width: 680px; margin: 0 auto; }
.hero-badge {
  display: inline-block;
  background: rgba(255,255,255,0.15);
  color: #f5d9a8;
  font-size: 0.75rem; font-weight: 600;
  letter-spacing: 0.12em; text-transform: uppercase;
  padding: 5px 16px; border-radius: 50px;
  border: 1px solid rgba(245,217,168,0.3);
  margin-bottom: 18px;
}
.hero h1 {
  font-family: var(--font-head);
  font-size: clamp(2rem, 5vw, 3.2rem);
  font-weight: 900; color: #fff;
  line-height: 1.12; margin-bottom: 14px;
}
.hero h1 em { color: #f5d9a8; font-style: normal; }
.hero p {
  color: rgba(255,255,255,0.75);
  font-size: 1.05rem; line-height: 1.65;
  margin-bottom: 28px;
}
.hero-cta {
  display: inline-flex; align-items: center; gap: 8px;
  background: var(--sand);
  color: var(--charcoal);
  font-size: 0.95rem; font-weight: 700;
  padding: 13px 28px; border-radius: 50px;
  transition: background var(--transition), transform var(--transition), box-shadow var(--transition);
  box-shadow: 0 4px 20px rgba(0,0,0,0.2);
}
.hero-cta:hover { background: #fff; transform: translateY(-2px); box-shadow: 0 8px 28px rgba(0,0,0,0.3); }

/* ============================================================
   CATEGORY SCROLL STRIP
============================================================ */
.cat-strip-section {
  background: var(--warm-white);
  padding: 32px 0 28px;
  border-bottom: 1.5px solid var(--sand);
}
.cat-strip-title {
  text-align: center;
  font-family: var(--font-head);
  font-size: 1.05rem; font-weight: 700;
  color: var(--warm-gray);
  letter-spacing: 0.06em; text-transform: uppercase;
  margin-bottom: 22px;
}
.cat-scroll-wrapper {
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  scrollbar-width: none;
  padding: 6px 28px 10px;
  cursor: grab;
}
.cat-scroll-wrapper:active { cursor: grabbing; }
.cat-scroll-wrapper::-webkit-scrollbar { display: none; }
.cat-scroll-track {
  display: flex; gap: 24px;
  width: max-content;
  margin: 0 auto;
}
.cat-icon-item {
  display: flex; flex-direction: column; align-items: center;
  gap: 10px; cursor: pointer;
  transition: transform var(--transition);
  user-select: none;
  min-width: 100px;
}
.cat-icon-item:hover { transform: translateY(-5px) scale(1.04); }
.cat-icon-item:active { transform: scale(0.96); }
.cat-circle {
  width: 88px; height: 88px; border-radius: 50%;
  overflow: hidden;
  border: 3px solid var(--sand);
  box-shadow: 0 4px 18px rgba(44,36,22,0.13);
  transition: border-color var(--transition), box-shadow var(--transition);
  background: var(--light-gray);
  flex-shrink: 0;
}
.cat-circle img { width: 100%; height: 100%; object-fit: cover; }
.cat-icon-item:hover .cat-circle {
  border-color: var(--terracotta);
  box-shadow: 0 6px 24px rgba(200,96,58,0.28);
}
.cat-label {
  font-size: 0.78rem; font-weight: 600;
  color: var(--charcoal);
  text-align: center; line-height: 1.25;
  max-width: 90px;
}

/* ============================================================
   FILTER BAR
============================================================ */
.filter-section {
  max-width: 1200px; margin: 36px auto 0;
  padding: 0 20px;
}
.filter-section h2 {
  font-family: var(--font-head);
  font-size: 1.8rem; font-weight: 700;
  margin-bottom: 16px;
  color: var(--charcoal);
}
.filter-bar {
  display: flex; flex-wrap: wrap; gap: 8px;
  margin-bottom: 28px;
}
.filter-btn {
  padding: 7px 18px; border-radius: 50px;
  font-size: 0.83rem; font-weight: 600;
  border: 1.5px solid var(--sand-dark);
  color: var(--warm-gray);
  background: var(--warm-white);
  transition: all var(--transition);
  letter-spacing: 0.02em;
}
.filter-btn:hover { border-color: var(--terracotta); color: var(--terracotta); background: #fff5f1; }
.filter-btn.active {
  background: var(--terracotta); color: #fff;
  border-color: var(--terracotta);
}

/* ============================================================
   PRODUCT GRID
============================================================ */
.product-grid {
  max-width: 1200px; margin: 0 auto 60px;
  padding: 0 20px;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  gap: 24px;
}
.product-card {
  background: var(--warm-white);
  border-radius: var(--radius);
  overflow: hidden;
  border: 1.5px solid var(--sand);
  transition: box-shadow var(--transition), transform var(--transition), border-color var(--transition);
  display: flex; flex-direction: column;
  cursor: pointer;
}
.product-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
  border-color: var(--sand-dark);
}
.card-img-wrap {
  position: relative; overflow: hidden;
  aspect-ratio: 1 / 1;
  background: var(--light-gray);
}
.card-img-wrap img {
  width: 100%; height: 100%; object-fit: cover;
  transition: transform 0.45s cubic-bezier(0.4,0,0.2,1);
}
.product-card:hover .card-img-wrap img { transform: scale(1.07); }
.card-category-badge {
  position: absolute; top: 10px; left: 10px;
  background: rgba(255,249,243,0.92);
  color: var(--terracotta);
  font-size: 0.68rem; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.08em;
  padding: 3px 10px; border-radius: 50px;
  border: 1px solid var(--sand);
}
.card-body { padding: 14px 16px 16px; flex: 1; display: flex; flex-direction: column; }
.card-name {
  font-family: var(--font-head);
  font-size: 1rem; font-weight: 700;
  color: var(--charcoal);
  line-height: 1.3; margin-bottom: 8px;
  flex: 1;
}
.card-price {
  font-size: 1.15rem; font-weight: 700;
  color: var(--terracotta);
  margin-bottom: 12px;
  font-family: var(--font-head);
}
.card-price .original { text-decoration: line-through; color: var(--warm-gray); font-size: 0.82rem; margin-left: 6px; font-family: var(--font-body); }
.card-actions { display: flex; gap: 8px; }
.btn-view {
  flex: 1; padding: 9px 12px;
  border-radius: 8px;
  background: var(--light-gray);
  color: var(--charcoal);
  font-size: 0.82rem; font-weight: 600;
  transition: background var(--transition), color var(--transition);
  text-align: center;
}
.btn-view:hover { background: var(--sand); }
.btn-cart {
  flex: 1.4; padding: 9px 12px;
  border-radius: 8px;
  background: var(--terracotta);
  color: #fff;
  font-size: 0.82rem; font-weight: 600;
  transition: background var(--transition), transform var(--transition);
  text-align: center;
}
.btn-cart:hover { background: var(--terracotta-dark); transform: scale(1.02); }
.btn-cart.in-cart { background: var(--success); }
.btn-cart.in-cart:hover { background: #4a7a4a; }

/* ============================================================
   PRODUCT DETAIL PAGE
============================================================ */
.product-detail { max-width: 1200px; margin: 0 auto; padding: 30px 20px 60px; }
.back-btn {
  display: inline-flex; align-items: center; gap: 6px;
  color: var(--warm-gray); font-size: 0.87rem; font-weight: 500;
  margin-bottom: 24px;
  padding: 6px 0;
  transition: color var(--transition);
}
.back-btn:hover { color: var(--terracotta); }
.pd-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  align-items: start;
  margin-bottom: 48px;
}
@media(max-width:768px){ .pd-grid { grid-template-columns: 1fr; gap: 28px; } }

/* Gallery */
.pd-gallery { position: sticky; top: 90px; }
.main-img-wrap {
  border-radius: var(--radius);
  overflow: hidden;
  aspect-ratio: 1/1;
  background: var(--light-gray);
  margin-bottom: 12px;
  border: 1.5px solid var(--sand);
}
.main-img-wrap img { width: 100%; height: 100%; object-fit: cover; }
.thumb-strip {
  display: flex; gap: 8px;
  overflow-x: auto; scrollbar-width: none;
  padding-bottom: 4px;
}
.thumb-strip::-webkit-scrollbar { display: none; }
.thumb {
  width: 64px; height: 64px; flex-shrink: 0;
  border-radius: 8px; overflow: hidden;
  border: 2px solid transparent;
  cursor: pointer;
  transition: border-color var(--transition), opacity var(--transition);
  background: var(--light-gray);
}
.thumb img { width: 100%; height: 100%; object-fit: cover; }
.thumb.active { border-color: var(--terracotta); }
.thumb:hover { opacity: 0.85; }

/* Product Info */
.pd-info {}
.pd-category-tag {
  display: inline-block;
  background: #fff5f1; color: var(--terracotta);
  font-size: 0.72rem; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.1em;
  padding: 4px 12px; border-radius: 50px;
  border: 1px solid #f5d4c0;
  margin-bottom: 12px;
}
.pd-name {
  font-family: var(--font-head);
  font-size: clamp(1.4rem, 3vw, 2rem);
  font-weight: 900; color: var(--charcoal);
  line-height: 1.2; margin-bottom: 14px;
}
.pd-price-row { display: flex; align-items: baseline; gap: 10px; margin-bottom: 20px; }
.pd-price {
  font-family: var(--font-head);
  font-size: 1.9rem; font-weight: 700;
  color: var(--terracotta);
}
.pd-stock {
  font-size: 0.78rem; font-weight: 600;
  color: var(--success);
  background: #edf7ed; padding: 3px 10px; border-radius: 50px;
}
.pd-short-desc {
  color: var(--warm-gray);
  font-size: 0.93rem; line-height: 1.7;
  margin-bottom: 24px;
  border-left: 3px solid var(--sand-dark);
  padding-left: 14px;
}
.qty-row { display: flex; align-items: center; gap: 12px; margin-bottom: 20px; }
.qty-label { font-size: 0.85rem; font-weight: 600; color: var(--warm-gray); }
.qty-control {
  display: flex; align-items: center;
  border: 1.5px solid var(--sand-dark);
  border-radius: 8px; overflow: hidden;
}
.qty-btn {
  width: 36px; height: 36px;
  background: var(--light-gray);
  color: var(--charcoal);
  font-size: 1.1rem; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  transition: background var(--transition);
}
.qty-btn:hover { background: var(--sand); }
.qty-num {
  width: 44px; text-align: center;
  font-size: 0.95rem; font-weight: 700;
  color: var(--charcoal);
  line-height: 36px;
  border-left: 1.5px solid var(--sand);
  border-right: 1.5px solid var(--sand);
}
.add-cart-main {
  width: 100%;
  background: var(--terracotta);
  color: #fff;
  font-size: 1rem; font-weight: 700;
  padding: 15px;
  border-radius: 10px;
  transition: background var(--transition), transform var(--transition), box-shadow var(--transition);
  letter-spacing: 0.02em;
  display: flex; align-items: center; justify-content: center; gap: 8px;
  margin-bottom: 14px;
}
.add-cart-main:hover { background: var(--terracotta-dark); transform: translateY(-2px); box-shadow: 0 6px 20px rgba(200,96,58,0.35); }
.add-cart-main.in-cart { background: var(--success); }
.add-cart-main.in-cart:hover { background: #4a7a4a; }

/* Info pills */
.pd-meta-pills {
  display: flex; flex-wrap: wrap; gap: 8px;
  margin-top: 16px; padding-top: 16px;
  border-top: 1px solid var(--sand);
}
.meta-pill {
  font-size: 0.75rem; font-weight: 500;
  color: var(--warm-gray);
  background: var(--light-gray);
  padding: 5px 12px; border-radius: 50px;
  display: flex; align-items: center; gap: 4px;
}

/* ============================================================
   ACCORDION — Product Detail Sections
============================================================ */
.accordion-section {
  max-width: 1200px; margin: 0 auto 48px;
  padding: 0 20px;
}
.accordion-title-main {
  font-family: var(--font-head);
  font-size: 1.4rem; font-weight: 700;
  color: var(--charcoal);
  margin-bottom: 16px;
}
.accordion-list { display: flex; flex-direction: column; gap: 0; border: 1.5px solid var(--sand); border-radius: var(--radius); overflow: hidden; }
.accordion-item {}
.accordion-item + .accordion-item { border-top: 1.5px solid var(--sand); }
.accordion-header {
  width: 100%;
  display: flex; align-items: center; justify-content: space-between;
  padding: 16px 20px;
  background: var(--warm-white);
  transition: background var(--transition);
  text-align: left;
}
.accordion-header:hover { background: var(--light-gray); }
.accordion-header-text {
  display: flex; align-items: center; gap: 10px;
  font-size: 0.97rem; font-weight: 700;
  color: var(--charcoal);
}
.accordion-icon-label {
  font-size: 1rem;
}
.accordion-toggle {
  width: 26px; height: 26px;
  border-radius: 50%;
  background: var(--sand);
  color: var(--charcoal);
  font-size: 1.1rem; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  transition: background var(--transition), transform var(--transition);
  flex-shrink: 0;
}
.accordion-item.open .accordion-toggle {
  background: var(--terracotta); color: #fff;
  transform: rotate(45deg);
}
.accordion-body {
  max-height: 0; overflow: hidden;
  transition: max-height 0.38s cubic-bezier(0.4,0,0.2,1);
}
.accordion-item.open .accordion-body { max-height: 2000px; }
.accordion-body-inner {
  padding: 0 20px 20px;
  font-size: 0.9rem; line-height: 1.8;
  color: var(--warm-gray);
}
.accordion-body-inner ul {
  list-style: none; padding: 0;
  display: flex; flex-direction: column; gap: 6px;
}
.accordion-body-inner ul li::before {
  content: '•';
  color: var(--terracotta);
  font-weight: 700;
  margin-right: 8px;
}
.accordion-body-inner p { margin-bottom: 10px; }

/* ============================================================
   RELATED PRODUCTS
============================================================ */
.related-section {
  max-width: 1200px; margin: 0 auto 60px;
  padding: 0 20px;
}
.related-section h2 {
  font-family: var(--font-head);
  font-size: 1.5rem; font-weight: 700;
  color: var(--charcoal); margin-bottom: 20px;
}
.related-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 18px;
}

/* ============================================================
   CART PAGE
============================================================ */
.cart-page { max-width: 900px; margin: 0 auto; padding: 36px 20px 60px; }
.cart-page h1 {
  font-family: var(--font-head);
  font-size: 2rem; font-weight: 800;
  margin-bottom: 28px; color: var(--charcoal);
}
.cart-empty {
  text-align: center; padding: 60px 20px;
}
.cart-empty svg { margin: 0 auto 18px; }
.cart-empty p {
  font-size: 1.1rem; color: var(--warm-gray);
  margin-bottom: 20px;
}
.cart-table { width: 100%; border-collapse: collapse; margin-bottom: 28px; }
.cart-table th {
  text-align: left; padding: 10px 12px;
  font-size: 0.78rem; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.08em;
  color: var(--warm-gray);
  border-bottom: 1.5px solid var(--sand);
}
.cart-table td {
  padding: 14px 12px;
  border-bottom: 1px solid var(--light-gray);
  vertical-align: middle;
}
.cart-item-img {
  width: 60px; height: 60px; object-fit: cover;
  border-radius: 8px; border: 1.5px solid var(--sand);
}
.cart-item-name { font-weight: 600; font-size: 0.9rem; }
.cart-item-price { color: var(--terracotta); font-weight: 700; }
.cart-qty-ctrl {
  display: flex; align-items: center; gap: 4px;
}
.cqb {
  width: 28px; height: 28px;
  background: var(--light-gray);
  border-radius: 6px;
  font-size: 0.95rem; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  transition: background var(--transition);
}
.cqb:hover { background: var(--sand); }
.cart-qty-num { min-width: 28px; text-align: center; font-weight: 700; font-size: 0.9rem; }
.cart-remove { color: var(--warm-gray); font-size: 1.1rem; transition: color var(--transition); padding: 4px; }
.cart-remove:hover { color: #c0392b; }
.cart-total-box {
  background: var(--warm-white);
  border: 1.5px solid var(--sand);
  border-radius: var(--radius);
  padding: 22px 24px;
  max-width: 360px; margin-left: auto;
}
.cart-total-row {
  display: flex; justify-content: space-between;
  font-size: 0.9rem; color: var(--warm-gray);
  margin-bottom: 8px;
}
.cart-total-row.grand {
  font-size: 1.15rem; font-weight: 800;
  color: var(--charcoal);
  border-top: 1.5px solid var(--sand);
  padding-top: 12px; margin-top: 6px;
}
.checkout-btn {
  width: 100%; margin-top: 14px;
  background: var(--terracotta); color: #fff;
  font-size: 1rem; font-weight: 700;
  padding: 14px; border-radius: 10px;
  transition: background var(--transition), transform var(--transition);
}
.checkout-btn:hover { background: var(--terracotta-dark); transform: translateY(-2px); }

/* ============================================================
   CHECKOUT PAGE
============================================================ */
.checkout-page { max-width: 960px; margin: 0 auto; padding: 36px 20px 60px; }
.checkout-page h1 {
  font-family: var(--font-head);
  font-size: 2rem; font-weight: 800;
  margin-bottom: 28px; color: var(--charcoal);
}
.checkout-grid {
  display: grid;
  grid-template-columns: 1fr 380px;
  gap: 36px;
  align-items: start;
}
@media(max-width:768px){ .checkout-grid { grid-template-columns: 1fr; } }
.form-card {
  background: var(--warm-white);
  border: 1.5px solid var(--sand);
  border-radius: var(--radius); padding: 28px;
}
.form-card h2 {
  font-family: var(--font-head);
  font-size: 1.2rem; font-weight: 700;
  margin-bottom: 20px; color: var(--charcoal);
}
.form-group { margin-bottom: 16px; }
.form-group label {
  display: block; font-size: 0.82rem; font-weight: 600;
  color: var(--warm-gray); margin-bottom: 6px;
  letter-spacing: 0.03em;
}
.form-group input,
.form-group textarea {
  width: 100%;
  background: var(--cream);
  border: 1.5px solid var(--sand-dark);
  border-radius: 8px;
  padding: 11px 14px;
  font-size: 0.92rem; font-family: var(--font-body);
  color: var(--charcoal);
  transition: border-color var(--transition), box-shadow var(--transition);
  outline: none;
}
.form-group input:focus,
.form-group textarea:focus {
  border-color: var(--terracotta);
  box-shadow: 0 0 0 3px rgba(200,96,58,0.12);
}
.form-group textarea { resize: vertical; min-height: 80px; }
.submit-order {
  width: 100%;
  background: var(--terracotta); color: #fff;
  font-size: 1rem; font-weight: 700;
  padding: 15px; border-radius: 10px;
  margin-top: 8px;
  transition: background var(--transition), transform var(--transition);
  display: flex; align-items: center; justify-content: center; gap: 8px;
}
.submit-order:hover { background: var(--terracotta-dark); transform: translateY(-2px); }
.submit-order:disabled { background: var(--warm-gray); cursor: not-allowed; transform: none; }

.order-summary-card {
  background: var(--warm-white);
  border: 1.5px solid var(--sand);
  border-radius: var(--radius); padding: 24px;
  position: sticky; top: 90px;
}
.order-summary-card h2 {
  font-family: var(--font-head);
  font-size: 1.1rem; font-weight: 700;
  margin-bottom: 18px; color: var(--charcoal);
}
.summary-item {
  display: flex; align-items: center; gap: 10px;
  margin-bottom: 12px; padding-bottom: 12px;
  border-bottom: 1px solid var(--light-gray);
}
.summary-item:last-of-type { border-bottom: none; }
.summary-img {
  width: 48px; height: 48px; object-fit: cover;
  border-radius: 7px; border: 1.5px solid var(--sand); flex-shrink: 0;
}
.summary-name { font-size: 0.83rem; font-weight: 600; flex: 1; line-height: 1.3; }
.summary-price { font-size: 0.88rem; font-weight: 700; color: var(--terracotta); white-space: nowrap; }
.summary-total-row {
  display: flex; justify-content: space-between;
  font-size: 1.1rem; font-weight: 800;
  color: var(--charcoal);
  border-top: 1.5px solid var(--sand);
  padding-top: 14px; margin-top: 8px;
}

/* ============================================================
   SUCCESS TOAST
============================================================ */
.success-overlay {
  display: none; position: fixed; inset: 0; z-index: 9999;
  background: rgba(44,36,22,0.55);
  align-items: center; justify-content: center;
  backdrop-filter: blur(3px);
}
.success-overlay.show { display: flex; }
.success-box {
  background: var(--warm-white);
  border-radius: 20px; padding: 48px 40px;
  text-align: center; max-width: 400px;
  box-shadow: var(--shadow-lg);
  animation: popIn 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
}
@keyframes popIn {
  from { transform: scale(0.75); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}
.success-icon { font-size: 3.5rem; margin-bottom: 16px; }
.success-box h2 {
  font-family: var(--font-head); font-size: 1.7rem; font-weight: 800;
  color: var(--charcoal); margin-bottom: 10px;
}
.success-box p { color: var(--warm-gray); line-height: 1.6; }

/* ============================================================
   FOOTER
============================================================ */
footer {
  background: var(--charcoal);
  color: rgba(255,255,255,0.7);
  padding: 40px 20px 24px;
  text-align: center;
}
.footer-logo {
  font-family: var(--font-head);
  font-size: 1.5rem; font-weight: 900;
  color: var(--sand); margin-bottom: 8px;
}
.footer-tagline { font-size: 0.8rem; margin-bottom: 18px; }
.footer-contact { font-size: 0.82rem; margin-bottom: 16px; line-height: 1.8; }
.footer-contact a { color: var(--terracotta-light); }
.footer-copy { font-size: 0.75rem; border-top: 1px solid rgba(255,255,255,0.1); padding-top: 16px; margin-top: 16px; }

/* ============================================================
   UTILITIES
============================================================ */
.btn-primary {
  display: inline-flex; align-items: center; justify-content: center; gap: 6px;
  background: var(--terracotta); color: #fff;
  font-size: 0.9rem; font-weight: 700;
  padding: 11px 22px; border-radius: 10px;
  transition: background var(--transition), transform var(--transition);
}
.btn-primary:hover { background: var(--terracotta-dark); transform: translateY(-1px); }
.btn-outline {
  display: inline-flex; align-items: center; justify-content: center; gap: 6px;
  background: transparent; color: var(--terracotta);
  font-size: 0.9rem; font-weight: 700;
  padding: 11px 22px; border-radius: 10px;
  border: 2px solid var(--terracotta);
  transition: all var(--transition);
}
.btn-outline:hover { background: var(--terracotta); color: #fff; }
.mt8 { margin-top: 8px; }
.mt16 { margin-top: 16px; }

/* mobile responsive tweaks */
@media(max-width: 600px) {
  .cart-table th:nth-child(3),
  .cart-table td:nth-child(3) { display: none; }
  .pd-gallery { position: static; }
}
</style>
</head>
<body>

<!-- ============================================================
   NAVBAR
============================================================ -->
<nav id="navbar">
  <div class="nav-inner">
    <div class="nav-logo" onclick="navigate('home')" style="cursor:pointer;">
      Fashion<span>Zones</span>
      <span class="nav-tagline">Smart Living, Delivered</span>
    </div>
    <div class="nav-actions">
      <button class="nav-home-btn" onclick="navigate('home')">🏠 Home</button>
      <button class="nav-cart-btn" onclick="navigate('cart')">
        🛒 Cart <span class="cart-count" id="cart-count">0</span>
      </button>
    </div>
  </div>
</nav>

<!-- ============================================================
   SUCCESS OVERLAY
============================================================ -->
<div class="success-overlay" id="success-overlay">
  <div class="success-box">
    <div class="success-icon">🎉</div>
    <h2>Order Placed!</h2>
    <p>Thank you for shopping with Fashion Zones. We'll confirm your order soon. Redirecting to home…</p>
  </div>
</div>

<!-- ============================================================
   HOME PAGE
============================================================ -->
<div class="page active" id="page-home">
  <!-- Hero -->
  <section class="hero">
    <div class="hero-content">
      <div class="hero-badge">✦ New Arrivals Every Week</div>
      <h1>Smart Products for <em>Smarter Living</em></h1>
      <p>Discover innovative home & kitchen essentials, trendy gadgets, and garden tools — curated for modern households.</p>
      <button class="hero-cta" onclick="document.getElementById('products-anchor').scrollIntoView({behavior:'smooth'})">
        Shop Now →
      </button>
    </div>
  </section>

  <!-- Category Scroll Strip -->
  <section class="cat-strip-section">
    <div class="cat-strip-title">Browse by Category</div>
    <div class="cat-scroll-wrapper" id="cat-scroll">
      <div class="cat-scroll-track" id="cat-track">
        <div class="cat-icon-item" onclick="setFilter('trendy items')">
          <div class="cat-circle">
            <img src="https://i.ibb.co/sJQWtw94/61n-Mbr-ZBSVL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif" alt="Trendy Items" loading="lazy">
          </div>
          <span class="cat-label">Trendy Items</span>
        </div>
        <div class="cat-icon-item" onclick="setFilter('home & kitchen')">
          <div class="cat-circle">
            <img src="https://i.ibb.co/mZ3sL4f/51-WMz-Zq09c-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif" alt="Home & Kitchen" loading="lazy">
          </div>
          <span class="cat-label">Home &amp; Kitchen</span>
        </div>
        <div class="cat-icon-item" onclick="setFilter('home essentials')">
          <div class="cat-circle">
            <img src="https://i.ibb.co/Xk4rm2RP/61-Sl-PPPIcw-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif" alt="Home Essentials" loading="lazy">
          </div>
          <span class="cat-label">Home Essentials</span>
        </div>
        <div class="cat-icon-item" onclick="setFilter('garden tools')">
          <div class="cat-circle">
            <img src="https://i.ibb.co/6cQNnzfG/71-XPyayo-Ig-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif" alt="Garden Tools" loading="lazy">
          </div>
          <span class="cat-label">Garden Tools</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Filter + Products -->
  <section class="filter-section" id="products-anchor">
    <h2>Our Products</h2>
    <div class="filter-bar" id="filter-bar"></div>
  </section>
  <div class="product-grid" id="product-grid"></div>
</div>

<!-- ============================================================
   PRODUCT DETAIL PAGE
============================================================ -->
<div class="page" id="page-product">
  <div class="product-detail">
    <button class="back-btn" onclick="navigate('home')">← Back to Products</button>
    <div class="pd-grid">
      <!-- Gallery -->
      <div class="pd-gallery">
        <div class="main-img-wrap">
          <img src="" alt="" id="pd-main-img">
        </div>
        <div class="thumb-strip" id="pd-thumbs"></div>
      </div>
      <!-- Info -->
      <div class="pd-info">
        <div class="pd-category-tag" id="pd-cat"></div>
        <h1 class="pd-name" id="pd-name"></h1>
        <div class="pd-price-row">
          <span class="pd-price" id="pd-price"></span>
          <span class="pd-stock" id="pd-stock"></span>
        </div>
        <p class="pd-short-desc" id="pd-short-desc"></p>
        <div class="qty-row">
          <span class="qty-label">Quantity:</span>
          <div class="qty-control">
            <button class="qty-btn" onclick="changeQty(-1)">−</button>
            <span class="qty-num" id="pd-qty">1</span>
            <button class="qty-btn" onclick="changeQty(1)">+</button>
          </div>
        </div>
        <button class="add-cart-main" id="pd-add-cart" onclick="addFromDetail()">
          🛒 Add to Cart
        </button>
        <div class="pd-meta-pills">
          <span class="meta-pill">🚚 Fast Delivery</span>
          <span class="meta-pill">🔒 Secure Payment</span>
          <span class="meta-pill">✅ Quality Assured</span>
          <span class="meta-pill">↩️ Easy Returns</span>
        </div>
      </div>
    </div>
  </div>

  <!-- Accordion -->
  <div class="accordion-section">
    <div class="accordion-list" id="pd-accordion"></div>
  </div>

  <!-- Related Products -->
  <div class="related-section">
    <h2>You Might Also Like</h2>
    <div class="related-grid" id="related-grid"></div>
  </div>
</div>

<!-- ============================================================
   CART PAGE
============================================================ -->
<div class="page" id="page-cart">
  <div class="cart-page">
    <h1>🛒 Your Cart</h1>
    <div id="cart-body"></div>
  </div>
</div>

<!-- ============================================================
   CHECKOUT PAGE
============================================================ -->
<div class="page" id="page-checkout">
  <div class="checkout-page">
    <h1>Checkout</h1>
    <div class="checkout-grid">
      <div class="form-card">
        <h2>Delivery Details</h2>
        <div class="form-group">
          <label>Full Name *</label>
          <input type="text" id="f-name" placeholder="Your full name" required>
        </div>
        <div class="form-group">
          <label>Email Address *</label>
          <input type="email" id="f-email" placeholder="you@email.com" required>
        </div>
        <div class="form-group">
          <label>Phone Number *</label>
          <input type="tel" id="f-phone" placeholder="+91 XXXXX XXXXX" required>
        </div>
        <div class="form-group">
          <label>Delivery Address *</label>
          <textarea id="f-address" placeholder="Full address with pincode…"></textarea>
        </div>
        <div class="form-group">
          <label>Order Notes (optional)</label>
          <textarea id="f-notes" placeholder="Any special instructions…" style="min-height:60px"></textarea>
        </div>
        <button class="submit-order" id="submit-order-btn" onclick="submitOrder()">
          ✅ Place Order
        </button>
      </div>
      <div class="order-summary-card">
        <h2>Order Summary</h2>
        <div id="checkout-summary-items"></div>
        <div class="summary-total-row" id="checkout-grand-total"></div>
      </div>
    </div>
  </div>
</div>

<!-- ============================================================
   FOOTER
============================================================ -->
<footer>
  <div class="footer-logo">FashionZones</div>
  <div class="footer-tagline">Smart Living, Delivered</div>
  <div class="footer-contact">
    📧 <a href="mailto:shivkmr603@gmail.com">shivkmr603@gmail.com</a><br>
    📞 <a href="tel:+919546700242">+91 9546700242</a>
  </div>
  <div class="footer-copy">© 2025 Fashion Zones. All rights reserved.</div>
</footer>

<!-- ============================================================
   JAVASCRIPT
============================================================ -->
<script>
/* ============================================================
   CONFIG
============================================================ */
const CONFIG = {
  storeName: "Fashion Zones",
  tagline: "Smart Living, Delivered",
  formspree: "https://formspree.io/f/mnjwqjde",
  currency: "₹",
  cartKey: "zone_cart"
};

/* ============================================================
   PRODUCTS DATA — EDIT BELOW
============================================================ */
const PRODUCTS = [
  {
    id: "p001",
    name: "Mattress Lifter Tool (Pack of 2)",
    price: 249,
    category: "trendy items",
    images: [
      "https://i.ibb.co/sJQWtw94/61n-Mbr-ZBSVL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/CszwQrDq/71-1ap-Brv-RL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/C5mvQsQk/61-Bx-OV-o-DLL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/RkmSx9YM/71-Hkons-FPDL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/Z11k2cVm/61j-Wng2cx-UL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/tMFkbPpY/71bn-CPYae-ML-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/8g7R1P0t/71u-Lx3mwsn-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Make your bed in seconds without straining your hands or back with this smart Mattress Lifter Tool. Specially designed to lift and hold the mattress easily, it helps you tuck bedsheets, adjust bed covers, and place bedding neatly underneath without heavy effort.",
    accordion: {
      description: "Make your bed in seconds without straining your hands or back with this smart Mattress Lifter Tool. Specially designed to lift and hold the mattress easily, it helps you tuck bedsheets, adjust bed covers, and place bedding neatly underneath without heavy effort. Its ergonomic wedge shape slides smoothly under the mattress and creates enough lifting space, giving you both hands free for quick and proper sheet tucking. Made from strong yet lightweight material, this tool is durable, reusable, and easy to handle for daily use.",
      features: ["Ergonomic wedge design for easy mattress lifting","Helps tuck bedsheets quickly and neatly","Reduces hand, wrist, and back strain","Strong, lightweight, and reusable material","Suitable for all standard bed sizes","Pack of 2 for convenient use on both sides"],
      howItWorks: "Simply slide the mattress lifter under the side or corner of the mattress and push gently. The tool lifts and holds the mattress in an elevated position, creating enough space underneath to tuck bedsheets or adjust bed covers easily. Once your bedding is set, remove the tool and the mattress settles back into place.",
      whyChoose: "This mattress lifter tool makes daily bed making faster, easier, and more comfortable by removing the need to lift a heavy mattress with your hands. It saves time, prevents body strain, and gives your bed a neat and tight finish with minimal effort. Lightweight, practical, and highly useful, it is a smart home utility tool for every household."
    }
  },
  {
    id: "p002",
    name: "2 in 1 Portable Mini Bag Sealer",
    price: 269,
    category: "trendy items",
    images: [
      "https://i.ibb.co/Sww5KzGR/51-H0-Fb4-S-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/TDRxHrVL/710-I5-NM2kl-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/DHGnm5G7/71-Km-Ip-QDdv-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/PZPN830B/61a6-Ahm-Ab0-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/fV2hZ6pN/61-OMmo0-G9-SL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/4BkQcKv/81bh666c-VEL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/sB9N5hQ/61-Mmg-CTu-Yd-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Keep your snacks and groceries fresh for longer with this smart 2 in 1 Portable Mini Bag Sealer. Designed with both sealing and cutting functions, this handy device quickly reseals opened plastic packets to protect food from air, moisture, and dust.",
    accordion: {
      description: "Keep your snacks and groceries fresh for longer with this smart 2 in 1 Portable Mini Bag Sealer. Designed with both sealing and cutting functions, this handy device quickly reseals opened plastic packets to protect food from air, moisture, and dust. It uses fast heat sealing technology to create an airtight lock within seconds, helping maintain freshness and reduce food wastage. The built-in cutter allows neat and easy packet opening whenever needed. USB rechargeable and lightweight in design, it is simple to carry, easy to use, and perfect for daily kitchen storage, travel, office, or hostel use.",
      features: ["2 in 1 sealing and cutting function","USB rechargeable with charging cable support","Quick heat sealing within seconds","Keeps food fresh and moisture free","Built-in packet cutter for easy opening","Compact, lightweight, and portable design","Easy one hand operation","Suitable for most plastic snack and grocery bags"],
      howItWorks: "Charge the device using the USB cable and switch it on. Wait a few seconds for the heating plate to warm up, then place the open end of the plastic packet between the sealing jaws. Press gently and slide across the packet to create an instant airtight seal. Use the built-in cutter side whenever you need to open the packet neatly.",
      whyChoose: "This mini bag sealer is a practical everyday kitchen gadget that helps keep food fresh, saves snacks from getting soft, and reduces unnecessary wastage. It removes the need for clips, rubber bands, or folding packets and offers a quick reusable sealing solution in one compact device. Easy, rechargeable, and highly useful, it is a smart addition to every home."
    }
  },
  {
    id: "p003",
    name: "Digital Kitchen Weighing Scale",
    price: 329,
    category: "home & kitchen",
    images: [
      "https://i.ibb.co/mZ3sL4f/51-WMz-Zq09c-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/1Yj6WFMX/8167vj-X682-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/bM949SZM/71m-Vt-VAps3-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/d0c54Rbz/71a-UHwb-KDKL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/yc68jG8v/81-Lq-ALYh-7-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/3m0VFPVd/717p0-EXx-Gj-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Measure ingredients and everyday items with perfect accuracy using this smart Digital Kitchen Weighing Scale. Designed for kitchen, baking, grocery, and household use, this electronic scale provides quick and precise weight readings up to 10kg.",
    accordion: {
      description: "Measure ingredients and everyday items with perfect accuracy using this smart Digital Kitchen Weighing Scale. Designed for kitchen, baking, grocery, and household use, this electronic scale provides quick and precise weight readings up to 10kg. It comes with an easy-to-read digital display and simple control buttons for hassle free operation. Whether you are weighing fruits, vegetables, flour, spices, parcels, or daily essentials, this compact machine ensures correct measurement every time. Made from durable lightweight material, it is portable, easy to store, and highly useful for home kitchens and regular household needs.",
      features: ["High precision digital weight measurement","Supports weighing up to 10kg capacity","Easy to read LCD display screen","Quick and accurate instant results","Compact, lightweight, and portable design","Simple button control for easy use","Ideal for kitchen, grocery, and household items","Durable and long lasting body material"],
      howItWorks: "Place the scale on a flat surface and switch it on using the power button. Put the item or ingredient on the weighing platform and the digital screen will instantly show the exact weight. You can reset or tare the scale as needed for multiple measurements, making weighing simple, quick, and accurate.",
      whyChoose: "This digital weighing scale helps you measure food items and household products with better accuracy, making cooking, baking, dieting, and daily use much easier. It saves time, prevents guesswork, and gives reliable readings instantly. Compact, practical, and easy to use, it is a smart essential tool for every kitchen and home."
    }
  },
  {
    id: "p004",
    name: "5 in 1 Portable USB Air Cooler Fan",
    price: 874,
    category: "home & kitchen",
    images: [
      "https://i.ibb.co/hFMHTNCr/61x-UWj-SYQ4-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/7dcsW60D/71p-OUIn2-JHL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/RGs2hC03/71f-Moex-YOe-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/MDX4fdmj/71kpr-Kt-HMz-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/p6SV9Z5J/71-GS8-Kad-A8-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Stay cool and comfortable anywhere with this advanced 5 in 1 Portable USB Air Cooler Fan. Designed with cooling fan, mist spray, humidifier, night light, and aroma diffuser functions in one compact device, it delivers refreshing cool air.",
    accordion: {
      description: "Stay cool and comfortable anywhere with this advanced 5 in 1 Portable USB Air Cooler Fan. Designed with cooling fan, mist spray, humidifier, night light, and aroma diffuser functions in one compact device, it delivers refreshing cool air while also adding moisture to the surroundings for a more pleasant experience. The built-in water tank creates a fine mist that helps reduce dry heat, while the adjustable fan angle and multiple wind speed modes allow customized cooling as per your comfort. Its USB powered portable design makes it perfect for bedroom, office desk, study table, travel, and personal use during hot summer days.",
      features: ["5 in 1 multifunction cooling device","Fan, air cooler, mist spray, humidifier, and night light","3 adjustable wind speed modes","Built-in water tank for cool mist spray","60 degree adjustable air flow direction","Soft LED light mode for night use","USB powered and energy efficient","Compact, lightweight, and portable design"],
      howItWorks: "Fill the water tank with clean water and connect the device through USB power. Switch it on and choose your preferred fan speed. Activate the mist spray mode to release cool moisture along with airflow for enhanced cooling. You can also adjust the fan direction and use the built-in light mode for night comfort. Simply refill water whenever needed for continuous refreshing air.",
      whyChoose: "This portable air cooler fan gives you personal cooling, humidifying, and mist comfort in one compact machine, making it far more useful than a normal table fan. It is energy saving, easy to carry, and ideal for hot weather when you need instant cool air in a small space. Practical, multifunctional, and stylish, it is a smart summer essential for home, office, or study use."
    }
  },
  {
    id: "p005",
    name: "Door Bottom Guard Seal Strip (Pack of 2)",
    price: 99,
    category: "home essentials",
    images: [
      "https://i.ibb.co/Xk4rm2RP/61-Sl-PPPIcw-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/6c9dscd4/61y1sp-Mvy-EL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/s9dpL9Jm/61ob-Ri-Sq-Hc-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/CKK1289C/71-YKSA9-NEAL-AC-SL1500.jpg",
      "https://i.ibb.co/1Y2VdWQV/61-R1-UH7q-QRL-AC-SL1500.jpg"
    ],
    stock: 99,
    shortDesc: "Protect your home from dust, insects, outside noise, and unwanted air with this practical Door Bottom Guard Seal Strip. Designed to fit neatly at the bottom of doors, this smart guard fills the gap to block dust, cold air, hot air, smoke, and small insects.",
    accordion: {
      description: "Protect your home from dust, insects, outside noise, and unwanted air with this practical Door Bottom Guard Seal Strip. Designed to fit neatly at the bottom of doors, this smart guard fills the gap between the floor and the door to block dust, cold air, hot air, smoke, and small insects from entering inside. It also helps reduce outside noise and improves room insulation for a more comfortable indoor environment. Made from soft yet durable material, it slides smoothly with the door and can be installed easily without complicated tools. Perfect for bedrooms, kitchens, offices, and main doors, this useful strip helps keep your room cleaner, quieter, and energy efficient.",
      features: ["Blocks dust, insects, smoke, and outside air","Helps reduce outside noise and door gaps","Improves room insulation and energy saving","Soft, durable, and long lasting material","Smooth sliding with door movement","Easy to install and remove","Suitable for most standard doors","Pack of 2 for extra convenience"],
      howItWorks: "Simply attach or place the guard strip at the bottom side of the door so that it covers the open gap between the door and the floor. As the door moves, the strip slides along smoothly while continuously blocking dust, air, insects, and noise from passing through the gap. It creates a protective barrier without affecting normal door use.",
      whyChoose: "This door guard seal strip is an easy and affordable way to make your room cleaner, quieter, and more comfortable. It helps stop dust buildup, prevents insects from entering, reduces unwanted outside noise, and keeps indoor air better controlled. Simple to use and highly practical, it is a smart household utility for everyday protection."
    }
  },
  {
    id: "p006",
    name: "Reusable Microfiber Cleaning Cloth Roll",
    price: 280,
    category: "home essentials",
    images: [
      "https://i.ibb.co/Gv420Qzp/81-Amu-Aw-EVVL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/LjHzgG7/91oue-WXjmf-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/67Kp2K6H/81-Ub-Diiz-Xp-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/7xGPvbGG/81l-v8pt-k-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/GvbmHbVp/81ib-FHID-TL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/W4bdvzHH/81-Dg-W1-C3-Kd-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/kpPwyX5/81-RBn7-BFz5-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Make everyday cleaning faster and more effective with this premium Reusable Microfiber Cleaning Cloth Roll. Designed with soft, highly absorbent microfiber material, each cloth easily wipes away dust, water, oil, stains, and dirt without leaving scratches or lint.",
    accordion: {
      description: "Make everyday cleaning faster and more effective with this premium Reusable Microfiber Cleaning Cloth Roll. Designed with soft, highly absorbent microfiber material, each cloth easily wipes away dust, water, oil, stains, and dirt from kitchen surfaces, glass, furniture, electronics, vehicles, and household items without leaving scratches or lint. The convenient tear-away roll design allows you to pull and use one cloth at a time just like paper towels, but unlike ordinary tissues, these cloths are washable and reusable for multiple uses. Strong, durable, and quick drying, this cleaning roll is a practical solution for both home and professional cleaning tasks.",
      features: ["Soft and highly absorbent microfiber material","Easily removes dust, water, oil, and stains","Tear-away roll design for convenient single use","Washable and reusable multiple times","Lint free and scratch free cleaning","Strong, durable, and quick drying cloth","Suitable for kitchen, glass, car, furniture, and electronics","Comes with multiple reusable cleaning sheets"],
      howItWorks: "Simply tear one cloth from the roll and use it to wipe the desired surface. The microfiber material instantly absorbs liquid, traps dust, and removes dirt effectively. After use, wash the cloth with water, let it dry, and reuse it again whenever needed. Pull a fresh sheet anytime for continuous cleaning convenience.",
      whyChoose: "This microfiber cleaning cloth roll gives you the convenience of paper towels with the durability of reusable fabric, making cleaning easier, cheaper, and more efficient. It saves money on disposable wipes, provides better absorbency, and works on almost every household surface. Practical, reusable, and highly useful, it is an everyday cleaning essential for every home."
    }
  },
  {
    id: "p007",
    name: "High Flow Submersible Cooler Water Pump",
    price: 399,
    category: "garden tools",
    images: [
      "https://i.ibb.co/qM8VXJfB/71-Pwk-Pf-Hj6-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/5hc5zw6J/71-RQ1-WTg7-EL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/nqHYwyhf/6102x2-Xo-Gb-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/RkJF5F4X/61-Lhw-My-XK7-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Ensure powerful and continuous water circulation with this efficient High Flow Submersible Cooler Water Pump. Specially designed for desert coolers, aquariums, fountains, and water circulation systems, this compact electric pump delivers strong water flow.",
    accordion: {
      description: "Ensure powerful and continuous water circulation with this efficient High Flow Submersible Cooler Water Pump. Specially designed for desert coolers, aquariums, fountains, and water circulation systems, this compact electric pump delivers a strong water flow rate for better cooling performance and smooth water movement. Built with durable motor technology, it operates with low power consumption while providing reliable high speed pumping. Its fully submersible design allows easy placement inside water tanks, and the sturdy body ensures long lasting daily use. Compact, lightweight, and easy to install, this pump is an ideal replacement or upgrade for home coolers and various water flow applications.",
      features: ["High flow water pumping performance","Suitable for desert coolers, aquariums, and fountains","Energy efficient low power consumption motor","Fully submersible easy install design","Durable and long lasting body construction","Continuous smooth water circulation","Compact, lightweight, and portable size","Reliable daily use with strong output"],
      howItWorks: "Simply place the pump inside the water tank or cooler tank and connect the outlet pipe properly. Once powered on, the internal motor starts drawing water from the tank and pushes it upward through the outlet with strong pressure. This continuous circulation keeps cooler pads wet or maintains water movement wherever used, ensuring effective performance.",
      whyChoose: "This submersible water pump provides strong water flow, better cooling efficiency, and dependable daily operation without consuming much electricity. It is easy to install, compact in size, and highly practical for replacing weak or damaged cooler pumps. Durable, efficient, and multipurpose, it is a smart utility product for every home cooler setup."
    }
  },
  {
    id: "p008",
    name: "Decorative Plastic Flower Pots Set (Pack of 5)",
    price: 350,
    category: "garden tools",
    images: [
      "https://i.ibb.co/6cQNnzfG/71-XPyayo-Ig-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/BKcDvN7f/71-34-S7z-SVL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/CKHgrTGL/61-O772-D66g-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/0pX65cYp/71-Gma4mb9i-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/Ldj4tx9B/71-HSn-Iim-Qc-L-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif",
      "https://i.ibb.co/VY1mrBBg/61-CUDI269-QL-AC-AIweblab1006854-T4-FMavif-SF700-700-PQ69.avif"
    ],
    stock: 99,
    shortDesc: "Add a fresh and elegant touch to your home or garden with this beautiful Decorative Plastic Flower Pots Set. Designed with a modern ribbed finish and attractive colors, these pots are perfect for indoor plants, flowers, herbs, succulents, and decorative greenery.",
    accordion: {
      description: "Add a fresh and elegant touch to your home or garden with this beautiful Decorative Plastic Flower Pots Set. Designed with a modern ribbed finish and attractive colors, these pots are perfect for indoor plants, flowers, herbs, succulents, and decorative greenery. Made from durable lightweight plastic, they are easy to move, unbreakable, and ideal for both indoor and outdoor use. Each pot comes with proper drainage support and a matching saucer tray to help maintain healthy plant growth while keeping surfaces clean. Stylish, practical, and reusable, this planter set enhances any balcony, office desk, living room, or garden corner instantly.",
      features: ["Modern decorative ribbed pot design","Durable lightweight plastic material","Suitable for indoor and outdoor plants","Includes drainage holes for healthy roots","Comes with matching saucer trays","Easy to clean and reusable","Unbreakable and easy to move","Pack of 5 attractive planter pots"],
      howItWorks: "Simply fill each pot with soil, place your favorite plant or flower inside, and water as needed. The drainage holes at the bottom allow excess water to flow out into the saucer tray, preventing overwatering and helping roots stay healthy. Place the pots anywhere in your home, balcony, office, or garden for an instant decorative plant display.",
      whyChoose: "This flower pot set offers the perfect combination of style, durability, and plant care convenience. It not only makes your plants look more attractive but also supports healthy growth with proper drainage and clean water collection. Lightweight, reusable, and visually appealing, it is an ideal planter solution for every home and garden lover."
    }
  }
];

/* ============================================================
   CART STATE
============================================================ */
let cart = [];
let currentFilter = "all";
let currentProductId = null;
let currentQty = 1;

function loadCart() {
  try { cart = JSON.parse(localStorage.getItem(CONFIG.cartKey)) || []; } catch(e) { cart = []; }
}
function saveCart() {
  localStorage.setItem(CONFIG.cartKey, JSON.stringify(cart));
  updateCartCount();
}
function updateCartCount() {
  const total = cart.reduce((s, i) => s + i.qty, 0);
  document.getElementById('cart-count').textContent = total;
}
function getCartItem(id) { return cart.find(i => i.id === id); }
function addToCart(id, qty = 1) {
  const item = getCartItem(id);
  if (item) { item.qty += qty; } else { cart.push({ id, qty }); }
  saveCart();
}
function removeFromCart(id) {
  cart = cart.filter(i => i.id !== id);
  saveCart();
}
function updateCartQty(id, qty) {
  const item = getCartItem(id);
  if (item) { item.qty = Math.max(1, qty); saveCart(); }
}

/* ============================================================
   ROUTING
============================================================ */
function navigate(page, productId) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById('page-' + page).classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
  if (page === 'product' && productId) renderProductDetail(productId);
  if (page === 'cart') renderCart();
  if (page === 'checkout') renderCheckout();
}

/* ============================================================
   HOME PAGE
============================================================ */
function getCategories() {
  const cats = new Set();
  PRODUCTS.forEach(p => p.category.split(',').forEach(c => cats.add(c.trim().toLowerCase())));
  return ['all', ...Array.from(cats)];
}

function setFilter(cat) {
  currentFilter = cat.toLowerCase();
  document.querySelectorAll('.filter-btn').forEach(b => {
    b.classList.toggle('active', b.dataset.cat === currentFilter);
  });
  renderProductGrid();
  // scroll to products
  document.getElementById('products-anchor').scrollIntoView({ behavior: 'smooth' });
}

function renderFilterBar() {
  const bar = document.getElementById('filter-bar');
  bar.innerHTML = '';
  getCategories().forEach(cat => {
    const btn = document.createElement('button');
    btn.className = 'filter-btn' + (cat === currentFilter ? ' active' : '');
    btn.dataset.cat = cat;
    btn.textContent = cat === 'all' ? 'All Products' : cat.replace(/\b\w/g, l => l.toUpperCase());
    btn.onclick = () => setFilter(cat);
    bar.appendChild(btn);
  });
}

function renderProductGrid() {
  const grid = document.getElementById('product-grid');
  const filtered = currentFilter === 'all'
    ? PRODUCTS
    : PRODUCTS.filter(p => p.category.toLowerCase().includes(currentFilter));
  grid.innerHTML = '';
  filtered.forEach(p => grid.appendChild(createProductCard(p)));
}

function createProductCard(p) {
  const inCart = !!getCartItem(p.id);
  const div = document.createElement('div');
  div.className = 'product-card';
  div.innerHTML = `
    <div class="card-img-wrap" onclick="navigate('product','${p.id}')">
      <img src="${p.images[0]}" alt="${p.name}" loading="lazy">
      <span class="card-category-badge">${p.category.split(',')[0].trim()}</span>
    </div>
    <div class="card-body">
      <div class="card-name" onclick="navigate('product','${p.id}')">${p.name}</div>
      <div class="card-price">${CONFIG.currency}${p.price.toLocaleString('en-IN')}</div>
      <div class="card-actions">
        <button class="btn-view" onclick="navigate('product','${p.id}')">View Details</button>
        <button class="btn-cart ${inCart ? 'in-cart' : ''}" id="card-cart-${p.id}" onclick="event.stopPropagation(); cardAddToCart('${p.id}')">
          ${inCart ? 'In Cart ✓' : 'Add to Cart'}
        </button>
      </div>
    </div>`;
  return div;
}

function cardAddToCart(id) {
  addToCart(id, 1);
  const btn = document.getElementById('card-cart-' + id);
  if (btn) { btn.textContent = 'In Cart ✓'; btn.classList.add('in-cart'); }
}

/* ============================================================
   PRODUCT DETAIL
============================================================ */
function renderProductDetail(id) {
  currentProductId = id;
  currentQty = 1;
  const p = PRODUCTS.find(x => x.id === id);
  if (!p) return;

  document.getElementById('pd-main-img').src = p.images[0];
  document.getElementById('pd-main-img').alt = p.name;
  document.getElementById('pd-cat').textContent = p.category.split(',')[0].trim().replace(/\b\w/g, l => l.toUpperCase());
  document.getElementById('pd-name').textContent = p.name;
  document.getElementById('pd-price').textContent = CONFIG.currency + p.price.toLocaleString('en-IN');
  document.getElementById('pd-stock').textContent = p.stock > 0 ? `✓ In Stock (${p.stock})` : 'Out of Stock';
  document.getElementById('pd-short-desc').textContent = p.shortDesc;
  document.getElementById('pd-qty').textContent = 1;

  // Cart button state
  updateDetailCartBtn();

  // Thumbnails
  const thumbs = document.getElementById('pd-thumbs');
  thumbs.innerHTML = '';
  p.images.forEach((img, i) => {
    const t = document.createElement('div');
    t.className = 'thumb' + (i === 0 ? ' active' : '');
    t.innerHTML = `<img src="${img}" alt="${p.name} ${i+1}" loading="lazy">`;
    t.onclick = () => {
      document.getElementById('pd-main-img').src = img;
      thumbs.querySelectorAll('.thumb').forEach(x => x.classList.remove('active'));
      t.classList.add('active');
    };
    thumbs.appendChild(t);
  });

  // Accordion
  renderAccordion(p);

  // Related
  renderRelated(p);
}

function updateDetailCartBtn() {
  const btn = document.getElementById('pd-add-cart');
  const inCart = !!getCartItem(currentProductId);
  if (inCart) {
    btn.textContent = '✓ In Cart'; btn.classList.add('in-cart');
  } else {
    btn.innerHTML = '🛒 Add to Cart'; btn.classList.remove('in-cart');
  }
}

function changeQty(delta) {
  currentQty = Math.max(1, currentQty + delta);
  document.getElementById('pd-qty').textContent = currentQty;
}

function addFromDetail() {
  addToCart(currentProductId, currentQty);
  updateDetailCartBtn();
  currentQty = 1;
  document.getElementById('pd-qty').textContent = 1;
  // refresh card button if visible
  const cardBtn = document.getElementById('card-cart-' + currentProductId);
  if (cardBtn) { cardBtn.textContent = 'In Cart ✓'; cardBtn.classList.add('in-cart'); }
}

function renderAccordion(p) {
  const a = p.accordion;
  const list = document.getElementById('pd-accordion');
  list.innerHTML = '';
  const sections = [
    { key: 'description', icon: '📋', label: 'Description', content: a.description, type: 'text' },
    { key: 'features',    icon: '✨', label: 'Features',    content: a.features,    type: 'list' },
    { key: 'howItWorks',  icon: '⚙️', label: 'How It Works', content: a.howItWorks, type: 'text' },
    { key: 'whyChoose',   icon: '💡', label: 'Why Choose This Product', content: a.whyChoose, type: 'text' },
  ];
  sections.forEach((s, idx) => {
    const item = document.createElement('div');
    item.className = 'accordion-item';
    let bodyHTML = '';
    if (s.type === 'list') {
      bodyHTML = '<ul>' + s.content.map(f => `<li>${f}</li>`).join('') + '</ul>';
    } else {
      bodyHTML = `<p>${s.content}</p>`;
    }
    item.innerHTML = `
      <button class="accordion-header" onclick="toggleAccordion(this.parentElement)">
        <span class="accordion-header-text">
          <span class="accordion-icon-label">${s.icon}</span>
          ${s.label}
        </span>
        <span class="accordion-toggle">+</span>
      </button>
      <div class="accordion-body">
        <div class="accordion-body-inner">${bodyHTML}</div>
      </div>`;
    list.appendChild(item);
  });
}

function toggleAccordion(item) {
  const isOpen = item.classList.contains('open');
  // close all
  document.querySelectorAll('.accordion-item.open').forEach(i => i.classList.remove('open'));
  if (!isOpen) item.classList.add('open');
}

function renderRelated(p) {
  const related = PRODUCTS.filter(x => x.id !== p.id && x.category.split(',').some(c => p.category.split(',').map(s=>s.trim().toLowerCase()).includes(c.trim().toLowerCase()))).slice(0, 4);
  const grid = document.getElementById('related-grid');
  grid.innerHTML = '';
  related.forEach(r => grid.appendChild(createProductCard(r)));
  if (!related.length) grid.innerHTML = '<p style="color:var(--warm-gray);font-size:0.9rem;">No related products found.</p>';
}

/* ============================================================
   CART PAGE
============================================================ */
function renderCart() {
  const body = document.getElementById('cart-body');
  if (!cart.length) {
    body.innerHTML = `
      <div class="cart-empty">
        <svg width="80" height="80" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="40" cy="40" r="40" fill="#f0ebe3"/>
          <text x="50%" y="54%" text-anchor="middle" dominant-baseline="middle" font-size="36">🛒</text>
        </svg>
        <p>Your cart is empty.</p>
        <button class="btn-primary" onclick="navigate('home')">Start Shopping</button>
      </div>`;
    return;
  }

  const subtotal = cart.reduce((s, i) => {
    const p = PRODUCTS.find(x => x.id === i.id);
    return s + (p ? p.price * i.qty : 0);
  }, 0);

  let rows = cart.map(i => {
    const p = PRODUCTS.find(x => x.id === i.id);
    if (!p) return '';
    return `<tr>
      <td><img class="cart-item-img" src="${p.images[0]}" alt="${p.name}"></td>
      <td><div class="cart-item-name">${p.name}</div></td>
      <td class="cart-item-price">${CONFIG.currency}${p.price.toLocaleString('en-IN')}</td>
      <td>
        <div class="cart-qty-ctrl">
          <button class="cqb" onclick="cartChangeQty('${p.id}',-1)">−</button>
          <span class="cart-qty-num">${i.qty}</span>
          <button class="cqb" onclick="cartChangeQty('${p.id}',1)">+</button>
        </div>
      </td>
      <td class="cart-item-price">${CONFIG.currency}${(p.price * i.qty).toLocaleString('en-IN')}</td>
      <td><button class="cart-remove" onclick="cartRemove('${p.id}')">🗑</button></td>
    </tr>`;
  }).join('');

  body.innerHTML = `
    <table class="cart-table">
      <thead><tr>
        <th></th><th>Product</th><th>Price</th><th>Qty</th><th>Total</th><th></th>
      </tr></thead>
      <tbody>${rows}</tbody>
    </table>
    <div class="cart-total-box">
      <div class="cart-total-row"><span>Subtotal</span><span>${CONFIG.currency}${subtotal.toLocaleString('en-IN')}</span></div>
      <div class="cart-total-row"><span>Delivery</span><span style="color:var(--success)">FREE</span></div>
      <div class="cart-total-row grand"><span>Grand Total</span><span>${CONFIG.currency}${subtotal.toLocaleString('en-IN')}</span></div>
      <button class="checkout-btn" onclick="navigate('checkout')">Proceed to Checkout →</button>
    </div>`;
}

function cartChangeQty(id, delta) {
  const item = getCartItem(id);
  if (!item) return;
  if (item.qty + delta < 1) { cartRemove(id); return; }
  updateCartQty(id, item.qty + delta);
  renderCart();
}

function cartRemove(id) {
  removeFromCart(id);
  renderCart();
  // refresh card btn
  const btn = document.getElementById('card-cart-' + id);
  if (btn) { btn.textContent = 'Add to Cart'; btn.classList.remove('in-cart'); }
}

/* ============================================================
   CHECKOUT PAGE
============================================================ */
function renderCheckout() {
  const itemsDiv = document.getElementById('checkout-summary-items');
  const grandDiv = document.getElementById('checkout-grand-total');
  let total = 0;
  itemsDiv.innerHTML = '';
  cart.forEach(i => {
    const p = PRODUCTS.find(x => x.id === i.id);
    if (!p) return;
    const itemTotal = p.price * i.qty;
    total += itemTotal;
    itemsDiv.innerHTML += `
      <div class="summary-item">
        <img class="summary-img" src="${p.images[0]}" alt="${p.name}">
        <span class="summary-name">${p.name} ×${i.qty}</span>
        <span class="summary-price">${CONFIG.currency}${itemTotal.toLocaleString('en-IN')}</span>
      </div>`;
  });
  grandDiv.innerHTML = `<span>Total</span><span>${CONFIG.currency}${total.toLocaleString('en-IN')}</span>`;
}

async function submitOrder() {
  const name = document.getElementById('f-name').value.trim();
  const email = document.getElementById('f-email').value.trim();
  const phone = document.getElementById('f-phone').value.trim();
  const address = document.getElementById('f-address').value.trim();
  const notes = document.getElementById('f-notes').value.trim();

  if (!name || !email || !phone || !address) {
    alert('Please fill in all required fields.'); return;
  }

  const btn = document.getElementById('submit-order-btn');
  btn.disabled = true;
  btn.textContent = 'Placing Order…';

  const orderItems = cart.map(i => {
    const p = PRODUCTS.find(x => x.id === i.id);
    return `${p ? p.name : i.id} × ${i.qty} = ${CONFIG.currency}${p ? (p.price * i.qty).toLocaleString('en-IN') : '?'}`;
  }).join('\n');

  const total = cart.reduce((s, i) => {
    const p = PRODUCTS.find(x => x.id === i.id);
    return s + (p ? p.price * i.qty : 0);
  }, 0);

  const message = `New Order from Fashion Zones\n\nName: ${name}\nEmail: ${email}\nPhone: ${phone}\nAddress: ${address}\nNotes: ${notes || 'None'}\n\n--- ORDER ITEMS ---\n${orderItems}\n\nGrand Total: ${CONFIG.currency}${total.toLocaleString('en-IN')}`;

  try {
    const res = await fetch(CONFIG.formspree, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json', 'Accept': 'application/json' },
      body: JSON.stringify({ name, email, phone, address, notes, message })
    });
    if (res.ok) {
      cart = []; saveCart();
      document.getElementById('success-overlay').classList.add('show');
      setTimeout(() => {
        document.getElementById('success-overlay').classList.remove('show');
        navigate('home');
      }, 3000);
    } else {
      alert('Something went wrong. Please try again.');
      btn.disabled = false; btn.textContent = '✅ Place Order';
    }
  } catch(e) {
    alert('Network error. Please check your connection.');
    btn.disabled = false; btn.textContent = '✅ Place Order';
  }
}

/* ============================================================
   CATEGORY STRIP DRAG SCROLL
============================================================ */
function initCatScroll() {
  const el = document.getElementById('cat-scroll');
  let isDown = false, startX, scrollLeft;
  el.addEventListener('mousedown', e => {
    isDown = true; el.classList.add('active');
    startX = e.pageX - el.offsetLeft;
    scrollLeft = el.scrollLeft;
  });
  el.addEventListener('mouseleave', () => { isDown = false; });
  el.addEventListener('mouseup', () => { isDown = false; });
  el.addEventListener('mousemove', e => {
    if (!isDown) return;
    e.preventDefault();
    const x = e.pageX - el.offsetLeft;
    el.scrollLeft = scrollLeft - (x - startX) * 1.4;
  });
}

/* ============================================================
   INIT
============================================================ */
loadCart();
updateCartCount();
renderFilterBar();
renderProductGrid();
initCatScroll();
</script>
</body>
</html>
