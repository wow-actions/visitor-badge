# Visitor Badge

> A Github Action to add a badge to count visitors for your issues and PRs.

## Usage

Create `.github/workflows/visitor-badge.yml` in the default branch:

```yaml
name: Visitor Badge
on:
  pull_request:
    types: [opened]
  issues:
    types: [opened]
jobs:
  run:
    runs-on: ubuntu-latest
    steps:
      - uses: bubkoo/visitor-badge@v1
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Inputs

#### GITHUB_TOKEN

Your GitHub token for authentication.

#### color

The color or the badge. You can use any valid HEX color or pick from a predefined set of named colors. Default is `blue`. Note that the HEX colors should be used without `#` symbol prefix.

| color | demo |
| --- | --- |
| `brightgreen` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=brightgreen) |
| `green` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=green) |
| `yellow` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=yellow) |
| `yellowgreen` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=yellowgreen) |
| `orange` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=orange) |
| `red` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=red) |
| `blue` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=blue) |
| `grey` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=grey) |
| `lightgrey` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=lightgrey) |
| `blueviolet` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=blueviolet) |
| `ff69b4` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=ff69b4) |

#### style

The style of the badge. Support `flat`, `flat-square `, `plastic`. Default is `flat`.

| style | demo |
| --- | --- |
| `flat` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=007ec6&style=flat) |
| `flat-square` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=007ec6&style=flat-square) |
| `plastic` | ![](https://img.shields.io/static/v1?label=visitors&message=1234567890&color=007ec6&style=plastic) |

#### label

The label of the badge. Default is `'visitors'`.

![](https://img.shields.io/static/v1?label=ISSUE+VIEWS&message=1234567890&color=007ec6)

![](https://img.shields.io/static/v1?label=PR+VIEWS&message=1234567890&color=007ec6)

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
