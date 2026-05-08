# base-ui-masonry

A responsive, highly optimized, justified masonry layout component with support for variable column widths and virtualization built for being used alongside [BaseUI](https://base-ui.com/) in React projects.

Very recommended to use with `babel-plugin-react-compiler`.

## Installation

### Install dependencies

```bash
npm install justified-layout @base-ui/react @base-ui/utils
```

```bash
pnpm add justified-layout @base-ui/react @base-ui/utils
```

```bash
bun add justified-layout @base-ui/react @base-ui/utils
```

```bash
yarn add justified-layout @base-ui/react @base-ui/utils
```

### Copy and paste the following code into your project

[masonry.tsx](./src/masonry.tsx)

## Anatomy

Import the parts, and compose them together.

```tsx
import {
  Masonry,
  MasonryItem,
} from "@/components/ui/masonry";

return (
  <Masonry columnCount={columnCount} gap={4}>
    <MasonryItem />
  </Masonry>
)
```

Inspired by [DiceUI](https://www.diceui.com/docs/components/base/masonry) and heavily modified.

## License

MIT
