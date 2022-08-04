Components ported from from bootstrap to only generate content on demand.

The steps for porting a component are as follows:

1. Copy the original component from bootstrap, e.g. /node_modules/bootstrap/scss/_badge.scss
2. Replace .selector with %selector

When using the component you should @extend %selector in your scss code.

```
.wy-badge {
  @extend %badge;
  
}
```
