# Define a dictionary to store the chatbot's responses
responses = {
    "hello": "Hello! How can I assist you today?",
    "hi": "Hi! What's on your mind?",
    "how are you": "I'm doing great, thanks! How about you?",
    "what's your name": "I'm BlackBoxAI, your friendly chatbot!",
    "goodbye": "Goodbye! It was nice chatting with you.",
    "default": "I didn't understand that. Can you please rephrase?"
}

def chatbot():
    print("Welcome to the chatbot! Type 'goodbye' to exit.")
    while True:
        user_input = input("You: ").lower()
        if user_input in responses:
            print("BlackBoxAI:", responses[user_input])
        elif "help" in user_input:
            print("BlackBoxAI: I can assist you with general queries. Try asking me something!")
        else:
            print("BlackBoxAI:", responses["default"])
        if user_input == "goodbye":
            break

# Run the chatbot
chatbot()
