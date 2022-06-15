# 1. installation

## CDN

```html
<head>
    <script src="https://flesanalysis.s3.ap-northeast-2.amazonaws.com/v0.2.3/bundle.js"></script>
</head>
```

## setup

```html
<script>
      const accessKey = 'YOUR ACCESSKEY';
      const FA = new FlesAnalysis(accessKey);
      FA.start();
</script>
```

## usage

if you want to check, go to event page

```js
window.analytics.track('event', object);
```
