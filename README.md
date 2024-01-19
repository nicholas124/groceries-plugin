# Item Management API with FastAPI and Redis

![API Image](link_to_image)

This is a simple FastAPI-based API for managing items, utilizing Redis as the data store. The API allows you to add, list, delete, and remove quantities of items. Each item is represented by an ID, name, and quantity.

## Features
- **Add Item:** POST request to `/items/{item_name}/{quantity}` to add an item with a specified name and quantity. If the item already exists, the quantity is incremented.

- **List Item by ID:** GET request to `/items/{item_id}` retrieves information about a specific item by its ID from Redis.

- **List All Items:** GET request to `/items` provides a list of all items stored in Redis, including their IDs, names, and quantities.

- **Delete Item by ID:** DELETE request to `/items/{item_id}` deletes a specific item by its ID from Redis.

- **Remove Quantity:** DELETE request to `/items/{item_id}/{quantity}` removes a specified quantity from a specific item. If the remaining quantity is zero or less, the item is deleted.

## How to Use
1. Install dependencies using `pip install -r requirements.txt`.
2. Run the API using `uvicorn main:app --reload`.
3. Access the API documentation at [http://127.0.0.1:8000/api/docs](http://127.0.0.1:8000/api/docs) or [http://127.0.0.1:8000/api/redoc](http://127.0.0.1:8000/api/redoc).

Feel free to explore the API and integrate it into your projects.

## Requirements
- [FastAPI](https://fastapi.tiangolo.com/)
- [Redis](https://redis.io/)
- [Uvicorn](https://www.uvicorn.org/)

## Model
The `ItemPayload` model represents the structure of items with optional ID, item name, and quantity.

## Author
[Your Name]  
[Optional: Your Contact Information]

## License
This project is licensed under the [MIT License](LICENSE).
