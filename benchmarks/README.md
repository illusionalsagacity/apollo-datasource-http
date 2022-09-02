# Benchmark

```
node http.js
```

## HTTP1

Compare `apollo-datasource-http` (HTTP1 + Undici Pool) with apollo's `apollo-datasource-rest` (HTTP1 + keepalive).

```
❯ node benchmarks/http.js
{
  'apollo-datasource-rest (http1)': { startTime: 1557606834329000n, endTime: 1557608744837333n },
  'apollo-datasource-http (http1)': { startTime: 1557606879482875n, endTime: 1557607752716750n }
}
Results for 1000 subsequent requests:
apollo-datasource-rest (http1) | total time: 1910508333ns (1910.508ms)
apollo-datasource-http (http1) | total time: 873233875ns (873.234ms)
---
apollo-datasource-http (http1) <> apollo-datasource-rest (http1) percent change: -54.293%
```

**Result:** `apollo-datasource-http` is around `50%` faster than `apollo-datasource-rest`
