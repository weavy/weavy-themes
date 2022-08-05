Components ported from from bootstrap to only generate content on demand.
The steps for creating a component that is based on an similar bootrap component is as follows:

1. Copy the original component from `/lib/bootstrap`.
2. Replace `.selector` with `%selector`.
3. Use `@extend %selector` when creating your component.

For example to create a `.wy-badge` you can do this:

1. Copy `/lib/bootstrap/_badge.scss` to `./_badge.scss`.
2. Replace `.badge` with `%badge`.
3. Create `../components/_badge.scss`. 

   ```
   @use "../bootstrap/badge";
   
   .wy-badge {
     @extend %badge;
    }
   ```
