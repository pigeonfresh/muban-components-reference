# Heading

In some cases the Content Manager wants to control the element type used for headings. Semantics and
SEO might be the argument to want to change the type of heading used. Having them as options in the
mock-data will steer the backend developer into implementing this feature. As a developer we might
want to keep control over the styling. We can do this by using our default type styling or/adding
our classes. If the Content Manager has additional options (e.g. colors or text effects) we can
combine this with our own classes.

## Data example
```yaml
main-title:
  type: h2
  copy: Lorem Ipsum
  style: 'is-light'

subtitle:
  type: h3
  copy: Dolor elut

```

## Usage in Template
```hbs
{{> general/heading main-title class="heading-1 main-title" }}
{{> general/heading sub-title }}
```

## Static HTML result:
```html
<h2 class="heading-1 main-title is-light">
  Lorem Ipsum
</h2>
<h3>
  Dolor elut
</h3>
```

## Properties
- type: h1-h6
- copy: string
- style?: string
- class?: string
