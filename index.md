---
layout: default
title: "首頁"
description: "亞之騰有限公司 - 消防局宣導商品設計製造，專業防身警報器製造商"
---

<section class="hero">
  <div class="hero-content">
    <div class="hero-text">
      <h1>{{ site.data.company.name }}</h1>
      <p class="lead">{{ site.data.company.description }}</p>
      <p class="highlight">消防局宣導商品設計製造</p>
      
      <div class="hero-buttons">
        {% for button in site.data.navigation.buttons %}
        <a href="{{ button.url | relative_url }}" class="btn {{ button.class }}">
          {{ button.title }}
        </a>
        {% endfor %}
      </div>
    </div>
    
    <div class="hero-image">
      <img src="{{ '/assets/images/hero-banner.jpg' | relative_url }}" 
           alt="防身警報器產品展示" 
           loading="lazy">
    </div>
  </div>
</section>

<section class="featured-products">
  <div class="container">
    <h2>熱門商品</h2>
    <div class="products-grid">
      {% for product in site.data.products.featured_products %}
      <div class="product-card">
        <img src="{{ product.image | relative_url }}" 
             alt="{{ product.name }}" 
             loading="lazy">
        <div class="product-info">
          <h3>{{ product.name }}</h3>
          <p class="price">NT$ {{ product.price }}</p>
          <ul class="features">
            {% for feature in product.features %}
            <li>{{ feature }}</li>
            {% endfor %}
          </ul>
          <p class="description">{{ product.description }}</p>
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>