# hugo-notice

[![Awesome](https://awesome.re/badge.svg)](https://github.com/budparr/awesome-hugo)

## About

A [Hugo](https://gohugo.io) theme component providing a shortcode: `notice` to display nice notices. Dark mode supported!

Four notice types are provided: `warning`, `info`, `note` and `tip`.

This component comes with __localization in 15 languages__: English, French, German, Italian, Portuguese, Spanish, Chinese, Russian, Turkish, Arabic, Polish, Finnish, Korean, Vietnamese and Swahili.

Other languages welcome! Send your pull request.

![Screenshot](screenshot.png)

## Installation

### Hugo module

1. Initialize your existing site as hugo module

    ```shell
    hugo mod init github.com/USERNAME/REPO
    ```

2. Add the `hugo-notice` as a hugo module to be able to get upstream changes later

    ```shell
    hugo mod get github.com/martignoni/hugo-notice
    ```

3. In your site's or theme's configuration file `hugo.yaml` or `hugo.toml`, add a new `module` section and define both `hugo-notice` and your currently used theme as modules to be imported.

    Example, with `hugo.yaml`:
    ```yaml
    module:
      imports:
        - path: github.com/martignoni/hugo-notice
        - path: my-theme
    ```
    or, with `hugo.toml`,
    ```toml
    [module]
      [[module.imports]]
        path = "github.com/martignoni/hugo-notice"
      [[module.imports]]
        path = "my-theme"
    ```

### Git submodule

1. Add the `hugo-notice` as a submodule to be able to get upstream changes later `git submodule add https://github.com/martignoni/hugo-notice.git themes/hugo-notice`

2. Add `hugo-notice` as the left-most element of the `theme` list variable in your site's or theme's configuration file `hugo.yaml` or `hugo.toml`.

   Example, with `hugo.yaml`:
    ```yaml
    theme: ["hugo-notice", "my-theme"]
    ```
    or, with `hugo.toml`,
    ```toml
    theme = ["hugo-notice", "my-theme"]
    ```
## Usage

In your site, use the shortcode, this way:
    ```go
    {{< notice warning >}}
    This is a warning notice. Be warned!
    {{< /notice >}}
    ```
    or
    ```go
    {{< notice tip >}}
    This is a very good tip.
    {{< /notice >}}
    ```

### Credits

Copyright © 2019 onwards, Nicolas Martignoni nicolas@martignoni.net.

Thanks to
- [Geraldo Ribeiro](https://github.com/geraldolsribeiro) for the Portuguese localization.
- [thatrocketx](https://github.com/thatrocketx) for the Italian localization.
- [casaqori](https://github.com/casaqori) for the Spanish localization.
- [理头张](https://github.com/qidongz) for the Chinese localization.
- [Алексей Корнеев](https://github.com/korney4eg) for the Russian localization.
- [Ahmad Al Maaz](https://github.com/Music47ell) for the Turkish and Arabic localizations.
- [Rafal S.](https://github.com/sulik76) for the Polish localization.
- [Oskari J. Manninen](https://github.com/x7Gv) for the Finnish localization.
- [Haseop Lee](https://github.com/haservi) for the Korean localization.
- [Bùi Nguyễn Hoàng Thọ](https://discourse.gohugo.io/u/hoangtho97/summary) for the Vietnamese localization.
- [callaloo](https://github.com/callaloo) for the Swahili localization.
