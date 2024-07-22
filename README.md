# shortcode-rewards

A Hugo theme component with `reward-log` or `sponsor-log` shortcode.

## Demo

## Requirements

- FixIt v0.3.9 or later.

## Install Component

The installation method is the same as [installing a theme](https://fixit.lruihao.cn/documentation/installation/). There are several ways to install, choose one, for example, install through Hugo Modules:

```diff
[module]
  [[module.imports]]
    path = "github.com/hugo-fixit/FixIt"
+ [[module.imports]]
+   path = "github.com/hugo-fixit/shortcode-rewards"
```

## Inject Partial

Inject the `shortcode-rewards.html` into the `custom-assets` through the custom block opened by the FixIt theme in the `layouts/partials/custom.html` file:

```go-html-template
{{- define "custom-assets" -}}
  {{- partial "inject/shortcode-rewards.html" . -}}
{{- end -}}
```

## Usage

First, create the `reward-log.yml` file and edit your data:

```bash
cp themes/shortcode-sponsor-log/reward_log.yml.example data/reward_log.yml
```

> If your site is multilingual, you can create a `reward_log.en.yml` file for English and `reward_log.zh-cn.yml` for Chinese.

Next, use the `reward-log` shortcode in any page:

```markdown
{{< reward-log >}}
```

> [!note]
> For compatibility with older versions, `sponsor-log` shortcode can also be used, and the corresponding data file is `sponsor_log.yml`.

## References

- [Develop Theme Components | FixIt](https://fixit.lruihao.cn/contributing/components/)
- [How to Develop a Hugo Theme Component | FixIt](https://fixit.lruihao.cn/components/dev-component/)
