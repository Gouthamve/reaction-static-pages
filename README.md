
Installation: 
=============
Copy to packages folder (prefered) or
    
```
meteor add teachmefly:reaction-static-pages
```

.html
=====
somewhere in app
```html
<template name="staticPagesLinks">
    {{#each staticPagesList}}
        <li><a id="{{_id}}-link" href="{{pathFor 'page' route=this.route}}">{{title}}</a></li>
    {{/each}}
</template>
```
.coffee
=======
same
```coffee
Template.staticPagesLinks.helpers
    staticPagesList: ->
        return ReactionCore.existingPages()
```
