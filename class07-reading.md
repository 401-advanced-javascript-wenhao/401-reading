# Reading 07 - Express

## Express Routing
1. Event Driven
  * `app.get('/route', (req, res) => {})`
  * Same pattern in vanialla JS and jQuery
  * this is async operation
2. req Object
  * params property: `app.get('/route/:number', ...)`. The value passed in :number will show up on `req.params.number`
  * query property: `localhost:3000/api?example=1`. `req.query.example === 1`
3. res Object
