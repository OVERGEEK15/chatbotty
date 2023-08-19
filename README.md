import random

# Define a list of greetings and responses
greetings = ["hello", "hi", "hey", "howdy"]
responses = ["Hello!", "Hi there!", "Hey!", "How can I help you today?"]

# Function to generate a response
def respond(input_text):
    input_text = input_text.lower()
    for word in greetings:
        if word in input_text:
            return random.choice(responses)
    return "I'm not sure how to respond to that."

# Main loop for the chatbot
while True:
    user_input = input("You: ")
    if user_input.lower() == "exit":
        print("Bot: Goodbye!")
        break
    else:
        bot_response = respond(user_input)
        print("Bot:", bot_response)

