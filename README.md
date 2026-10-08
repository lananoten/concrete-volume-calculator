# Concrete Volume Calculator

A tiny, dependency-free concrete calculator. Open `index.html` in any browser — no build step, no dependencies, no signup.

## What it calculates

Four shapes, each with adjustable waste buffer (5% / 10% / 15%):

| Shape | Inputs |
|---|---|
| **Slab** | Length (ft) × Width (ft) × Thickness (in) |
| **Post hole** | Diameter (in) × Depth (in) × Number of holes |
| **Trench footing** | Width (in) × Depth (in) × Length (ft) |
| **Wall** | Length (ft) × Height (ft) × Thickness (in) |

Outputs for every calculation:

- Cubic yards and cubic feet (exact)
- Order quantity with your chosen waste buffer
- Bag counts across all four standard sizes (80 / 60 / 50 / 40 lb)
- Delivery hints (short-load fee warning under ~4 yd³, multi-truck note over 10 yd³)

## Formulas

```
Slab:          L(ft) × W(ft) × (T(in) ÷ 12) ÷ 27            = cubic yards
Post hole:     π × (Dia(in) ÷ 24)² × (Depth(in) ÷ 12)       = cubic feet (× holes)
Trench:        (W(in) ÷ 12) × (D(in) ÷ 12) × L(ft) ÷ 27     = cubic yards
Wall:          L(ft) × H(ft) × (T(in) ÷ 12) ÷ 27            = cubic yards
Order qty:     Cubic Yards × (1 + waste)
```

Bag yields per cubic foot of mixed concrete: 80 lb = 0.60, 60 lb = 0.45, 50 lb = 0.375, 40 lb = 0.30. Bag counts always round up.

## Worked example

16 × 30 ft slab at 4" thick, 10% waste:

- 160 cu ft ÷ 27 = **5.93 yd³** exact → **6.52 yd³** to order
- Bags: 267 × 80 lb (or 356 × 60 lb)

## When to use ready-mix vs. bags

- **Bags** make sense under ~1.5 yd³ (up to ~60–70 eighty-pound bags).
- **Ready-mix truck** wins above ~2 yd³ — cheaper per yard, faster, no cold joints.
- **Short-load fees** ($75–$120) apply under ~4 yd³ — combine small pours when possible.

## More calculators

For stairs, columns, rebar, block walls, gravel subbase, and full project cost estimation — 30 free tools, no signup: <https://concretecalcus.com/>

## License

MIT — see [LICENSE](LICENSE).
