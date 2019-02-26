# Secret Santa Gift
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors)

A portfolio for [Reddy Prasad ](https://www.linkedin.com/in/reddy-prasad-77668817/) as part of secret santa gift.

[Live Website](http://reddyprasad.co.in/)

### Building your site

```
npm run build
```

Copy the content of the `public` folder to your webhost or use a website like Netlify which automates that for you.

Make sure to use the right build command in your build settings e.g. if you use Netlify!
Per default Netlify sets it to `gatsby build` but you have to use `yarn run build` to run postcss before building the Gatsby site.

## Configuration

You have multiple options to configure this project.

1. Use the `config/website.js` to configure data passed to the SEO component and other parts of the Gatsby site:

```JS
module.exports = {
  pathPrefix: '/', // Prefix for all links. If you deploy your site to example.com/portfolio your pathPrefix should be "/portfolio"

  siteTitle: 'Cara - Gatsby Starter Portfolio', // Navigation and Site Title
  siteTitleAlt: 'Cara', // Alternative Site title for SEO
  siteUrl: 'https://portfolio-cara.netlify.com', // Domain of your site. No trailing slash!
  siteLanguage: 'en', // Language Tag on <html> element
  siteLogo: '/logos/logo-1024.png', // Used for SEO and manifest
  siteDescription: 'Playful & Colorful One-Page website with Parallax effect',

  // siteFBAppID: '123456789', // Facebook App ID - Optional
  userTwitter: '@cara', // Twitter Username
  ogSiteName: 'cara', // Facebook Site Name
  ogLanguage: 'en_US', // Facebook Language

  // Manifest and Progress color
  themeColor: tailwind.colors.orange,
  backgroundColor: tailwind.colors.blue,
};
```

2. Use the `tailwind.js` file to configure TailwindCSS. Their [documentation](https://tailwindcss.com/docs/configuration) explains it step-by-step.

3. Modify the files in the `src/styles` directory.

4. You can also place the icons somewhere else on the page, modify their animation and hide them on smaller screens:

```JSX
  <SVG icon="triangle" className={hidden} width={48} stroke={colors.orange} left="10%" top="20%" />
  <SVG icon="hexa" width={48} stroke={colors.red} left="60%" top="70%" />
  <SVG icon="box" width={6} fill={colors['grey-darker']} left="60%" top="15%" />
```

-   For `icon`, you have the options: `triangle, circle, arrowUp, upDown, box, hexa`
-   If you want the SVG to be hidden on mobile view, add `className={hidden}` to the SVG component
-   You can define the width via the TailwindCSS width [option](https://tailwindcss.com/docs/width)
-   The colors get defined via the TailwindCSS color [option](https://tailwindcss.com/docs/colors)
    -   Please note that you will either have to define the color in `stroke` **or** `fill` depending on the icon. For reference, have a look at the currently used SVGs
-   The options `left` and `top` position the icon relatively to its parent container
-   You can also wrap the SVGs with `<UpDown />` or `<UpDownWide />` to animate them

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/all-contributors/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars0.githubusercontent.com/u/15323807?v=4" width="100px;" alt="Shashank Keshava"/><br /><sub><b>Shashank Keshava</b></sub>](https://www.shashankkeshava.com/)<br />[💻](https://github.com/shashankKeshava/reddy-prasad-portfolio/commits?author=shashankKeshava "Code") [🚇](#infra-shashankKeshava "Infrastructure (Hosting, Build-Tools, etc)") |
| :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!