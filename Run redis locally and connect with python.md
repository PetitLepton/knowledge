## Start redis interactively

```bash
docker run -it -p 6379:6379 redis:latest
```

## Connect to the redis container in the shell

Get the container name through
```bash
docker ps | grep redis
```

With the name `name`, run
```bash
docker exec -it name redis-cli 
```


## Connect to the redis container with python
```python
import redis
r = redis.Redis(decode_responses=True, host="0.0.0.0")
r.ping()

```