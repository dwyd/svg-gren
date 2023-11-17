__A SVG package for [Gren](https://gren-lang.org/), uses the [HTML package](https://github.com/icidasset/html-gren/) as the foundation.__

🐉 I haven't properly tested this yet, so there be dragons.

```gren
import Transmutable.Html
import Transmutable.Html.VirtualDom
import Transmutable.Svg exposing (Svg, svg)
import Transmutable.Svg.Attributes as A

someSvg : Svg msg -- Just an alias for `Transmutable.Html.Html msg`
someSvg =
  svg
      [ A.fill "none"
      , A.viewBox "0 0 201 233"
      ]
      []

string =
  Transmutable.Html.toString someSvg

virtualDom =
  Transmutable.Html.VirtualDom.toVirtualDom someSvg
```

You can convert this SVG/HTML to `VirtualDom` using [this package](https://packages.gren-lang.org/package/icidasset/html-virtualdom-gren/).
