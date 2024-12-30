# Nuxt 3 Components Management Example

If there are components that I've needed to break out just for one page, they belong in a sub-folder of that page. There is no need for me to hunt around. This also saves you from going up/down the folder tree all the time just to complete a feature.

In the example above, it's assumed the Product components are special to the gallery page. The second they are needed on any OTHER page, then they should be moved into the old components folder. That folder should be reserved for any component that's used on multiple pages, or doesn't belong to any one page (like global modals).

I don't recommend using auto import in local components, if you want to use auto import you can add this code on your nuxt config

```js
components: [
  '~/components', {
    path: '~/pages',
    pattern: '*/components/**',
    pathPrefix: false
  }
]
```

## Getting Started
1. Install dependencies:

```
bun install
```

2. Run the application:
```
bun dev
```

3. Open your browser and visit http://localhost:3000 to see the application in action.


src : https://deltener.com/blog/nuxt-enterprise-patterns-component-management