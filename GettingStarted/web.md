---
description: how to apply on web
---

# CDN

```html
<head>
  <script src="https://flesanalysis.s3.ap-northeast-2.amazonaws.com/bundle.js"> </script>
</head>
```

or 

specity version

```html
<head>
  <script src="https://flesanalysis.s3.ap-northeast-2.amazonaws.com/[버전]/bundle.js"> </script>
</head>
```

# setup

```html
<script>
    (async () => {
      // audienceM을 통해서 발급받은 accessKey, secretKey키
      const accessKey = 'web SDK test key-askdfksdf1243295 zcxmz'; 
      const secretKey = 'secretkey-test';                          

      const FA=new FlesAnalysis(accessKey,secretKey);!function(){var e=window.analytics=window.analytics||[];if(!e.initialize)if(e.invoked)window.console&&console.error&&console.error("Segment snippet included twice.");else{e.invoked=!0,e.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","once","off","on","addSourceMiddleware","addIntegrationMiddleware","setAnonymousId","addDestinationMiddleware"],e.factory=function(t){return function(){var a=Array.prototype.slice.call(arguments);return a.unshift(t),e.push(a),e}};for(var t=0;t<e.methods.length;t++){var a=e.methods[t];e[a]=e.factory(a)}e.load=function(t,a){var n=document.createElement("script");n.type="text/javascript",n.async=!0,n.src="https://cdn.segment.com/analytics.js/v1/"+t+"/analytics.min.js";var i=document.getElementsByTagName("script")[0];i.parentNode.insertBefore(n,i),e._loadOptions=a},e._writeKey="3XsdMzbGab5BiR8WuTdFyqTA3jYcdIEH",e.SNIPPET_VERSION="4.13.2",e.load("BIPs9934EYbVKIU8zp86wBxM6JE0hhOn"),e.addSourceMiddleware(({payload:e,integration:t,next:a})=>{e.obj.properties.appKey=accessKey,e.obj.properties.fingerPrint=FA.flesSDK.visitorId;let{obj:n}=e;FA.track(n),a(e)}),window.analytics=e,e.page(),FA.registerClickEvent("click",e=>{window.analytics.track("User Event",{eventType:"click",customData:(new Date).getTime()})}).registerClickEvent("mousemove",e=>{window.analytics.track("User Event",{eventType:"mousemove",customData:(new Date).getTime()})}).registerClickEvent("scroll",e=>{window.analytics.track("User Event",{eventType:"scroll",customData:(new Date).getTime()})}).start()}}();
    })();
</script>
```

# usage

if you want to check, go to [event page](../Events/general.md)

```js
window.analytics.trace('event', object);
```