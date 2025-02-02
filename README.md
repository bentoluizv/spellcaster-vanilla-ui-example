# Spellcaster Script Example

Example written using Vanilla JS, the component can be imported through the CDN using the import syntax:

```html
<script type="module">
        import * as core from 'https://cdn.jsdelivr.net/npm/spellcaster-core@0.0.3/+esm';
</script>
```

The content of the package that interacts with the wallet can be accessed via the core.browser component. Through it you can recover the solana object injected by the phantom wallet in the browser, redirecting to the wallet website when the extension is not installed;

```javascript
 const spellcaster = core.browser;

 cosnt provider = spellcaster.getProvider()

 const publicKey = await spellcaster.connect(provider)
```

 If everything goes well and the user accepts the authentication, the wallet's public key will be returned.

 You can see the full example [here](https://github.com/bentoluizv/spellcaster-vanilla-ui-example/blob/main/index.html).
