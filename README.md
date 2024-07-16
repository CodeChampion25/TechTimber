# TechTimber
mycode
class ChatBot:
    def __init__(self, name):
        self.name = name
        self.qna = {
            "hi": "Hello! How can I help you today?",
            "how are you": "I'm just a bot, but I'm here to help you!",
            "what is your name": f"My name is {self.name}.",
            "bye": "Goodbye! Have a great day!"
        }

    def greet(self):
        print(f"Hi! I'm {self.name}, your virtual assistant. Ask me anything or type 'bye' to exit.")

    def get_response(self, user_input):
        return self.qna.get(user_input.lower(), "Sorry, I don't understand that. Can you rephrase?")

    def start_chat(self):
        self.greet()
        while True:
            user_input = input("You: ")
            if user_input.lower() == "bye":
                print("Bot: Goodbye! Have a great day!")
                break
            response = self.get_response(user_input)
            print(f"Bot: {response}")

def main():
    bot_name = "ChatGPT"
    chatbot = ChatBot(bot_name)
    chatbot.start_chat()

if __name__ == "__main__":
    main()
