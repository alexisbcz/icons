# icons

Lucide, Tabler and Hugeicons icons as Go functions that render SVG.

## Install

```sh
go get github.com/alexisbcz/icons
go mod tidy
```

## Use

```go
package main

import (
	"fmt"

	"github.com/alexisbcz/icons/hugeicons"
	"github.com/alexisbcz/icons/lucide"
	"github.com/alexisbcz/icons/tabler"
	h "github.com/alexisbcz/libhtml"
)

func main() {
	for _, icon := range []h.Node{
		lucide.Check(h.Class("size-4")),
		tabler.IconBell(),
		hugeicons.Add01Icon(),
	} {
		html, _ := h.RenderString(icon)
		fmt.Println(html)
	}
}
```

## License

MIT. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
