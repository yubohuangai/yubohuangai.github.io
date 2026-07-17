---
layout: default
title: "A Menu, Visualized"
---

<style>
.menu-body { padding: 0 2.5%; }
.menu-body h2 { margin-top: 0.6rem; }
.menu-meta { font-size: 0.92rem; margin: 0.3rem 0 1.1rem; }
.menu-body p { line-height: 1.6; }
.menu-hero { width: 100%; height: 240px; object-fit: cover; border-radius: 6px; display: block; margin: 1.3rem 0 0.4rem; }
.menu-hero-cap { font-size: 0.82rem; margin: 0.35rem 0 1.4rem; }
.menu-note { font-size: 0.9rem; border-left: 2px solid #1772d0; padding: 0.5rem 0 0.5rem 0.9rem; margin: 1.2rem 0; }

.course { font-size: 15px; font-weight: 700; letter-spacing: 0.14em; text-transform: uppercase;
  border-bottom: 1px solid #e2e2e2; padding-bottom: 0.35rem; margin: 2.1rem 0 1.1rem; }

.menu-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(210px, 1fr)); gap: 1.4rem 1.3rem; }
.dish { margin: 0; display: flex; flex-direction: column; }
.dish-img { aspect-ratio: 4 / 3; overflow: hidden; border: 1px solid #e2e2e2; border-radius: 5px; background: #fafafa; }
.dish-img img { width: 100%; height: 100%; object-fit: cover; display: block; }
.dish-img--none { display: flex; align-items: center; justify-content: center;
  background: repeating-linear-gradient(45deg, #f4f4f4 0 9px, #fbfbfb 9px 18px); }
.dish-img--none span { font-size: 0.72rem; letter-spacing: 0.05em; text-align: center;
  padding: 0 0.6rem; border: 1px solid #cfcfcf; border-radius: 14px; padding: 4px 10px; background: #fff; }
.dish figcaption { margin-top: 0.5rem; display: flex; flex-direction: column; gap: 0.15rem; }
.dish-head { display: flex; align-items: baseline; gap: 0.5rem; }
.dish-name { font-weight: 700; font-size: 0.98rem; line-height: 1.25; flex: 1 1 auto; }
.dish-price { font-size: 0.9rem; white-space: nowrap; font-variant-numeric: tabular-nums; }
.dish-en { font-style: italic; font-size: 0.86rem; }
.dish-desc { font-size: 0.83rem; line-height: 1.45; }

@media screen and (max-width: 480px) {
  .menu-grid { grid-template-columns: 1fr 1fr; gap: 1rem 0.8rem; }
  .dish-name { font-size: 0.9rem; }
  .dish-desc { font-size: 0.78rem; }
  .menu-hero { height: 180px; }
}
</style>

<div class="menu-body">

<h2>A Menu, Visualized</h2>
<p class="menu-meta">July 2026 &middot; a weekend build</p>

<p><strong>A weekend build.</strong> Dinner was at a French bistro, and the menu
was a wall of French I couldn't parse — so I pointed a coding agent at it and
asked for a gallery: fetch a representative photo of every dish, translate each
name, lay it out. The interesting part turned out to be <em>verification</em>. The
agent had to <em>look</em> at every image it pulled and discard the wrong ones — it
caught a live snail standing in for escargots, a soccer stadium for panisse, and
a tub of American pimento cheese posing as a French cheese board. Twenty-five of
twenty-six dishes came back with a real, verified photo. This is that gallery.</p>

<img class="menu-hero" src="/assets/img/menu-visualized/hero.jpg" alt="A bistro table" />
<p class="menu-hero-cap">The ambient shot — the one photo taken in an actual dining room. The dish images below are representative examples.</p>

<p class="menu-note">Dish photos are <strong>representative examples</strong> from Wikimedia
Commons and Wikipedia, not the restaurant's own plating — a boeuf bourguignon looks
like a boeuf bourguignon. Panisse is marked: no clean photo survived the verification pass.</p>

  <h3 class="course">Entrées</h3>
  <div class="menu-grid">
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/01.jpg" alt="Huîtres" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Huîtres</span><span class="dish-price">30 / 55</span></span>
        <span class="dish-en">Oysters</span>
        <span class="dish-desc">Feature oysters, sherry mignonette, lemon. Half dozen / dozen.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/02.jpg" alt="Salade d&#x27;Endives" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Salade d&#x27;Endives</span><span class="dish-price">20</span></span>
        <span class="dish-en">Endive Salad</span>
        <span class="dish-desc">Endives, red-wine poached pears, roquefort, walnuts, orange vinaigrette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/03.jpg" alt="Plateau de Fromages" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Plateau de Fromages</span><span class="dish-price">28</span></span>
        <span class="dish-en">Cheese Platter</span>
        <span class="dish-desc">Assorted French cheese, berry compote, baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/04.jpg" alt="Escargots à la Persillade" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Escargots à la Persillade</span><span class="dish-price">16</span></span>
        <span class="dish-en">Snails in Garlic-Parsley Butter</span>
        <span class="dish-desc">Snails, parsley butter, house-baked baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/05.jpg" alt="Frites" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Frites</span><span class="dish-price">14</span></span>
        <span class="dish-en">Fries</span>
        <span class="dish-desc">Cooked in duck fat, herbs, house-made mayo.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/06.jpg" alt="Soupe à l&#x27;Oignon" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Soupe à l&#x27;Oignon</span><span class="dish-price">18</span></span>
        <span class="dish-en">French Onion Soup</span>
        <span class="dish-desc">Caramelized onion, croûtons, gruyère.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/07.jpg" alt="Coquilles St. Jacques" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Coquilles St. Jacques</span><span class="dish-price">28</span></span>
        <span class="dish-en">Scallops Gratin</span>
        <span class="dish-desc">Scallops, butter, white wine, gruyère, crispy potatoes.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/08.jpg" alt="Foie Gras Torchon" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Foie Gras Torchon</span><span class="dish-price">30</span></span>
        <span class="dish-en">Truffled Foie Gras</span>
        <span class="dish-desc">Truffle, sour cherry confiture, served on brioche.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/09.jpg" alt="Charcuterie" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Charcuterie</span><span class="dish-price">25</span></span>
        <span class="dish-en">Cured Meats</span>
        <span class="dish-desc">French imported cured meat, condiments, baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/10.jpg" alt="Os à Moelle Rôti" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Os à Moelle Rôti</span><span class="dish-price">21</span></span>
        <span class="dish-en">Roasted Bone Marrow</span>
        <span class="dish-desc">Grilled baguette. Add cognac 12.</span>
      </figcaption>
    </figure>
  </div>

  <h3 class="course">Plats</h3>
  <div class="menu-grid">
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/11.jpg" alt="Steak Tartare" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Steak Tartare</span><span class="dish-price">35</span></span>
        <span class="dish-en">Steak Tartare — raw beef</span>
        <span class="dish-desc">Hand-chopped AAA beef, horseradish vinaigrette, crispy shallots, pickled mustard seeds, pickles, grilled baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/12.jpg" alt="Poulet Forestière" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Poulet Forestière</span><span class="dish-price">34</span></span>
        <span class="dish-en">Forest-Style Chicken</span>
        <span class="dish-desc">Duchess potato, wild mushroom cream sauce.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/13.jpg" alt="Steak-Frites au Poivre" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Steak-Frites au Poivre</span><span class="dish-price">65</span></span>
        <span class="dish-en">Peppercorn Steak &amp; Fries</span>
        <span class="dish-desc">6oz filet mignon, red peppercorn, mushrooms, shallot &amp; cognac cream jus.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/14.jpg" alt="Bouillabaisse" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Bouillabaisse</span><span class="dish-price">36</span></span>
        <span class="dish-en">Provençal Seafood Stew</span>
        <span class="dish-desc">Shrimp, cod, mussels, scallops, potatoes, cherry tomatoes, saffron broth, baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/15.jpg" alt="Gnocchi à la Parisienne" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Gnocchi à la Parisienne</span><span class="dish-price">30</span></span>
        <span class="dish-en">Parisian Gnocchi</span>
        <span class="dish-desc">House-made gnocchi, truffled ham, mornay sauce, apple, comté &amp; gruyère.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/16.jpg" alt="Option Végétarienne" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Option Végétarienne</span><span class="dish-price">MP</span></span>
        <span class="dish-en">Vegetarian Option</span>
        <span class="dish-desc">Roasted butternut squash, mushrooms, walnut, crispy sage, comté.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/17.jpg" alt="Magret de Canard" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Magret de Canard</span><span class="dish-price">42</span></span>
        <span class="dish-en">Seared Duck Breast</span>
        <span class="dish-desc">7oz. Confit parsnips, fried Brussels sprouts, beetroot, port purée, plum demi.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/18.jpg" alt="Moules Marinières" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Moules Marinières</span><span class="dish-price">35</span></span>
        <span class="dish-en">Sailor-Style Mussels</span>
        <span class="dish-desc">Garlic cream, white wine, lemon, baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img dish-img--none"><span>photo did not survive verification</span></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Panisse</span><span class="dish-price">27</span></span>
        <span class="dish-en">Provençal Chickpea Cake</span>
        <span class="dish-desc">Vadouvan, tomato sauce, ratatouille compote, coriander-pickled onion, lovage oil.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/20.jpg" alt="Boeuf Bourguignon" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Boeuf Bourguignon</span><span class="dish-price">35</span></span>
        <span class="dish-en">Burgundy Beef Stew</span>
        <span class="dish-desc">Beef, bacon, onion, mushrooms, carrots, tomatoes, potatoes, bouquet garni, Pinot Noir, baguette.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/21.jpg" alt="Bastille Burger" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Bastille Burger</span><span class="dish-price">32</span></span>
        <span class="dish-en">Bastille Burger</span>
        <span class="dish-desc">Thick-cut bacon, brie, truffle mayo, house-made brioche.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/22.jpg" alt="Sole Meunière" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Sole Meunière</span><span class="dish-price">36</span></span>
        <span class="dish-en">Sole in Brown Butter</span>
        <span class="dish-desc">Pan-seared, potato gratin, crispy artichokes, zucchini, creamy caper jus.</span>
      </figcaption>
    </figure>
  </div>

  <h3 class="course">Desserts</h3>
  <div class="menu-grid">
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/23.jpg" alt="Crème Brûlée" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Crème Brûlée</span><span class="dish-price">15</span></span>
        <span class="dish-en">Burnt Cream Custard</span>
        <span class="dish-desc">Madagascar vanilla beans, tuiles.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/24.jpg" alt="Tarte au Citron" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Tarte au Citron</span><span class="dish-price">13</span></span>
        <span class="dish-en">Lemon Tart</span>
        <span class="dish-desc">Mascarpone chantilly, tuiles.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/25.jpg" alt="Profiteroles" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Profiteroles</span><span class="dish-price">15</span></span>
        <span class="dish-en">Cream Puffs</span>
        <span class="dish-desc">French vanilla, choux pastry, Bernard chocolate sauce.</span>
      </figcaption>
    </figure>
    <figure class="dish">
      <div class="dish-img"><img src="/assets/img/menu-visualized/26.jpg" alt="Sorbet de Saison" /></div>
      <figcaption>
        <span class="dish-head"><span class="dish-name">Sorbet de Saison</span><span class="dish-price">12</span></span>
        <span class="dish-en">Seasonal Sorbet</span>
        <span class="dish-desc">Rotating seasonal flavor.</span>
      </figcaption>
    </figure>
  </div>

</div>
