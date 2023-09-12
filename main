import time
import random
import string
import requests
import json

# Replace with your Discord webhook URL
webhook_url = "https://discord.com/api/webhooks/1151212724936777789/A0AgeE6zuuvnZdMAuWuZFVLgaw3DfLaB_sOVWMmT5MQzTZl5NsVMQHJX2c2OGsaTI6pG"

def generate_key(length):
    characters = string.ascii_letters + string.digits
    key = ''.join(random.choice(characters) for _ in range(length))
    return key

while True:
    # Generate a new key
    new_key = generate_key(16)  # You can adjust the key length as needed

    # Prepare the message for Discord
    message = {
        "content": f"New Key: {new_key}"
    }

    # Send the message to the Discord webhook
    response = requests.post(webhook_url, data=json.dumps(message), headers={"Content-Type": "application/json"})

    if response.status_code == 204:
        print("Key sent successfully!")

    # Sleep for 24 hours (86400 seconds)
    time.sleep(86400)
