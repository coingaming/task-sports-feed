You are required to build a tiny application that ingests a list of 5000 sport updates from 10 unique matches in `updates.json`. Each update will be in the format

```json
{
  "match_id": 1,
  "delay": 500,
  "status": "active",
  "name": "Arsenal vs Manchester United",
  "crash": true
}
```

where:
- `match_id` is an integer ID for the match.
- `delay` is the time period in millisecond to wait before processing the current update.
- `status` is the match's current status.
- `name` is the match name.
- `crash` is a boolean value. If `true`, processing the current update should raise an exception and move on to the next update.

All 10 events should be rendered on a web-based UI, and subsequent updates should be displayed in real time.

A few things to note
- No external database should be used. If persistence is needed, it should be done entirely in memory.
- Order is very important. Messages for each match should be processed in the order it was defined in the json file.
- We're very much interested in how you use concurrency.
- We want to see how you test the solution.
- The application does not need to be deployed on a remote server, but appropriate instructions on how to run it locally is essential.
- We prefer that the task is done in Elixir, but it can also be done in any language you're comfortable with.

Good luck!