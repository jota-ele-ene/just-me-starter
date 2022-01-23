# Hugo Just me! theme Forestry starter

This repo serves the demo site for **[Just me!](https://github.com/jota-ele-ene/just-me)**, a minimal and fancy theme for [Hugo](http://gohugo.io/) to create Personal Pages with no blog or extra content, just awesome rotating backgrounds and your social profiles to allow people contact you. This demo site is deployed here: https://jota-ele-ene.github.io/just-me-starter.

![Just me! screenshot](https://raw.githubusercontent.com/jota-ele-ene/just-me/main/images/screenshot.png)

## Features

- Just a homepage with rotating fullscreen backgrounds
- Configure it including your social profiles
- Manage both backgrounds and social profiles like any other content in Hugo to avoid hard-coding in config-files
- Support for Google Analytics
- Contact form (in progress)

## Getting started

The easiest way to get started is to [import this theme in Forestry CMS](https://app.forestry.io/quick-start?repo=jota-ele-ene/just-me-starter&engine=hugo&version=0.81.0&branch=main) in a single click

<a href="https://app.forestry.io/quick-start?repo=jota-ele-ene/just-me-starter&engine=hugo&version=0.81.0">
    <img alt="Import this project into Forestry" src="https://assets.forestry.io/import-to-forestryK.svg" />
</a>

Once the import is complete, you can start to customize your site editing front matter for backgrounds, profiles and home page. They are accesible from the **Forestry** sidebar. 

## Configuring the Home Page

The site's home and only page can be accesed from the `Pages` menu on the Forestry sidebar. It appears under the title `Hello World`. When you click on it, the content itself will be displayed on the right panel. The theme will display the `title` param highlighted in the middle and the page and the content itself as a kind of subtitle. Edit them to fit your needs. This is the text by default:

```
Yes! You reach my personal page. Welcome here. I'm **John doe**.
Find me at [Linkedin](#), read some of my thoughts in [my blog](#) or visit my photos at [Flickr](#).
```

### Configuring Social Profiles

Beyond the claim and the text, the homepage also includes some social icons linked to your social profiles. You can manage them like any other content by accesing the `Profiles` section on Forestry sidebar. By default, 19 profiles are included with the theme. 

Consider that:

1. Each content determine a social profile. 

2. You can create additional social icons by clicking the `Create new` button on the top of the page. Forestry does not import your Hugo archetypes. So, choose one of the existing profiles as an example to create a front matter template in Forestry.

3. There are two types of profiles. Most common ones are those where an icon exists in the [Font Awesome icon set](https://fontawesome.com/). If you can find the icon for your new profile there, fill in the `profile` field. For example, if you want to add your Github profile, an icon exists for **Github**. To use the Github icon everywhere, your HTML must include this code:

    ```
    <i class="fab fa-github"></i>
    ```

    To use it in your home page rendered with **Just-me!**, set the `profile` field, removing the `fa-` prefix.

    If you can't find an icon in Font Awesome, you can provide your own image. Review `blog` profile to see an example about how the picture is referred.

4. Only the profiles with `draft` field set to `false` are shown in the homepage.

### Favicon

To update favicon of the site, override the ones in `static/icons/` folder with your own. You can also review the template `partials\head\icons.html` to understand how they are included in your pages.

### Backgrounds

Just like Social icons, you can manage your homepage backgrounds by editing the existing content accesible from the `Backgrounds` section in Forestry sidebar.

Review the examples to see the fields included in these contents. The most important one are the `imageURL` and `imagesize` variables. The theme will use it to set the `image-background` style property for the background. On loading, the theme will build the page including only those backgrounds with the field `draft` set to `false`. Additionally, the scripts will process the `size` param to use only those images that match with the window current orientation (landscape or portrait). After any `resize` event, orientation is re-evaluated.

The rest of the fields will be used to attribute image credits. You can acces them by clicking in the `i` icon on the right-bottom corner of the page.

## License

This repo is licensed under the **MIT** license. Check the [LICENSE file](https://github.com/jota-ele-ene/just-me-starter/blob/main/LICENSE) for details.

Thanks to the authors of following resources, among others, used for developing this code:

- [Font Awesome](https://fontawesome.com/), a popular icon set that I use to display the social profiles
- [Unsplash](https://unsplash.com), the internet’s source of freely-usable images where I have taken the sample backgrounds from

## Author

José Luis Núñez [https://joseluisnuñez.es](https://joseluisnuñez.es)

if you find this repo useful, enjoy it and please consider buying me a coffee ☕️.

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/U7U27W8VV)

Thanks! ❤️

