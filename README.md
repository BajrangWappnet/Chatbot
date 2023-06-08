# wappnet_chat_bot
This is wappnet chat bot.

## Installation

To run this project in your development machine, follow these steps:

Step 1. Fork this repo and clone your fork:

    git clone https://github.com/Wappnet-Systems/openai_invoice_parser.git

Step 2. Create a virtual environment and activate:

    python3 -m venv .venv

Step 3. Install dependencies in virtual environment .venv:

    pip install -r requirements.txt

Step 4. Setup for rasa chatbot :

    - Go into rasa_chatbot directory.
    - Run Cmd -> Rasa train 
    - Run a server using cmd -> rasa run actions  (In a terminal 1 for using custom action file that we have creted in code)
    - Run another server using cmd - > rasa run --enable-api --cors "*" (Run this CMD on another termina. This will start the chatbot server on http://localhost:5005.  )


Step 5. Setup for widget 

    - Go into widget directory
    - Then make some adjustment into  static > js > constant.js
        - const action_name = "action_hello_world";
        - const rasa_server_url = "http://localhost:5005/webhooks/rest/webhook";
        - const sender_id = uuidv4();
    - In rasa_servel_url as we need.
    - Run the widget on any server it will use the rasa_chatbot localhost to handle request.

Step 6. Use the widget to access the rasa chat bot.

