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


## 🧩 1️⃣ When to use `@PathVariable` vs `@RequestParam`

|Case|Use|Example|
|---|---|---|
|**Resource identification**|`@PathVariable`|`/users/42` → identifies _which user_|
|**Filtering / options**|`@RequestParam`|`/users?sort=desc&page=2` → adds _extra behavior_|

👉 **Rule of thumb:**

- Use **PathVariable** for unique identifiers (acts like a _noun_ in a REST resource).
    
- Use **RequestParam** for filters, pagination, search parameters (acts like _adjectives_).
    

**Example:**

`@GetMapping("/users/{id}") public User getUser(@PathVariable int id) { ... }  @GetMapping("/users") public List<User> getUsers(@RequestParam int page, @RequestParam int limit) { ... }`

---

## 📬 2️⃣ Why use `@RequestBody` only for POST/PUT (not GET)

GET requests are meant to **retrieve** data and **should not have a body** as per HTTP standard.

- Most browsers, proxies, and frameworks ignore bodies in GET requests.
    
- POST and PUT, on the other hand, are meant to **send or modify** data, so they support request bodies.
    

**Example:**

`@PostMapping("/stocks") public Stock createStock(@RequestBody Stock stock) { ... }  // ✅ valid`

If you try this:

`@GetMapping("/stocks") public Stock getStock(@RequestBody Stock stock) { ... }  // 🚫 ignored by clients`

…it may not work because GET doesn’t process body content.

---

## 🧱 3️⃣ What if JSON keys don’t match Java field names?

Spring uses **Jackson** to convert JSON ↔ Java.  
If keys don’t match, those fields simply stay **null or default**.

Example:

`class Stock {     private String name;     private double price; }`

Request:

`{   "stockName": "TCS",   "price": 3400 }`

→ `name` becomes `null` because `stockName ≠ name`.

✅ Fix it using:

`@JsonProperty("stockName") private String name;`

So the JSON key `"stockName"` maps to `name`.

---

## 🔐 4️⃣ How to pass a JWT token from frontend → Spring Boot controller

JWTs are sent via the **Authorization header** using the Bearer scheme.

### Frontend (React, Angular, etc.)

`fetch("/api/users", {   headers: {     "Authorization": "Bearer " + token   } });`

### Spring Boot Controller

`@GetMapping("/api/users") public String getUser(@RequestHeader("Authorization") String authHeader) {     System.out.println("Token received: " + authHeader);     return "OK"; }`

In real apps, Spring Security automatically extracts and validates the token using a **JWT filter** or the `OAuth2ResourceServer` setup.