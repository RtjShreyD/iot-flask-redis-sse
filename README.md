## Flask SSE using Redis

1. Install Redis, following the [redis docs](https://redis.io/topics/quickstart).
2. Clone the repository.
3. Create and Activate python virtual environment.
4. Install requirements `pip install requirements.txt`.
5. Run Redis command in new terminal, `redis-server`.
6. Run App, `python app.py`.
7. Using Postman or any tool send POST request with header *content-type --> text-plain* and send any numerical string.
8. The value should get updated immediately on frontend without reloading it.

9. To stop the redis-server, press Ctrl+C or if the terminal got closed by mistake Redis would still be running, so run `redis-cli shutdown` to close it.

