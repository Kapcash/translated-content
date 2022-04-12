---
title: itemscope
slug: Web/HTML/Global_attributes/itemscope
tags:
  - Attribut
  - Attribut universel
  - HTML
  - Micro-données
  - Microdata
  - Reference
translation_of: Web/HTML/Global_attributes/itemscope
original_slug: Web/HTML/Attributs_universels/itemscope
---
{{HTMLSidebar("Global_attributes")}}

L'[attribut universel](/fr/docs/Web/HTML/Attributs_universels) **`itemscope`** fonctionne généralement avec l'attribut `itemtype` afin d'indiquer qu'un bloc HTML contient un objet donné. `itemscope` crée l'objet et définit la portée de l'`itemtype` associé. Il est possible d'associer un attribut `itemscope` à n'importe quel élément HTML.

### Les identifiants rattachés à `itemscope`

Un élément qui possède un attribut `itemscope` permet de définir un nouvel élément qui sera un groupe de paires de noms/valeurs. Les éléments qui ont un attribut `itemscope` et un attribut `itemtype` peuvent également définir un attribut `id` (à ne pas confondre avec `itemid)` pour identifier de façon unique l'élément sur le Web.

## Syntaxe

### Syntaxe formelle

    itemscope

## Exemple

Dans cet exemple, on a trois attributs `itemscopes`. Ces trois `itemscopes` définissent les portées respectives des `itemtypes` correspondants qui sont : _Recipe_ (Recette), _AggregateRating_ (Notes) et _NutritionInformation_ (Informations nutritionnelles).

### HTML

```html
<div itemscope itemtype="http://schema.org/Recipe">
  <h2 itemprop="name">La tarte aux pommes de grand-mère pour les fêtes</h2>
  <img itemprop="image" src="https://c1.staticflickr.com/1/30/42759561_8631e2f905_n.jpg" width="50" height="50" />
  <p>
    Par <span itemprop="author" itemscope itemtype="http://schema.org/Person">
      <span itemprop="name">Carole Dupont</span>
    </span>
  </p>
  <p>
    Publié le : <time datetime="2009-11-05" itemprop="datePublished">5 Novembre 2009</time>
  </p>
  <span itemprop="description">C'est la recette de la tarte aux pommes de ma grand-mère. J'aime ajouter une pincée de noix de muscade.</span>
  <br>
  <span itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    <span itemprop="ratingValue">4.0</span> étoiles, basé sur <span itemprop="reviewCount">35</span> avis
  </span>
  <br>
  Temps de préparation: <time datetime="PT30M" itemprop="prepTime">30min</time><br>
  Temps de cuisson: <time datetime="PT1H" itemprop="cookTime">1h</time>r<br>
  Temps total: <time datetime="PT1H30M" itemprop="totalTime">1h30min</time><br>
  Yield: <span itemprop="recipeYield">1 tarte de 22cm (8 parts)</span><br>
  <span itemprop="nutrition" itemscope itemtype="http://schema.org/NutritionInformation">
    Taille de la portion : <span itemprop="servingSize">1 part moyenne</span><br>
    Calories par portion: <span itemprop="calories">250cal</span><br>
    Matières grasses par portion: <span itemprop="fatContent">12g</span><br>
  </span>
  <p>
    Ingrédients:<br>
    <span itemprop="recipeIngredient">Pommes coupées en fines tranches : environ 500g<br></span>
    <span itemprop="recipeIngredient">Sucre blanc : 3 cuillères à café<br></span>
    ...
  </p>
  Étapes: <br>
  <div itemprop="recipeInstructions">
    1. Couper et éplucher les pommes<br>
    2. Mélanger le sucre et la cannelle. Rajouter du sucre pour les pommes acidulées. <br>
    ...
  </div>
</div>
```

### Structure des données

<table class="standard-table">
  <tbody>
    <tr>
      <td colspan="1" rowspan="14">itemscope</td>
      <td>itemtype</td>
      <td colspan="2" rowspan="1">Recipe</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>name:</td>
      <td>La tarte aux pommes de grand-mère</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>image:</td>
      <td>https://c1.staticflickr.com/1/30/42759561_8631e2f905_n.jpg</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>datePublished:</td>
      <td>2009-11-05</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>description:</td>
      <td>
        C'est la recette de la tarte aux pommes de ma grand-mère. J'aime ajouter une pincée de noix de muscade.
      </td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>prepTime:</td>
      <td>PT30M</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>cookTime:</td>
      <td>PT1H</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>totalTime:</td>
      <td>PT1H30M</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>recipeYield:</td>
      <td>1 tarte de 22cm (8 parts)</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>recipeIngredient:</td>
      <td>Pommes coupées en fines tranches : environ 500g</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>recipeIngredient:</td>
      <td>Sucre blanc: 6 cuillères à soupe</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>recipeInstructions:</td>
      <td>
        1. Couper et éplucher les pommes 2. Mélanger le sucre et la cannelle. Rajouter du sucre pour les pommes acidulées.
      </td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td colspan="2" rowspan="1">author [Person]:</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>name:</td>
      <td>Carole Dupont</td>
    </tr>
    <tr>
      <td colspan="1" rowspan="3">itemscope</td>
      <td>itemprop[itemtype]</td>
      <td colspan="2" rowspan="1">aggregateRating [AggregateRating]:</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>ratingValue:</td>
      <td>4.0</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>reviewCount:</td>
      <td>35</td>
    </tr>
    <tr>
      <td colspan="1" rowspan="4">itemscope</td>
      <td>itemprop[itemtype]</td>
      <td colspan="2" rowspan="1">nutrition [NutritionInformation]:</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>servingSize:</td>
      <td>1 part moyenne</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>calories:</td>
      <td>250cal</td>
    </tr>
    <tr>
      <td>itemprop</td>
      <td>fatContent:</td>
      <td>12g</td>
    </tr>
  </tbody>
</table>

> **Note :** Pour extraire des micro-données d'un document HTML, vous pouvez utiliser [l'outil d'extraction de Google pour les micro-données.](https://developers.google.com/structured-data/testing-tool/) Vous pouvez par exemple utiliser le document HTML précédent.

## Spécifications

| Spécification                                                                                    | État                                 | Commentaires |
| ------------------------------------------------------------------------------------------------ | ------------------------------------ | ------------ |
| {{SpecName('HTML Microdata', "#dfn-itemscope", "itemscope")}}                 | {{Spec2('HTML Microdata')}} |              |
| {{SpecName('HTML WHATWG', "microdata.html#attr-itemscope", "itemscope")}} | {{Spec2('HTML WHATWG')}}     |              |

## Compatibilité des navigateurs

{{Compat("html.global_attributes.itemscope")}}

## Voir aussi

- [Les différents attributs universels](/fr/docs/Web/HTML/Attributs_universels)
- Les autres attributs universels relatifs aux microdonnées :

  - {{htmlattrxref("itemid")}}
  - {{htmlattrxref("itemprop")}}
  - {{htmlattrxref("itemref")}}
  - {{htmlattrxref("itemscope")}}
  - {{htmlattrxref("itemtype")}}
