# Temporal

{% embed url="https://github.com/tc39/proposal-temporal" %}



2025/07/16時点でStage 3。

```typescript
const d = Temporal.ZonedDateTime.from({
  timeZone: "Asia/Tokyo",
  year: 2000,
  month: 1,
  day: 10
});
// 2000-01-10T00:00:00+09:00[Asia/Tokyo]

d.year; // 2000
d.month; // 1
d.day; // 10
d.dayOfWeek; // 1
```

### ZonedDateTime

特定のタイムゾーンやカレンダーにおける日時。

```javascript
const d = Temporal.ZonedDateTime.from({
  timeZone: "Asia/Tokyo",
  year: 2000,
  month: 1,
  day: 10
});
```

### PlainDateTime

特定のタイムゾーンを持たないカレンダー上の日時。

```javascript
Temporal.PlainDatetime.from({
  year: 2000,
  month: 1,
  day: 10
});
```

システムタイムゾーンとカレンダーからタイムゾーンを得る。

```javascript
Temporal.Now.plainDateTimeISO();
// PlainDateTime 2025-07-16T22:19:04.054
```

### Instant

カレンダーや場所によらない特定の時刻。\
人間に読みやすい形ではないらしい。

```javascript
Temporal.Instant.from("2025-01-10T10:11:12+09:00");
```

