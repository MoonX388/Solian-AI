
# Solian

Solian is a state-of-the-art mixed-language model designed to handle a wide range of natural language processing tasks with high accuracy and optimal efficiency. The project was developed specifically to meet the needs of industrial and research applications, with a focus on flexibility, scalability, and ease of integration.


## Demo

You can try it at https://solian.com


## Screenshots


![Solian](./.github/solian-ai.png)
# API Reference

## Create Session

```http
curl -X POST https://api.solian.com/v1/sessions \
  -H "Authorization: Bearer $SOLIAN_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "expires_after": { "anchor": "created_at", "seconds": 600 },
    "session": {
      "type": "realtime",
      "model": "gpt-realtime",
      "instructions": "You are a friendly assistant."
    }
  }'
```

| Parameter | Type     | Required | Description        |
| :-------- | :------- | :--------| :----------------- |
| `Authorization` | `string` | **Yes**| Bearer token using your API key |
| `expires_after.seconds` | `integer` | **No**| Session expiration time in seconds |
| `session.type` | `string` | **Yes**| Session type, for example realtime |
| `session.model` | `string` | **Yes**| Model used, example: solian-16464 |
| `session.instructions` | `string` | **Yes**| Additional instructions for assistants |

#### add(num1, num2)

Takes two numbers and returns the sum.


## Usage/Examples

```javascript
from solian_ai import SolianModel

# Inisialisasi model
model = SolianModel()

# Input teks yang ingin diproses
input_text = "Halo, bagaimana kabarmu hari ini?"

# Dapatkan hasil prediksi atau respon dari model
output = model.predict(input_text)

print("Input:", input_text)
print("Output:", output)
```


## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.


## License

- [MIT](https://choosealicense.com/licenses/mit/)
- [GNU](https://)

