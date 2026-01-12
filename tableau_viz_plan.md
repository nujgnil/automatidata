# Tableau Visualization Plan (Accessible)

## Dataset preparation
- Use the cleaned dataset (drop negative durations, exclude trips with duration > 120 minutes for summary charts).
- Keep core fields: pickup/dropoff time, trip distance, fare, payment type, passenger count, and location IDs.

## Recommended sheets
1) Trips by month (line chart)
   - X: pickup month
   - Y: trip count
2) Trip duration distribution (box plot or histogram)
   - X: duration (minutes)
   - Y: trip count (if histogram)
3) Payment type distribution (bar chart)
   - X: payment type
   - Y: trip count
4) Top pickup locations (bar chart)
   - X: PULocationID (or zone name if joined)
   - Y: trip count

## Dashboard layout
- Top: Monthly trip trend (largest visual)
- Middle: Trip duration distribution
- Bottom: Payment type and top pickup locations side-by-side
- Include filters for month and payment type

## Accessibility notes
- Use a high-contrast, colorblind-safe palette (avoid relying only on color).
- Add direct labels and clear titles; increase font sizes for titles and axis labels.
- Provide text descriptions of each chart in the dashboard caption.
- Avoid red/green contrasts and small marks; use thicker lines and larger bars.
- Make tooltips concise with plain language and units (minutes, miles, dollars).
