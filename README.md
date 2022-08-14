# be-tagmemic [TODO]

Activates scripts / fonts when tags are found in the DOM tree.

```html
<template be-tagmemic>
    <when-acme-1-product-2 where-1='["ny", "ca"]' where-2='["rocket-powered-roller-skates", "giant-kite-kit"]'>
        <script id="acme/1/product-2.js"></script>
    </when-acme-1-product-2>
</template>
```

What this does:

1.  Monitors for the presence of tags with names acme-ny-rocket-powered-roller-skates, acme-ny-giant-kite-kit, acme-ca-rocket-powered-roller-skates, acme-ca-giant-kite-kit.
2.  When such a tag is spotted, emits a corresponding [be-active](https://github.com/bahrus/be-active) template tag, eg:

```html
<template be-active>
    <script id=acme/ny/product-giant-kite-kit.js></script>
</template>
```