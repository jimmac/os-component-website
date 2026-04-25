+++
template = "index.html"
+++
<picture class="full pixels">
    <source srcset="assets/splash-dark.png" media="(prefers-color-scheme: dark)">
    <img src="assets/splash.png">
</picture>


[OS Component Template](https://github.com/jimmac/os-component-website) is a project that aims to greatly simplify creating a  website for your project. It aims to let you write simple markdown pages and deploy the simple [Zola](https://www.getzola.org/) project to [gitlab](https://gitlab.org) or [github](https://github.com).

Originally built with [Jekyll](https://jekyllrb.com/), the template has been ported to [Zola](https://www.getzola.org/) -- a single static binary with no dependencies. Builds are near-instant and there's no Ruby/gem dependency hell to deal with.

Edit a bit of metadata and tweak some of the included graphics and have a site up in minutes!


- Proper favicon for modern browsers and Apple device icons
- Twitter, Facebook and other social media meta cards for easy sharing. Try [Share Preview](https://flathub.org/apps/details/com.rafaelmardojai.SharePreview) to test.
- Local copy of the amazing [Inter font](https://rsms.me/inter/). No slowdowns pulling from external hosting.
- Mobile friendly, dark variant included.


## Setup

The process of setting up the site locally consists of:

- Install [Homebrew](https://brew.sh/) if you don't have it already. It's a package manager that works on Linux, macOS and WSL, making it the easiest way to install tools like Zola regardless of your platform.

- Install [Zola](https://www.getzola.org/documentation/getting-started/installation/):

```
brew install zola
cd os-component-website
zola serve
```

  Other installation methods are available on the [Zola installation page](https://www.getzola.org/documentation/getting-started/installation/), and some distributions (such as Arch Linux) ship Zola in their repositories.

- Edit the [Zola](https://www.getzola.org/) config file --`config.toml`.
- Replace or edit all the graphics. I recommend using [Inkscape](https://inkscape.org). If you want to shave off some kB out of the SVGs, use [svgo](https://github.com/svg/svgo).

- Test the site locally:
```
zola serve
```

- `git commit` your changes and push to your remote repo for automatic deployment. There is an included `.gitlab-ci.yml` that should be easy to adjust to your gitlab hosting situation. For github pages situation, [see these instructions](https://pages.github.com/). 

Alternatively you can be wild and edit the site directly on github using the remote VSCode editor by pressing `.` after cloning the repo. Right in the browser. It's insane.

Written with love using [Apostrophe](https://flathub.org/apps/details/org.gnome.gitlab.somas.Apostrophe).
