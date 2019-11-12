# CTA Component

The CTA component is used for cta links or buttons. It renders by default an anchor but can be a button (or any other
html object).

## Data example
```yaml
login-cta:
  type: button
  class: login-google
  copy: Log in with Google
```

## Usage in Template
```hbs
{{> general/cta }}
{{> general/cta class="secondary" copy="More info" }}
{{> general/cta login-cta }}
```

## Static HTML result:
```html
<a href="#" class="cta">Read More</a>
<a href="#" class="cta secondary">More Info</a>
<button class="cta login-google">Log in with Google</button>
```

## Properties
- type?: HTMLElement (default: a)
- href?: URL (default: # unless a type is defined)
- title?: String
- class?: String
- target?: String (e.g: _blank)
- copy?: String (default: Read more)
