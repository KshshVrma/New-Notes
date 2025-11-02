PUT /stocks/TCS?newPrice=3500
Header: User-Agent: Postman
Body:
{
  "name": "Tata Consultancy Services",
  "price": 3500
}

@PutMapping("/stocks/{symbol}")
public String updateStock(@PathVariable String symbol,
                          @RequestParam double newPrice,
                          @RequestHeader("User-Agent") String userAgent,
                          @RequestBody Stock stockDetails) {
    return "Updated " + symbol + " to " + newPrice + " by " + userAgent +
           ", details: " + stockDetails.getName();
}
