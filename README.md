# 📄 Instructions to Use the Tab UI Snippet in Shopify
**Create the Snippet**

Go to your Shopify admin: Online Store > Themes > Edit Code

Under the Snippets folder, click “Add a new snippet” and name it:
```liquid
tab-ui
```

Paste your full Tab UI code into this file and save.

Add Metafields for Products

Go to: Settings > Custom Data > Products

**Add the following metafields with type multi-line text:**

ingredients

benifits

allergens

These will be used to show content inside the tabs.

Render the Snippet on the Product Page

Open: sections/main-product.liquid

Find where you want the tab section to appear (usually below product description).

Add this code:
```liquid
{% render 'tab-ui' %}
```

You can also add the below code in schema block, if you want to show and hide via theme editor
```liquid
{
  "type": "tab_ui",
  "name": "Tab UI",
  "settings": [
    {
      "type": "textarea",
      "id": "description",
      "label": "Description"
    },
    {
      "type": "textarea",
      "id": "ingredients",
      "label": "Ingredients"
    },
    {
      "type": "textarea",
      "id": "benifits",
      "label": "Benifits"
    }
  ]
}
```
