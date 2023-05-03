# Welcome to Gunmetal Code pro

## About the theme

An aesthetically pleasing, multifaceted, contemporary and sophisticated chromatic scheme constructed to augment the legibility of code and optimize user productivity.

### Suggest Editor Settings

Utilize the aforementioned editor configurations to achieve optimal outcomes. Cascadia Code is pre-embedded within the Windows Terminal, thus installation may be superfluous. If employing an alternate font, it may be necessary to modify the font family, font size and line height to one’s preference.

```json
"editor.fontSize": 15,
"editor.lineHeight": 24,
"editor.fontFamily": "Cascadia Code",
"editor.fontLigatures": "'calt','ss01', 'ss02', 'ss03', 'ss04', 'ss05', 'ss06', 'ss20', 'cv01', 'cv02', 'zero', 'onum'",
"editor.fontVariations": true,
```

Cascadia Code Download: <https://github.com/microsoft/cascadia-code/releases/tag/v2111.01>

### Tweaks & theming

Should one desire to experiment with novel hues, the `workbench.colorCustomizations` setting may be utilized to tailor the presently chosen theme. For instance, the following code snippet may be incorporated into one’s `"settings.json"` file:

```json
"workbench.colorCustomizations": {
  "tab.activeBackground": "#282c34",
  "activityBar.background": "#282c34",
  "sideBar.background": "#282c34",
  "tab.activeBorder": "#d19a66",
}
```

or use the setting `editor.tokenColorCustomizations`

```json
"editor.tokenColorCustomizations": {
  "[Gunmetal Code Pro]": {
    "textMateRules": [
      {
        "scope": ["source.python"],
        "settings": {
          "foreground": "#e06c75"
        }
      }
    ]
  }
}
```

#### Italic

One could configure their settings.json to render code entirely in italicized font. Nevertheless, this is not advocated as the theme has been astutely devised to integrate italic typeface in specific locations to enhance legibility.

```json
"editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "name": "italic font",
        "scope": [
          "comment",
          "keyword",
          "storage",
          "keyword.control",
          "keyword.control.from",
          "keyword.control.flow",
          "keyword.operator.new",
          "keyword.control.import",
          "keyword.control.export",
          "keyword.control.default",
          "keyword.control.trycatch",
          "keyword.control.conditional",
          "storage.type",
          "storage.type.class",
          "storage.modifier.tsx",
          "storage.type.function",
          "storage.modifier.async",
          "variable.language",
          "variable.language.this",
          "variable.language.super",
          "meta.class",
          "meta.var.expr",
          "constant.language.null",
          "support.type.primitive",
          "entity.name.method.js",
          "entity.other.attribute-name",
          "punctuation.definition.comment",
          "text.html.basic entity.other.attribute-name",
          "tag.decorator.js entity.name.tag.js",
          "tag.decorator.js punctuation.definition.tag.js",
          "source.js constant.other.object.key.js string.unquoted.label.js",
        ],
        "settings": {
          "fontStyle": "italic",
        }
      },
    ]
  }
```

## Python & Pylance users

For Python users, I advocate the utilization of the [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance) extension to facilitate rapid and multifaceted language assistance.

Semantic hues may be personalized within settings.json by correlating the Pylance semantic token classifications and modifiers with the preferred colors.

- Semantic token types

  - class, enum
  - parameter, variable, property, enumMember
  - function, member
  - module
  - intrinsic
  - magicFunction (dunder methods)
  - selfParameter, clsParameter

- Semantic token modifiers
  - declaration
  - readonly, static, abstract
  - async
  - typeHint, typeHintComment
  - decorator
  - builtin

The [scope inspector](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide#scope-inspector) instrument facilitates the exploration of semantic tokens present within a source file and the identification of corresponding theme regulations.

Example of customizing semantic colors in settings.json:

```jsonc
{
  "editor.semanticTokenColorCustomizations": {
    "[Gunmetal Code Pro]": {
      // Apply to this theme only
      "enabled": true,
      "rules": {
        "magicFunction:python": "#ee0000",
        "function.declaration:python": "#990000",
        "*.decorator:python": "#0000dd",
        "*.typeHint:python": "#5500aa",
        "*.typeHintComment:python": "#aaaaaa",
        "parameter:python": "#aaaaaa"
      }
    }
  }
}
```

Please check the official documentation for
[Theme Color Reference](https://code.visualstudio.com/docs/getstarted/theme-color-reference) and
[Theme Color](https://code.visualstudio.com/docs/getstarted/themes), for more helpful information on building your own themes.

## CHANGELOG

Check out any changes and any new features of this extension in the [CHANGELOG.MD](https://github.com/DrInfinite/gunmetal-code-pro/blob/main/CHANGELOG.md) file.
