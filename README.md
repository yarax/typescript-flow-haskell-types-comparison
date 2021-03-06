# typescript-flow-haskell-types-comparison

| Type  | Haskell  | TypeScript  | Flow | JsDoc | JSON Schema  |
|---|---|---|---|---|---|
| Union  |  `data Shape = Circle \| Triangle` | `type Shape = CircleInterface \| TriangleInterface`  |  `var Shape: CircleVar \| TriangleVar` | `({x: number, y: number, r: number}|{{x: number, y: number, a: number, b: number, c: number}})` |`anyOf: [{ type: "object"}, { type: "object"}]` |
|Product|`Data Circle = Int Int Int`| `interface Circle {x: number; y: number; radius: number` }| `var Circle = {x: number, y: number, radius: number}` | `{{x: number; y: number; radius: number}}` | `type: "object", properties: {x: "number", y: "number", radius: "number"}` |
| Nullable | Maybe type | `type T1 = (x?: number)` | `var Salary = ?number` | `{?number}` | Depends on parser, either `type: null` if it supports undefined as well or using `required` |
| Non-nulalble | - | `let s = e!.name` | ? | `{!{number}}`  | - | `required: ['field']` |
| Discriminated union  |  Pattern matching in type constructor | [Understanding context](https://github.com/Microsoft/TypeScript/pull/9163)  |  [Understanding context](https://flowtype.org/blog/2015/07/03/Disjoint-Unions.html) |  - | - |
|Generics| `data Maybe a = Nothing \| Just a`  | `interface GenericObject<T> {foo: T;}` | `type GenericObject<T> = { foo: T };` | - | - |
