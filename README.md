
# 🧠 Frontend Engineer Assessment – Uri

Welcome! This short assessment is designed to evaluate your practical skills with **Next.js**, **React**, **Material UI**, **data visualization**, and **performance optimizations**.

> ⏱ **Time Limit:** 2 hours  
> 🛠 **Stack:** Next.js, TypeScript, Material UI, @mui/x-charts

---

## 🎯 Task: Hashtag Sentiment Insight Page

Create a page at `/insights/[hashtag]` that fetches hashtag sentiment data and displays it in a styled, interactive chart card.

---

## ✅ Requirements

1. **Dynamic route:** `/insights/[hashtag]`
2. **Fetch data** from a mocked API: `/api/trends/[hashtag]`
3. **Render an interactive chart** using `@mui/x-charts/LineChart`
4. **Good layout** make design appealing
5. Show:
   - Hashtag title (e.g. `#uri`)
   - Date range (e.g. `Apr 1 - Apr 7, 2025`)
   - Sentiment trend line
   - Indicator for trend direction (📈 or 📉)
6. Implement:
   - Loading state (e.g. skeleton or spinner)
   - Error state (e.g. message + retry)
   - Mobile responsiveness
7. Use `React.memo`, `useMemo`, and `useCallback` where appropriate

---

## 🧪 Sample API Response

Simulate a GET request to `/api/trends/uri` that returns:

```json
{
  "hashtag": "#uri",
  "range": "Apr 1 - Apr 7, 2025",
  "trend": [
    { "date": "2025-04-01", "sentiment": -0.2 },
    { "date": "2025-04-02", "sentiment": 0.0 },
    { "date": "2025-04-03", "sentiment": 0.1 },
    { "date": "2025-04-04", "sentiment": 0.3 },
    { "date": "2025-04-05", "sentiment": 0.2 },
    { "date": "2025-04-06", "sentiment": 0.4 },
    { "date": "2025-04-07", "sentiment": 0.5 }
  ]
}
```

You can hardcode this response or use a local file or API route under `/pages/api/trends/[hashtag].ts`.

---

## 📁 Suggested File Structure

```
/pages
  /insights/[hashtag].tsx
  /api/trends/[hashtag].ts
/components
  HashtagTrendCard.tsx
  SentimentChart.tsx
/hooks
  useHashtagTrend.ts
/mocks
  trendData.ts
```

---

## 💡 Bonus (Optional)

- Add a dropdown to switch hashtags
- Chart zoom/pan interaction
- Min/max sentiment markers
- Dark mode support
- Lazy-load chart with `next/dynamic`

---

## 📦 Submission Instructions

- Push your code to a **GitHub repo** (public or private)
- Include in your `README.md`:
  - Brief overview of your approach
  - Screenshots/Demo
  - Time spent
- Share the link with us

---

## 🔥 Tips

- Use **React Query** or **SWR** in `useHashtagTrend`
- Optimize renders with memoization
- Keep your code clean and componentized
- If anything is unclear, explain your assumptions

---

Good luck!  
💜 Team Uri
