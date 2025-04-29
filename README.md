Interview - Full Stack Engineer 
===================

## Overview

You’ve been brought in to bootstrap a full stack application for a commodities trading analytics platform. Your job is to create an API with a simple frontend that can receive trade data and display useful insights for traders.

## ⏱️ Time Estimate

Take-home portion: ~3-4 hours max

## 🔧 Requirements

### 1. REST API Endpoints

Build a small API with the following routes:

* `POST /trades`: Accepts a batch of commodity trade data in JSON format.

* `GET /trades`: Returns a list of trades

* `GET /insights`: Returns aggregated statistics based on submitted trades.

#### Trade Data Input Format (`POST /trades`)


```
[
  {
    "commodity": "Gold",
    "traderId": "T123",
    "price": 2023.5,
    "quantity": 10,
    "timestamp": "2025-04-10T14:30:00Z"
  },
  {
    "commodity": "Oil",
    "traderId": "T456",
    "price": 85.2,
    "quantity": 100,
    "timestamp": "2025-04-10T15:10:00Z"
  }
]
```
#### Insights Output Format (`GET /insights`)

The response should return:

* `totalVolumeByCommodity`: The sum of all traded quantities per commodity.

* `averagePriceByCommodity`: The average price per commodity.

* `topTradersByVolume`: A ranked list of traders by total traded quantity.

#### Example output:

```
{
  "totalVolumeByCommodity": {
    "Gold": 10,
    "Oil": 100
  },
  "averagePriceByCommodity": {
    "Gold": 2023.5,
    "Oil": 85.2
  },
  "topTradersByVolume": [
    { "traderId": "T456", "volume": 100 },
    { "traderId": "T123", "volume": 10 }
  ]
}
```

### 2. Dashboard

Build a simple dashboard on top of the APIs that displays the information in a clean and intuitive way. You may wish to generate some additional mock data to showcase a more representative UX.

## Technical Constraints / Considerations

* Use either **Python** or **Node.js** for the backend

* Build the front end however you see fit (consider that we are optimising for speed of development as well as simplicity)

* Use **in-memory storage** (no database required).

* All API responses must be in **JSON**.

Your code should be clean, modular, and generally easy to follow. Write tests if it helps your development process

## Evaluation Criteria

✅ Correctness and completeness of the API

✅ Proper aggregation of data and handling of edge cases

✅ Code clarity, structure, and modularity

✅ Graceful handling of errors and malformed input

✅ Use AI code generation tools if you wish, but if you aren’t able to adequately explain resulting code this will work against you

## Submission Instructions

Please submit your project as a GitHub repo. Include a short `README.md` with:

* Setup and run instructions

* Dependencies

* Any assumptions or notes

Keep it simple. Don’t over-engineer. Clean, functional, readable code is what we’re after.
