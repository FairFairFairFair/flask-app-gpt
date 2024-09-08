# flask-app-gpt (sentiment) api

## Template openai connect model
```python
import openai

# Set your OpenAI API key
openai.api_key = "your-openai-api-key"

# Define the text you want to analyze or interact with
text = "ฝนกกลางคืนรุ้งกินน้ำ"

# Make a request to the OpenAI GPT-3.5 API
response = openai.ChatCompletion.create(
    model="gpt-3.5-turbo-0125",
    messages=[
        {"role": "system", "content": "ใช้ชื่อเพลงต่อไปนี้แต่งเพลงให้หน่อย"},
        {"role": "user", "content": text}
    ]
)

# Extract the response text
response_text = response['choices'][0]['message']['content'].strip()

print("Response from GPT-3.5:", response_text)
```
