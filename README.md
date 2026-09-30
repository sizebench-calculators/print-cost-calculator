# 3D Print Cost & Price Calculator

A single-file, open-source web app that calculates the **real cost of a 3D print** and a **selling price** that covers marketplace fees (Etsy, Mercado Livre, Shopee, Amazon) and your profit margin.

- Filament, electricity, printer wear, failure allowance and extras
- Price solved so fees are charged on the **selling price**, not on your cost
- Profit per printer hour
- English, Português and Español (auto-detected)
- One `index.html`: no build, no dependencies, works offline

**Live demo:** https://sizebench-calculators.github.io/print-cost-calculator/ · **Full calculator suite:** [sizebench.com/3d-printing](https://sizebench.com/3d-printing)

## Formulas
```
filament     = grams ÷ 1000 × price per kg
electricity  = watts × hours ÷ 1000 × price per kWh
printer wear = printer price ÷ lifetime hours × print hours
cost         = (filament + electricity + wear) × (1 + failure %) + extras
price        = (cost + fixed fee) ÷ (1 − fee % − margin %)
```
Example: a 50 g, 3 h PLA part costs about **$1.50**. A $5.00 part with 9.5% + $0.45 fees and a 30% margin sells for **$9.01**.

## Run it
Open `index.html` in any browser. To publish: **Settings → Pages → Source: GitHub Actions**. The included workflow deploys on every push to `main`.

## Contributing
Ideas that would help: more languages, currency presets, marketplace fee presets (with sources), resin mode. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License
MIT © [SizeBench](https://sizebench.com)
