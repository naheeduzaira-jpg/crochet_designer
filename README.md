# genz-crochet shop with backend

## Run it
1. Install Python 3.9 or newer.
2. In this folder run: `pip install -r requirements.txt`
3. Set an admin password, then start the server:
   - Windows: `set ADMIN_PASSWORD=your-secret` then `python app.py`
   - Mac/Linux: `ADMIN_PASSWORD=your-secret python app.py`
4. Open http://127.0.0.1:5000 for the shop and http://127.0.0.1:5000/admin to see orders
   (any username, your password).

## What the backend does
- Saves every order, custom request and newsletter signup in `shop.db` (SQLite).
- Works out order totals itself from `products.json`, so customers cannot change prices.
- When the shop is opened through this server, checkout says "We've received your order" and
  nothing needs to be emailed.

## Changing products or prices
Products are in `index.html` (the `P=[...]` list). After you change a price there, update the same
price in `products.json`. The server uses `products.json` for order totals.

## Putting it online
Any Python host works (Render, Railway, PythonAnywhere). Start command: `python app.py`.
Set `ADMIN_PASSWORD` in the host's settings. Back up `shop.db` regularly.
