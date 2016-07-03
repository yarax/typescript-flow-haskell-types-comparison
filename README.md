# typescript-flow-haskell-types-comparison

| Type  | Haskell  | TypeScript  | Flow | JSON Schema  |
|---|---|---|---|---|
| **Algebraic data types**  |   |   |   |   |
| Enum  |  `data Shape = Circle | Triangle` | `type Shape = CircleInterface | TriangleInterface`  |  `var Shape: CircleVar | TriangleVar` |  `anyOf: [{ type: "object"}, { type: "object"}]` |
| Discriminated union  |  Pattern matching in type constructor | Understanding context (https://github.com/Microsoft/TypeScript/pull/9163)  |  Understanding context (https://flowtype.org/blog/2015/07/03/Disjoint-Unions.html) |  - |
|Product|`Data Circle = Int Int Int`| `interface Circle {x: number; y: number; radius: number` }| `var Circle = {x: number, y: number, radius: number}` | `type: "object", properties: {x: "number", y: "number", radius: "number"}` |
|Abstract data types| ||||
