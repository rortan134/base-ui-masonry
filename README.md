# base-ui-masonry

A responsive, highly optimized, justified masonry layout component with support for variable column widths and virtualization built for being used alongside [BaseUI](https://base-ui.com/) in React projects.

Very recommended to use with `babel-plugin-react-compiler`.

## Why

CSS `column`-based masonry layouts reorder items vertically, breaking logical tab order and keyboard navigation. True masonry requires absolute positioning with explicit top/left coordinates, but computing those layouts efficiently becomes difficult as the number of items grows.

Scroll performance and layout stability introduce further challenges. As items resize or new ones are measured, the layout must update incrementally without causing visible jumps or expensive recalculations. Responsive column counts, variable-width items, and justified row packing each add another layer of complexity.

base-ui-masonry provides a low-level, virtualized masonry and justified-layout engine that preserves DOM order, uses interval-tree spatial indexing for O(log n) scroll queries, integrates with BaseUI's resize observation and animation frame primitives, and follows BaseUI's component practices for smooth, accessible, performant layouts.

## 1. Installation

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

and [justified-layout.d.ts](./justified-layout.d.ts) if you run into type issues.

## 2. Anatomy

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
