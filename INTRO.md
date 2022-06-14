# 1. installation

## CDN

```html
<head>
  <script src="https://flesanalysis.s3.ap-northeast-2.amazonaws.com/bundle.js"> </script>
</head>
```

## setup

```html
<script>
    (async () => {
      // audienceM을 통해서 발급받은 accessKey, secretKey키
      const accessKey = 'YOUR ACCESSKEY'; 
      const secretKey = 'secretkey-test';       
                         
      t=new FlesAnalysis(accessKey,"secretkey-test");!function(){var i=window.analytics=window.analytics||[];if(!i.initialize)if(i.invoked)window.console&&console.error&&console.error("Segment snippet included twice.");else{i.invoked=!0,i.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","once","off","on","addSourceMiddleware","addIntegrationMiddleware","setAnonymousId","addDestinationMiddleware"],i.factory=function(e){return function(){var t=Array.prototype.slice.call(arguments);return t.unshift(e),i.push(t),i}};for(var n=0;n<i.methods.length;n++){var a=i.methods[n];i[a]=i.factory(a)}i.load=function(e,t){var n=document.createElement("script");n.type="text/javascript",n.async=!0,n.src="https://cdn.segment.com/analytics.js/v1/"+e+"/analytics.min.js";var a=document.getElementsByTagName("script")[0];a.parentNode.insertBefore(n,a),i._loadOptions=t},i._writeKey="BIPs9934EYbVKIU8zp86wBxM6JE0hhOn",i.SNIPPET_VERSION="4.13.2",i.load("BIPs9934EYbVKIU8zp86wBxM6JE0hhOn"),i.addSourceMiddleware((async({payload:i,integration:n,next:a})=>{let{obj:r}=i;if("identify"===r.type){const n=i.obj.traits,a=await t.encrypt(n);i.obj.traits=a,i.obj.traits.appKey=e,i.obj.traits.fingerPrint=t.flesSDK.visitorId}else i.obj.properties.appKey=e,i.obj.properties.fingerPrint=t.flesSDK.visitorId;a(i)})),window.analytics=i,i.page()}}()})();
    })();
</script>
```

## usage

if you want to check, go to event page

```js
window.analytics.track('event', object);
```
