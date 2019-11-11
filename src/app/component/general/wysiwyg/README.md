# Wysiwyg Component

The Wysiwyg component can be used for blocks of copy that is added by the author through a wysiwyg editor.
This component supports a collection of presets that can be used to scaffold out content.
This might be important because this content usually contains HTML elements without classes.
This means that with the stylesheet included default styles might be needed to be overwritten
without the use of a class on the element itself.


#### Important steps:
- Determine with the client/backend what elements are supported (less is better/easier)
  E.g. h1-h6, paragraphs and anchors.
- Add the supported tags to default partial.
- Create presets that can be used to not have to add content in data.yaml.


## Data example
```yaml
news-article:
  type: article
  preset: news-article

editorial-note:
  content: <p>This is an evolving story. Updates will follow</p>

```

## Usage in Template
```hbs
{{> general/wysiwyg news-article class="news-content" }}
{{> general/wysiwyg editorial-note" }}
{{> general/wysiwyg type='article' }}
```

## Static HTML result:
```html
<articlec class="wysiwyg news-content">
  <h2>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusantium, corporis!</h2>
  <p>...</p>
  <h3>Consectetur adipisicing elit. Iusto tempora ullam vel!</h3>
  <p>...</p>
</articlec>
<div class="wysiwyg">
  <p>This is an evolving story. Updates will follow</p>
</div>
<article class="wysiwyg">
  ... content of default partial
</article>
```

## Properties
- type?: HTMLElement (e.g. div or article)
- preset?: string
- class?: string
